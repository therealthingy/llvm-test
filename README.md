```shell
❯ ./run_demo
+ echo /Users/gg/.cargo/bin:/opt/homebrew/opt/llvm/bin:/opt/homebrew/bin:/opt/homebrew/sbin:/usr/local/bin:/usr/bin:/bin:/usr/local/sbin:/usr/sbin:/sbin:/var/run/com.apple.security.cryptexd/codex.system/bootstrap/usr/local/bin:/var/run/com.apple.security.cryptexd/codex.system/bootstrap/usr/bin:/var/run/com.apple.security.cryptexd/codex.system/bootstrap/usr/appleinternal/bin:/opt/X11/bin:/Library/Apple/usr/bin:/Library/TeX/texbin:/Applications/Wireshark.app/Contents/MacOS:/Applications/Little Snitch.app/Contents/Components:/usr/local/opt/binutils/bin:/Applications/Tools/Virtualization/VMware Fusion.app/Contents/Public:/Applications/Development/iTerm.app/Contents/Resources/utilities:/Users/gg/.local/bin
/Users/gg/.cargo/bin:/opt/homebrew/opt/llvm/bin:/opt/homebrew/bin:/opt/homebrew/sbin:/usr/local/bin:/usr/bin:/bin:/usr/local/sbin:/usr/sbin:/sbin:/var/run/com.apple.security.cryptexd/codex.system/bootstrap/usr/local/bin:/var/run/com.apple.security.cryptexd/codex.system/bootstrap/usr/bin:/var/run/com.apple.security.cryptexd/codex.system/bootstrap/usr/appleinternal/bin:/opt/X11/bin:/Library/Apple/usr/bin:/Library/TeX/texbin:/Applications/Wireshark.app/Contents/MacOS:/Applications/Little Snitch.app/Contents/Components:/usr/local/opt/binutils/bin:/Applications/Tools/Virtualization/VMware Fusion.app/Contents/Public:/Applications/Development/iTerm.app/Contents/Resources/utilities:/Users/gg/.local/bin
+ uname -smr
Darwin 24.4.0 arm64
+ cmake --version
+ sed -n 1p
cmake version 4.0.0
+ ninja --version
1.12.1
+ cmake --workflow --preset llvm_makefiles_scan
Executing workflow step 1 of 2: configure preset "llvm_makefiles_scan"

-- The CXX compiler identification is Clang 20.1.1
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Check for working CXX compiler: /opt/homebrew/opt/llvm/bin/clang++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Configuring done (0.4s)
-- Generating done (0.0s)
-- Build files have been written to: /Users/gg/Downloads/llvm-test/build-llvm_makefiles_scan

Executing workflow step 2 of 2: build preset "llvm_makefiles_scan"

[ 50%] Building CXX object CMakeFiles/test.dir/test.cpp.o
[100%] Linking CXX executable test
[100%] Built target test
+ cmake --workflow --preset llvm_ninja_noscan
Executing workflow step 1 of 2: configure preset "llvm_ninja_noscan"

-- The CXX compiler identification is Clang 20.1.1
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Check for working CXX compiler: /opt/homebrew/opt/llvm/bin/clang++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Configuring done (0.4s)
-- Generating done (0.0s)
-- Build files have been written to: /Users/gg/Downloads/llvm-test/build-llvm_ninja_noscan

Executing workflow step 2 of 2: build preset "llvm_ninja_noscan"

[2/2] Linking CXX executable test
+ cmake --workflow --preset llvm_ninja_scan
Executing workflow step 1 of 2: configure preset "llvm_ninja_scan"

-- The CXX compiler identification is Clang 20.1.1
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Check for working CXX compiler: /opt/homebrew/opt/llvm/bin/clang++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Configuring done (0.4s)
-- Generating done (0.0s)
-- Build files have been written to: /Users/gg/Downloads/llvm-test/build-llvm_ninja_scan

Executing workflow step 2 of 2: build preset "llvm_ninja_scan"

[1/4] Scanning /Users/gg/Downloads/llvm-test/test.cpp for CXX dependencies
FAILED: CMakeFiles/test.dir/test.cpp.o.ddi
"/opt/homebrew/Cellar/llvm/20.1.1/bin/clang-scan-deps" -format=p1689 -- /opt/homebrew/opt/llvm/bin/clang++   -g -std=gnu++23 -arch arm64 -x c++ /Users/gg/Downloads/llvm-test/test.cpp -c -o CMakeFiles/test.dir/test.cpp.o -resource-dir "/opt/homebrew/Cellar/llvm/20.1.1/lib/clang/20" -MT CMakeFiles/test.dir/test.cpp.o.ddi -MD -MF CMakeFiles/test.dir/test.cpp.o.ddi.d > CMakeFiles/test.dir/test.cpp.o.ddi.tmp && mv CMakeFiles/test.dir/test.cpp.o.ddi.tmp CMakeFiles/test.dir/test.cpp.o.ddi
Error while scanning dependencies for /Users/gg/Downloads/llvm-test/test.cpp:
In file included from /Users/gg/Downloads/llvm-test/test.cpp:1:
In file included from /opt/homebrew/opt/llvm/bin/../include/c++/v1/iostream:45:
In file included from /opt/homebrew/opt/llvm/bin/../include/c++/v1/ios:223:
In file included from /opt/homebrew/opt/llvm/bin/../include/c++/v1/__locale:14:
In file included from /opt/homebrew/opt/llvm/bin/../include/c++/v1/__locale_dir/locale_base_api.h:115:
In file included from /opt/homebrew/opt/llvm/bin/../include/c++/v1/__locale_dir/support/apple.h:18:
/opt/homebrew/opt/llvm/bin/../include/c++/v1/__locale_dir/support/bsd_like.h:21:10: fatal error: 'time.h' file not found
ninja: build stopped: subcommand failed.
```
