# Installing Zathura Mupdf extension
## Problem:
```
// This actually isn't the original error flag but something very similar.
relocation R_X86_64_32 against `vtable for Torch::MemoryDataSet' can not be used 
when making a shared object; recompile with -fPIC
```
## Solution:
```
// Clean everything for recompiliation on the Mupdf build; not the extension with Zathura (if needed)
sudo make clean

sudo CFLAGS="-fPIC" CXXFLAGS="-fPIC" make prefix=/usr/local install 

cd /path/to/zathura-mupdf-x/build

ninja 

ninja install
```

## Explanation:
-fPIC allowed the library to be shared around.
