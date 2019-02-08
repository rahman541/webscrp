## Web Scrapw with C++
Build:
```sh
rmdir /s/q build
cmake -Bbuild .
# Debug / Release
cmake --build build
cmake --build build --config Release
```

## Build static library (Windows)
### Zlib
1. Download https://www.zlib.net/
2. Build static lib
```sh
cd <inside zlib folder>
cmake -Bbuild .
cmake --build build --config Release
```
3. Copy header file inside zlib folder to `dependencies/zlib-1.2.11/include`
4. Copy `*.lib` file inside Release folder to `dependencies/zlib-1.2.11/lib`

### libCurl
1. Download Curl `curl-7.64.0.zip` https://curl.haxx.se/download.html
2. Open `Visual Studio Command Prompt <vstudio_version>`
```
cd <inside curl folder>/winbuild
Set RTLIBCFG=static
nmake /f MakeFile.vc mode=static DEBUG=no MACHINE=x86
```
3. Copy `libcurl-vc-x86-release-static-ipv6-sspi-winssl` to `dependency` folder
