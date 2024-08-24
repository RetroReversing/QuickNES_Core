# RetroReversing Core for NES

# Building
To build:
```
git submodule update --init --recursive
make
```

# Running
To run in MacOSX:
```bash
/Applications/RetroArch.app/Contents/MacOS/RetroArch -v -L quicknes_libretro.dylib yourgame.nes
```

# Possible Errors

If you get the error:
```
libRetroReversing/cdl/CDL.hpp:21:26: error: no member named 'fs' in namespace 'std'
     namespace fs = std::fs::filesystem;
```

Then change CDL.hpp to:
```
  namespace fs = std::__fs::filesystem;
```