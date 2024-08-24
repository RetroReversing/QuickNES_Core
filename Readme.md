# RetroReversing Core for NES

# Building
To build:
```
git submodule update --init --recursive
make
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