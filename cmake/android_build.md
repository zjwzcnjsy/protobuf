## android的编译方法
``` bash
mkdir android_build
cd android_build
cmake -DCMAKE_TOOLCHAIN_FILE=../android.toolchain.cmake -G"MinGW Makefiles" -DCMAKE_MAKE_PROGRAM="%NDK_HOME%/prebuilt/windows-x86_64/bin/make.exe" -DANDROID_NDK="%NDK_HOME%" -DANDROID_NATIVE_API_LEVEL=android-21 -DCMAKE_BUILD_TYPE=Release -DANDROID_ABI="arm64-v8a" ..
cmake --build .
```
其中，`NDK_HOME`为ndk所在的目录。
具体参考android.toolchain.cmake