# MacOS
```shell
❯ ./run_demo
+ uname -smr
Darwin 24.4.0 arm64
+ cmake --version
+ sed -n 1p
cmake version 4.0.0
+ ninja --version
1.12.1
+ cmake --workflow --preset llvm19
Executing workflow step 1 of 2: configure preset "llvm19"

-- Configuring done (0.1s)
-- Generating done (0.0s)
-- Build files have been written to: /Users/gary/Downloads/llvm-test/build-llvm19

Executing workflow step 2 of 2: build preset "llvm19"

[1/3] Generating CXX dyndep file CMakeFiles/test.dir/CXX.dd
+ cmake --workflow --preset llvm20
Executing workflow step 1 of 2: configure preset "llvm20"

-- Configuring done (0.1s)
-- Generating done (0.0s)
-- Build files have been written to: /Users/gary/Downloads/llvm-test/build-llvm20

Executing workflow step 2 of 2: build preset "llvm20"

[1/4] Scanning /Users/gary/Downloads/llvm-test/test.cpp for CXX dependencies
FAILED: CMakeFiles/test.dir/test.cpp.o.ddi
"/opt/homebrew/Cellar/llvm/20.1.1/bin/clang-scan-deps" -format=p1689 -- /opt/homebrew/opt/llvm/bin/clang++   -g -std=gnu++23 -arch arm64 -x c++ /Users/gary/Downloads/llvm-test/test.cpp -c -o CMakeFiles/test.dir/test.cpp.o -resource-dir "/opt/homebrew/Cellar/llvm/20.1.1/lib/clang/20" -MT CMakeFiles/test.dir/test.cpp.o.ddi -MD -MF CMakeFiles/test.dir/test.cpp.o.ddi.d > CMakeFiles/test.dir/test.cpp.o.ddi.tmp && mv CMakeFiles/test.dir/test.cpp.o.ddi.tmp CMakeFiles/test.dir/test.cpp.o.ddi
Error while scanning dependencies for /Users/gary/Downloads/llvm-test/test.cpp:
In file included from /Users/gary/Downloads/llvm-test/test.cpp:1:
In file included from /opt/homebrew/opt/llvm/bin/../include/c++/v1/iostream:45:
In file included from /opt/homebrew/opt/llvm/bin/../include/c++/v1/ios:223:
In file included from /opt/homebrew/opt/llvm/bin/../include/c++/v1/__locale:14:
In file included from /opt/homebrew/opt/llvm/bin/../include/c++/v1/__locale_dir/locale_base_api.h:115:
In file included from /opt/homebrew/opt/llvm/bin/../include/c++/v1/__locale_dir/support/apple.h:18:
/opt/homebrew/opt/llvm/bin/../include/c++/v1/__locale_dir/support/bsd_like.h:21:10: fatal error: 'time.h' file not found
ninja: build stopped: subcommand failed.


❯ ./build-llvm19/test
Hello World%
❯ ./build-llvm20/test
zsh: no such file or directory: ./build-llvm20/test
```
