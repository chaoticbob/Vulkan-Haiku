**Source**: https://github.com/chaoticbob/spirv-tools/tree/haiku

### 1. Getting Source ###
Clone the source from the forked repo - make sure you're using the **`haiku`** branch.

```
git clone -b haiku --recursive https://github.com/chaoticbob/SPIRV-Tools.git
cd SPIRV-Tools/external
git clone https://github.com/KhronosGroup/SPIRV-Headers.git
```

### 2. Generate Build Files ###
If you're not familiar with in-source vs out-of-source build - please read up on this. This step assumes that you're using an out-of-source build directory.
```
cmake <path to SPIRV-Tools source>
```

### 3. Build ###
Use **`make`** to build. **`N`** is the number of build processes. **`-j N`** is optional, if it's omitted a single process is used for building.
```
make -j N
```
