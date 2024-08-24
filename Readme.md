# RetroReversing Core for NES



# Running
To run in MacOSX:
```bash
/Applications/RetroArch.app/Contents/MacOS/RetroArch -v -L quicknes_libretro.dylib yourgame.nes
```

The following should automatically popup in your browser:
![UI](https://github.com/user-attachments/assets/3cab894d-5821-41b4-a369-ade4a2c38069)

Click Run/Resume to run  the game.

After pausing it will save data to:
~/Documents/RetroArch/system/RE_projects/NES/

Unless you have a different RetroArch system directory.

---
# Building
To build:
```
git submodule update --init --recursive
make
```

## Possible Build Errors

If you get the error:
```
libRetroReversing/cdl/CDL.hpp:21:26: error: no member named 'fs' in namespace 'std'
     namespace fs = std::fs::filesystem;
```

Then change CDL.hpp to:
```
  namespace fs = std::__fs::filesystem;
```
