## HOW TO

- put `Sim` folder into `<LLVM-PROJECT>/llvm/lib/Target`
- add `Sim` to `LLVM_ALL_TARGETS` in `<LLVM-PROJECT>/llvm/CMakeLists.txt`
- add `sim` to `enum ArchType` in `<LLVM-PROJECT>/llvm/include/llvm/ADT/Triple.h`
- add

```
elseif (LLVM_NATIVE_ARCH MATCHES "sim")
  set(LLVM_NATIVE_ARCH Sim)
```

after

```
if (LLVM_NATIVE_ARCH MATCHES "i[2-6]86")
  set(LLVM_NATIVE_ARCH X86)
```

in `<LLVM-PROJECT>/llvm/cmake/config-ix.cmake`
