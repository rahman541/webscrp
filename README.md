## Web Scrapw with C++

## Lib Build (Dev)
### Zlib
1. Download https://www.zlib.net/
2. Build static lib
```
cd <inside zlib folder>
cmake -Bbuild .
cmake --build build --config Release
```
3. Copy header file inside zlib folder to `dependencies/zlib-1.2.11/include`
4. Copy `*.lib` file inside Release folder to `dependencies/zlib-1.2.11/lib`
