Source: https://github.com/chaoticbob/swiftshader/tree/haiku

### 1. Getting Source ###
Clone the source from the forked repo - make sure you're using the **`haiku`** branch.

```
git clone -b haiku --recursive https://github.com/chaoticbob/swiftshader.git
```

### 2. Generate Build Files ###
If you're not familiar with in-source vs out-of-source build - please read up on this. This step assumes that you're using an out-of-source build directory.
```
cmake <path to SwiftShader source> -DSWIFTSHADER_BUILD_EGL=FALSE \
-DSWIFTSHADER_BUILD_GLESv2=FALSE -DSWIFTSHADER_BUILD_PVR=FALSE \
-DSWIFTSHADER_BUILD_TESTS=FALSE -DSWIFTSHADER_WARNINGS_AS_ERRORS=FALSE \
-DREACTOR_ENABLE_MEMORY_SANITIZER_INSTRUMENTATION=FALSE \
-DSWIFTSHADER_ENABLE_ASTC=FALSE -DSPIRV_SKIP_EXECUTABLES=1
```

### 3. Build ###
Use **`make`** to build. **`N`** is the number of build processes. **`-j N`** is optional, if it's omitted a single process is used for building.
```
make -j N
```

### 3. Build Output ###
The built binaries are in the **`Haiku`** directory of your build location.
