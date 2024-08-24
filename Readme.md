# RetroReversing Core for NES

# Building
To build:
```
git submodule update --init --recursive
make
```

![UI](https://github.com/user-attachments/assets/3cab894d-5821-41b4-a369-ade4a2c38069)


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
