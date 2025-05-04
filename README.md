murka2006@murka:~/Mari-Mur-Meow/workspace/projects$ cd
murka2006@murka:~$ export GITHUB_USERNAME=Mari-Mur-Meow
murka2006@murka:~$ alias gsed =sed 
alias gsed='sed'
bash: alias: =sed: не найден
murka2006@murka:~$ alias gsed=sed 
murka2006@murka:~$ cd ${GITHUB_USERNAME}/workspace
murka2006@murka:~/Mari-Mur-Meow/workspace$ pushd .
~/Mari-Mur-Meow/workspace ~/Mari-Mur-Meow/workspace ~/Mari-Mur-Meow/workspace
murka2006@murka:~/Mari-Mur-Meow/workspace$ source scripts/activate
murka2006@murka:~/Mari-Mur-Meow/workspace$ git clone https://github.com/${GITHUB_USERNAME}/lab06 projects/lab07
Клонирование в «projects/lab07»...
remote: Enumerating objects: 89, done.
remote: Counting objects: 100% (89/89), done.
remote: Compressing objects: 100% (45/45), done.
remote: Total 89 (delta 37), reused 80 (delta 33), pack-reused 0 (from 0)
Получение объектов: 100% (89/89), 29.63 КиБ | 9.88 МиБ/с, готово.
Определение изменений: 100% (37/37), готово.
murka2006@murka:~/Mari-Mur-Meow/workspace$ cd projects/lab07
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ git remote remove origin
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ git remote add origin https://github.com/${GITHUB_USERNAME}/lab07
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ mkdir -p cmake
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ wget https://raw.githubusercontent.com/cpp-pm/gate/master/cmake/HunterGate.cmake -O cmake/HunterGate.cmake
--2025-05-04 22:33:15--  https://raw.githubusercontent.com/cpp-pm/gate/master/cmake/HunterGate.cmake
Распознаётся raw.githubusercontent.com (raw.githubusercontent.com)… 185.199.108.133, 185.199.109.133, 185.199.110.133, ...
Подключение к raw.githubusercontent.com (raw.githubusercontent.com)|185.199.108.133|:443... соединение установлено.
HTTP-запрос отправлен. Ожидание ответа… 200 OK
Длина: 17231 (17K) [text/plain]
Сохранение в: ‘cmake/HunterGate.cmake’

cmake/HunterGate.cm 100%[===================>]  16,83K  --.-KB/s    за 0,001s  

2025-05-04 22:33:15 (22,4 MB/s) - ‘cmake/HunterGate.cmake’ сохранён [17231/17231]

murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ gsed -i '/cmake_minimum_required(VERSION 3.4)/a \
> include("cmake/HunterGate.cmake") \
HunterGate( \
    URL "https://github.com/cpp-pm/hunter/archive/v0.23.308.tar.gz" \
    SHA1 "23f1b5a0acffae50fdad2338bc843a8e7b6e1ebb" \
)' CMakeLists.txt
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ git rm -rf third-party/gtest
rm 'third-party/gtest'
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ sed -i '/cmake_minimum_required(VERSION 3.4)/a \
include("cmake/HunterGate.cmake") \
HunterGate( \
    URL "https://github.com/cpp-pm/hunter/archive/v0.23.308.tar.gz" \
    SHA1 "23f1b5a0acffae50fdad2338bc843a8e7b6e1ebb" \
)' CMakeLists.txt
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ gsed -i '/set(PRINT_VERSION_STRING "v${PRINT_VERSION}")/a \ hunter_add_package(GTest)\
find_package(GTest CONFIG REQUIRED)' CMakeLists.txt
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ gsed -i '/set(PRINT_VERSION_STRING "v${PRINT_VERSION}")/a \
 hunter_add_package(GTest)\
find_package(GTest CONFIG REQUIRED)'\ CMakeLists.txt
sed: отсутствуют входные файлы
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ gsed -i '/set(PRINT_VERSION_STRING "v${PRINT_VERSION}")/a \
 hunter_add_package(GTest)\
find_package(GTest CONFIG REQUIRED)' CMakeLists.txt
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ gsed -i 's/add_subdirectory(third-party\/gtest)//' CMakeLists.txt
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ marialuneva@1511:~$ exmurka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ gsed -i 's/add_subdiremurka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ alias gsed =sed 
alias gsed='sed'
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ gsed -i 's/gtest_main/GTest::main/' CMakeLists.txt
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ rm -rf third-party/gtest
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ mkdir -p third-party
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ git clone https://github.com/google/googletest.git third-party/gtest
Клонирование в «third-party/gtest»...
remote: Enumerating objects: 28040, done.
remote: Counting objects: 100% (261/261), done.
remote: Compressing objects: 100% (168/168), done.
remote: Total 28040 (delta 166), reused 95 (delta 93), pack-reused 27779 (from 4)
Получение объектов: 100% (28040/28040), 13.56 МиБ | 161.00 КиБ/с, готово.
Определение изменений: 100% (20767/20767), готово.
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ cmake -H. -B_builds -DBUILD_TESTS=ON
CMake Deprecation Warning at CMakeLists.txt:1 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


-- Found Threads: TRUE  
-- Configuring done (0.0s)
-- Generating done (0.0s)
-- Build files have been written to: /home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/_builds
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ cmake --build _builds
[  8%] Building CXX object CMakeFiles/print.dir/sources/print.cpp.o
[ 16%] Linking CXX static library libprint.a
[ 16%] Built target print
[ 25%] Building CXX object third-party/gtest/googletest/CMakeFiles/gtest.dir/src/gtest-all.cc.o
[ 33%] Linking CXX static library ../../../lib/libgtest.a
[ 33%] Built target gtest
[ 41%] Building CXX object third-party/gtest/googletest/CMakeFiles/gtest_main.dir/src/gtest_main.cc.o
[ 50%] Linking CXX static library ../../../lib/libgtest_main.a
[ 50%] Built target gtest_main
[ 58%] Building CXX object CMakeFiles/check.dir/tests/test1.cpp.o
[ 66%] Linking CXX executable check
[ 66%] Built target check
[ 75%] Building CXX object third-party/gtest/googlemock/CMakeFiles/gmock.dir/src/gmock-all.cc.o
[ 83%] Linking CXX static library ../../../lib/libgmock.a
[ 83%] Built target gmock
[ 91%] Building CXX object third-party/gtest/googlemock/CMakeFiles/gmock_main.dir/src/gmock_main.cc.o
[100%] Linking CXX static library ../../../lib/libgmock_main.a
[100%] Built target gmock_main
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ cmake --build _builds --target test
Running tests...
Test project /home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/_builds
    Start 1: check
1/1 Test #1: check ............................   Passed    0.00 sec

100% tests passed, 0 tests failed out of 1

Total Test time (real) =   0.00 sec
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ ls -la $HOME/.hunter
итого 12
drwxrwxr-x  3 murka2006 murka2006 4096 мая  1 23:04 .
drwxr-x--- 29 murka2006 murka2006 4096 мая  1 23:04 ..
drwxrwxr-x  6 murka2006 murka2006 4096 мая  1 23:06 _Base
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ git clone https://github.com/cpp-pm/hunter $HOME/projects/hunter
Клонирование в «/home/murka2006/projects/hunter»...
remote: Enumerating objects: 54528, done.
remote: Counting objects: 100% (1503/1503), done.
remote: Compressing objects: 100% (402/402), done.
remote: Total 54528 (delta 1300), reused 1102 (delta 1100), pack-reused 53025 (from 3)
Получение объектов: 100% (54528/54528), 13.98 МиБ | 202.00 КиБ/с, готово.
Определение изменений: 100% (33936/33936), готово.
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ export HUNTER_ROOT=$HOME/projects/hunter
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ rm -rf _builds
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ cmake -H. -B_builds -DBUILD_TESTS=ON
CMake Deprecation Warning at CMakeLists.txt:1 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


-- The C compiler identification is GNU 13.3.0
-- The CXX compiler identification is GNU 13.3.0
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Check for working C compiler: /usr/bin/cc - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Check for working CXX compiler: /usr/bin/c++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD - Success
-- Found Threads: TRUE  
-- Configuring done (0.3s)
-- Generating done (0.0s)
-- Build files have been written to: /home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/_builds
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ cmake --build _builds
[  8%] Building CXX object CMakeFiles/print.dir/sources/print.cpp.o
[ 16%] Linking CXX static library libprint.a
[ 16%] Built target print
[ 25%] Building CXX object third-party/gtest/googletest/CMakeFiles/gtest.dir/src/gtest-all.cc.o
[ 33%] Linking CXX static library ../../../lib/libgtest.a
[ 33%] Built target gtest
[ 41%] Building CXX object third-party/gtest/googletest/CMakeFiles/gtest_main.dir/src/gtest_main.cc.o
[ 50%] Linking CXX static library ../../../lib/libgtest_main.a
[ 50%] Built target gtest_main
[ 58%] Building CXX object CMakeFiles/check.dir/tests/test1.cpp.o
[ 66%] Linking CXX executable check
[ 66%] Built target check
[ 75%] Building CXX object third-party/gtest/googlemock/CMakeFiles/gmock.dir/src/gmock-all.cc.o
[ 83%] Linking CXX static library ../../../lib/libgmock.a
[ 83%] Built target gmock
[ 91%] Building CXX object third-party/gtest/googlemock/CMakeFiles/gmock_main.dir/src/gmock_main.cc.o
[100%] Linking CXX static library ../../../lib/libgmock_main.a
[100%] Built target gmock_main
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ cmake --build _builds --target test
Running tests...
Test project /home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/_builds
    Start 1: check
1/1 Test #1: check ............................   Passed    0.00 sec

100% tests passed, 0 tests failed out of 1

Total Test time (real) =   0.00 sec
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ cat $HUNTER_ROOT/cmake/configs/default.cmake | grep GTest
  hunter_default_version(GTest VERSION 1.7.0-hunter-6)
  hunter_default_version(GTest VERSION 1.15.2)
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ cat $HUNTER_ROOT/cmake/projects/GTest/hunter.cmake
# Copyright (c) 2013, Ruslan Baratov
# All rights reserved.

# !!! DO NOT PLACE HEADER GUARDS HERE !!!

include(hunter_add_version)
include(hunter_cacheable)
include(hunter_download)
include(hunter_pick_scheme)
include(hunter_cmake_args)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.7.0-hunter"
    URL
    "https://github.com/hunter-packages/gtest/archive/v1.7.0-hunter.tar.gz"
    SHA1
    1ed1c26d11fb592056c1cb912bd3c784afa96eaa
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.7.0-hunter-1"
    URL
    "https://github.com/hunter-packages/gtest/archive/v1.7.0-hunter-1.tar.gz"
    SHA1
    0cb1dcf75e144ad052d3f1e4923a7773bf9b494f
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.7.0-hunter-2"
    URL
    "https://github.com/hunter-packages/gtest/archive/v1.7.0-hunter-2.tar.gz"
    SHA1
    e62b2ef70308f63c32c560f7b6e252442eed4d57
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.7.0-hunter-3"
    URL
    "https://github.com/hunter-packages/gtest/archive/v1.7.0-hunter-3.tar.gz"
    SHA1
    fea7d3020e20f059255484c69755753ccadf6362
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.7.0-hunter-4"
    URL
    "https://github.com/hunter-packages/gtest/archive/v1.7.0-hunter-4.tar.gz"
    SHA1
    9b439c0c25437a083957b197ac6905662a5d901b
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.7.0-hunter-5"
    URL
    "https://github.com/hunter-packages/gtest/archive/v1.7.0-hunter-5.tar.gz"
    SHA1
    796804df3facb074087a4d8ba6f652e5ac69ad7f
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.7.0-hunter-6"
    URL
    "https://github.com/hunter-packages/gtest/archive/v1.7.0-hunter-6.tar.gz"
    SHA1
    64b93147abe287da8fe4e18cfd54ba9297dafb82
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.7.0-hunter-7"
    URL
    "https://github.com/hunter-packages/gtest/archive/v1.7.0-hunter-7.tar.gz"
    SHA1
    19b5c98747768bcd0622714f2ed40f17aee406b2
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.7.0-hunter-8"
    URL
    "https://github.com/hunter-packages/gtest/archive/v1.7.0-hunter-8.tar.gz"
    SHA1
    ac4d2215aa1b1d745a096e5e3b2dbe0c0f229ea5
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.7.0-hunter-9"
    URL
    "https://github.com/hunter-packages/gtest/archive/v1.7.0-hunter-9.tar.gz"
    SHA1
    8a47fe9c4e550f4ed0e2c05388dd291a059223d9
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.7.0-hunter-10"
    URL
    "https://github.com/hunter-packages/gtest/archive/v1.7.0-hunter-10.tar.gz"
    SHA1
    374e6dbe8619ab467c6b1a0b470a598407b172e9
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.7.0-hunter-11"
    URL
    "https://github.com/hunter-packages/gtest/archive/v1.7.0-hunter-11.tar.gz"
    SHA1
    c6ae948ca2bea1d734af01b1069491b00933ed31
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    1.8.0-hunter-p2
    URL
    "https://github.com/hunter-packages/googletest/archive/1.8.0-hunter-p2.tar.gz"
    SHA1
    93148cb8850abe78b76ed87158fdb6b9c48e38c4
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    1.8.0-hunter-p5
    URL https://github.com/hunter-packages/googletest/archive/1.8.0-hunter-p5.tar.gz
    SHA1 3325aa4fc8b30e665c9f73a60f19387b7db36f85
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    1.8.0-hunter-p6
    URL
    "https://github.com/hunter-packages/googletest/archive/1.8.0-hunter-p6.tar.gz"
    SHA1
    f57096bd01c6f8cbef043b312d4d1e82f29648b6
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    1.8.0-hunter-p7
    URL
    "https://github.com/hunter-packages/googletest/archive/1.8.0-hunter-p7.tar.gz"
    SHA1
    4fe083a96d7597f7dce6f453dca01e1d94a1e45b
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    1.8.0-hunter-p8
    URL
    "https://github.com/hunter-packages/googletest/archive/1.8.0-hunter-p8.tar.gz"
    SHA1
    1cdd396b20c8d29f7ea08baaa49673b1c261f545
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    1.8.0-hunter-p9
    URL
    "https://github.com/hunter-packages/googletest/archive/1.8.0-hunter-p9.tar.gz"
    SHA1
    a345f16cb610e0b5dfa7778dc2852b784cfede5b
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    1.8.0-hunter-p10
    URL
    "https://github.com/hunter-packages/googletest/archive/1.8.0-hunter-p10.tar.gz"
    SHA1
    1d92c9f51af756410843b13f8c4e4df09e235394
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.8.0-hunter-p11"
    URL
    "https://github.com/hunter-packages/googletest/archive/1.8.0-hunter-p11.tar.gz"
    SHA1
    76c6aec038f7d7258bf5c4f45c4817b34039d285
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.8.1"
    URL
    "https://github.com/google/googletest/archive/release-1.8.1.tar.gz"
    SHA1
    152b849610d91a9dfa1401293f43230c2e0c33f8
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.10.0"
    URL
    "https://github.com/google/googletest/archive/release-1.10.0.tar.gz"
    SHA1
    9c89be7df9c5e8cb0bc20b3c4b39bf7e82686770
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.10.0-p0"
    URL
    "https://github.com/hunter-packages/googletest/archive/v1.10.0-p0.tar.gz"
    SHA1
    f7c72be12120e018f53cda0e0daa26fab5da7dfc
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.10.0-p1"
    URL
    "https://github.com/hunter-packages/googletest/archive/v1.10.0-p1.tar.gz"
    SHA1
    06a1f667f200ff94d38b608e44c3c8061c7b8f2f
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.11.0"
    URL
    "https://github.com/google/googletest/archive/release-1.11.0.tar.gz"
    SHA1
    7b100bb68db8df1060e178c495f3cbe941c9b058
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.12.1"
    URL
    "https://github.com/google/googletest/archive/release-1.12.1.tar.gz"
    SHA1
    cdddd449d4e3aa7bd421d4519c17139ea1890fe7
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.13.0"
    URL
    "https://github.com/google/googletest/archive/v1.13.0.tar.gz"
    SHA1
    bfa4b5131b6eaac06962c251742c96aab3f7aa78
)

hunter_add_version(
    PACKAGE_NAME
    GTest
    VERSION
    "1.14.0"
    URL
    "https://github.com/google/googletest/archive/v1.14.0.tar.gz"
    SHA1
    2b28c2a3a30d86b1759543ef61fac3c4d69f8c4c
)

hunter_add_version(
        PACKAGE_NAME
        GTest
        VERSION
        "1.15.2"
        URL
        "https://github.com/google/googletest/archive/v1.15.2.tar.gz"
        SHA1
        568d58e26bd4e838449ca7ab8ebc152b3cbd210d
)


if(HUNTER_GTest_VERSION VERSION_LESS 1.8.0 OR HUNTER_GTest_VERSION VERSION_GREATER_EQUAL 1.11.0)
  set(_gtest_license "LICENSE")
else()
  set(_gtest_license "googletest/LICENSE")
endif()

# gtest_force_shared_crt prevents GoogleTest from modifying options
# rather than forcing it to use shared libraries
hunter_cmake_args(
    GTest
    CMAKE_ARGS
    HUNTER_INSTALL_LICENSE_FILES=${_gtest_license}
    gtest_force_shared_crt=TRUE
)

hunter_pick_scheme(DEFAULT url_sha1_cmake)
hunter_cacheable(GTest)
hunter_download(PACKAGE_NAME GTest PACKAGE_INTERNAL_DEPS_ID 1)
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ mkdir cmake/Hunter
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ cat > cmake/Hunter/config.cmake <<EOF
> hunter_config(GTest VERSION 1.7.0-hunter-9)
> EOF
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ mkdir demo
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ cat > demo/main.cpp <<EOF
> #include <print.hpp>

#include <cstdlib>

int main(int argc, char* argv[])
{
  const char* log_path = std::getenv("LOG_PATH");
  if (log_path == nullptr)
  {
    std::cerr << "undefined environment variable: LOG_PATH" << std::endl;
    return 1;
  }
  std::string text;
  while (std::cin >> text)
  {
    std::ofstream out{log_path, std::ios_base::app};
    print(text, out);
    out << std::endl;
  }
}
> EOF
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ gsed -i '/endif()/a\

add_executable(demo ${CMAKE_CURRENT_SOURCE_DIR}/demo/main.cpp)
target_link_libraries(demo print)
install(TARGETS demo RUNTIME DESTINATION bin)
' CMakeLists.txt
sed: -e выражение #1, символ 105: лишние символы после команды
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ gsed -i '/endif()/a\

add_executable(demo ${CMAKE_CURRENT_SOURCE_DIR}/demo/main.cpp)\
target_link_libraries(demo print)\
install(TARGETS demo RUNTIME DESTINATION bin)\
' CMakeLists.txt
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ mkdir tools
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ git submodule add https://github.com/ruslo/polly tools/polly
Клонирование в «/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/tools/polly»...
remote: Enumerating objects: 6578, done.
remote: Counting objects: 100% (32/32), done.
remote: Compressing objects: 100% (15/15), done.
remote: Total 6578 (delta 21), reused 20 (delta 17), pack-reused 6546 (from 1)
Получение объектов: 100% (6578/6578), 1.68 МиБ | 207.00 КиБ/с, готово.
Определение изменений: 100% (4551/4551), готово.
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ tools/polly/bin/polly.py --test
Python version: 3.12
Build dir: /home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/_builds/default
Execute command: [
  `which`
  `cmake`
]

[/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07]> "which" "cmake"

/usr/bin/cmake
Execute command: [
  `cmake`
  `--version`
]

[/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07]> "cmake" "--version"

cmake version 3.28.3

CMake suite maintained and supported by Kitware (kitware.com/cmake).
Execute command: [
  `cmake`
  `-H.`
  `-B/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/_builds/default`
  `-DCMAKE_TOOLCHAIN_FILE=/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/tools/polly/default.cmake`
]

[/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07]> "cmake" "-H." "-B/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/_builds/default" "-DCMAKE_TOOLCHAIN_FILE=/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/tools/polly/default.cmake"

CMake Deprecation Warning at CMakeLists.txt:1 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


-- [polly] Used toolchain: Default
-- The C compiler identification is GNU 13.3.0
-- The CXX compiler identification is GNU 13.3.0
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Check for working C compiler: /usr/bin/cc - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Check for working CXX compiler: /usr/bin/c++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- [hunter] Calculating Toolchain-SHA1
-- [hunter] Calculating Config-SHA1
-- [hunter] HUNTER_ROOT: /home/murka2006/projects/hunter
-- [hunter] [ Hunter-ID: xxxxxxx | Toolchain-ID: fb15dbb | Config-ID: cf272be ]
-- [hunter] GTEST_ROOT: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Install (ver.: 1.15.2)
-- [hunter] Building GTest
loading initial cache file /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/cache.cmake
loading initial cache file /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/args.cmake
-- [polly] Used toolchain: Default
-- The C compiler identification is GNU 13.3.0
-- The CXX compiler identification is GNU 13.3.0
-- Check for working C compiler: /usr/bin/cc - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /usr/bin/c++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Configuring done (0.1s)
-- Generating done (0.0s)
-- Build files have been written to: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Build
[  6%] Creating directories for 'GTest-Release'
[ 12%] Performing download step (download, verify and extract) for 'GTest-Release'
-- Downloading...
   dst='/home/murka2006/projects/hunter/_Base/Download/GTest/1.15.2/568d58e/v1.15.2.tar.gz'
   timeout='none'
   inactivity timeout='none'
-- Using src='https://github.com/google/googletest/archive/v1.15.2.tar.gz'
-- [download 1% complete]
-- [download 2% complete]
-- [download 3% complete]
-- [download 4% complete]
-- [download 5% complete]
-- [download 7% complete]
-- [download 9% complete]
-- [download 10% complete]
-- [download 11% complete]
-- [download 13% complete]
-- [download 14% complete]
-- [download 15% complete]
-- [download 18% complete]
-- [download 21% complete]
-- [download 22% complete]
-- [download 23% complete]
-- [download 32% complete]
-- [download 33% complete]
-- [download 34% complete]
-- [download 35% complete]
-- [download 36% complete]
-- [download 37% complete]
-- [download 38% complete]
-- [download 40% complete]
-- [download 45% complete]
-- [download 50% complete]
-- [download 53% complete]
-- [download 54% complete]
-- [download 55% complete]
-- [download 58% complete]
-- [download 60% complete]
-- [download 61% complete]
-- [download 62% complete]
-- [download 64% complete]
-- [download 66% complete]
-- [download 69% complete]
-- [download 71% complete]
-- [download 73% complete]
-- [download 74% complete]
-- [download 76% complete]
-- [download 78% complete]
-- [download 80% complete]
-- [download 82% complete]
-- [download 84% complete]
-- [download 86% complete]
-- [download 88% complete]
-- [download 90% complete]
-- [download 91% complete]
-- [download 93% complete]
-- [download 99% complete]
-- [download 100% complete]
-- verifying file...
       file='/home/murka2006/projects/hunter/_Base/Download/GTest/1.15.2/568d58e/v1.15.2.tar.gz'
-- Downloading... done
-- extracting...
     src='/home/murka2006/projects/hunter/_Base/Download/GTest/1.15.2/568d58e/v1.15.2.tar.gz'
     dst='/home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Source'
-- extracting... [tar xfz]
-- extracting... [analysis]
-- extracting... [rename]
-- extracting... [clean up]
-- extracting... done
[ 18%] No update step for 'GTest-Release'
[ 25%] No patch step for 'GTest-Release'
[ 31%] Performing configure step for 'GTest-Release'
loading initial cache file /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/cache.cmake
loading initial cache file /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/args.cmake
-- [polly] Used toolchain: Default
-- The C compiler identification is GNU 13.3.0
-- The CXX compiler identification is GNU 13.3.0
-- Check for working C compiler: /usr/bin/cc - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /usr/bin/c++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD - Success
-- Found Threads: TRUE
-- Configuring done (0.2s)
-- Generating done (0.0s)
-- Build files have been written to: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Build/GTest-Release-prefix/src/GTest-Release-build
[ 37%] Performing build step for 'GTest-Release'
[ 12%] Building CXX object googletest/CMakeFiles/gtest.dir/src/gtest-all.cc.o
[ 25%] Linking CXX static library ../lib/libgtest.a
[ 25%] Built target gtest
[ 37%] Building CXX object googlemock/CMakeFiles/gmock.dir/src/gmock-all.cc.o
[ 50%] Building CXX object googletest/CMakeFiles/gtest_main.dir/src/gtest_main.cc.o
[ 62%] Linking CXX static library ../lib/libgtest_main.a
[ 62%] Built target gtest_main
[ 75%] Linking CXX static library ../lib/libgmock.a
[ 75%] Built target gmock
[ 87%] Building CXX object googlemock/CMakeFiles/gmock_main.dir/src/gmock_main.cc.o
[100%] Linking CXX static library ../lib/libgmock_main.a
[100%] Built target gmock_main
[ 43%] Performing install step for 'GTest-Release'
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/internal
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/internal/custom
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/internal/custom/gmock-generated-actions.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/internal/custom/gmock-matchers.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/internal/custom/README.md
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/internal/custom/gmock-port.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/internal/gmock-port.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/internal/gmock-internal-utils.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/internal/gmock-pp.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/gmock-actions.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/gmock-more-matchers.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/gmock-function-mocker.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/gmock-spec-builders.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/gmock.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/gmock-matchers.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/gmock-nice-strict.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/gmock-cardinalities.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/gmock-more-actions.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/lib/libgmock.a
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/lib/libgmock_main.a
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/lib/pkgconfig/gmock.pc
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/lib/pkgconfig/gmock_main.pc
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/lib/cmake/GTest/GTestTargets.cmake
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/lib/cmake/GTest/GTestTargets-release.cmake
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/lib/cmake/GTest/GTestConfigVersion.cmake
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/lib/cmake/GTest/GTestConfig.cmake
-- Up-to-date: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/gtest-message.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/gtest-spi.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/gtest.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/internal
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/internal/gtest-port.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/internal/gtest-death-test-internal.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/internal/gtest-param-util.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/internal/gtest-port-arch.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/internal/gtest-type-util.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/internal/custom
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/internal/custom/gtest.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/internal/custom/gtest-port.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/internal/custom/gtest-printers.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/internal/custom/README.md
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/internal/gtest-internal.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/internal/gtest-string.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/internal/gtest-filepath.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/gtest-printers.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/gtest-assertion-result.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/gtest-param-test.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/gtest_prod.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/gtest_pred_impl.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/gtest-typed-test.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/gtest-death-test.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/gtest-matchers.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/gtest-test-part.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/lib/libgtest.a
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/lib/libgtest_main.a
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/lib/pkgconfig/gtest.pc
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/lib/pkgconfig/gtest_main.pc
loading initial cache file /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/args.cmake
[ 50%] Completed 'GTest-Release'
[ 50%] Built target GTest-Release
[ 56%] Creating directories for 'GTest-Debug'
[ 62%] Performing download step (download, verify and extract) for 'GTest-Debug'
-- verifying file...
       file='/home/murka2006/projects/hunter/_Base/Download/GTest/1.15.2/568d58e/v1.15.2.tar.gz'
-- File already exists and hash match (skip download):
  file='/home/murka2006/projects/hunter/_Base/Download/GTest/1.15.2/568d58e/v1.15.2.tar.gz'
  SHA1='568d58e26bd4e838449ca7ab8ebc152b3cbd210d'
-- extracting...
     src='/home/murka2006/projects/hunter/_Base/Download/GTest/1.15.2/568d58e/v1.15.2.tar.gz'
     dst='/home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Source'
-- extracting... [tar xfz]
-- extracting... [analysis]
-- extracting... [rename]
-- extracting... [clean up]
-- extracting... done
[ 68%] No update step for 'GTest-Debug'
[ 75%] No patch step for 'GTest-Debug'
[ 81%] Performing configure step for 'GTest-Debug'
loading initial cache file /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/cache.cmake
loading initial cache file /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/args.cmake
-- [polly] Used toolchain: Default
-- The C compiler identification is GNU 13.3.0
-- The CXX compiler identification is GNU 13.3.0
-- Check for working C compiler: /usr/bin/cc - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /usr/bin/c++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD - Success
-- Found Threads: TRUE
-- Configuring done (0.2s)
-- Generating done (0.0s)
-- Build files have been written to: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Build/GTest-Debug-prefix/src/GTest-Debug-build
[ 87%] Performing build step for 'GTest-Debug'
[ 12%] Building CXX object googletest/CMakeFiles/gtest.dir/src/gtest-all.cc.o
[ 25%] Linking CXX static library ../lib/libgtestd.a
[ 25%] Built target gtest
[ 50%] Building CXX object googlemock/CMakeFiles/gmock.dir/src/gmock-all.cc.o
[ 50%] Building CXX object googletest/CMakeFiles/gtest_main.dir/src/gtest_main.cc.o
[ 62%] Linking CXX static library ../lib/libgtest_maind.a
[ 62%] Built target gtest_main
[ 75%] Linking CXX static library ../lib/libgmockd.a
[ 75%] Built target gmock
[ 87%] Building CXX object googlemock/CMakeFiles/gmock_main.dir/src/gmock_main.cc.o
[100%] Linking CXX static library ../lib/libgmock_maind.a
[100%] Built target gmock_main
[ 93%] Performing install step for 'GTest-Debug'
-- Up-to-date: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include
-- Up-to-date: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock
-- Up-to-date: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/internal
-- Up-to-date: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/internal/custom
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/internal/custom/gmock-generated-actions.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/internal/custom/gmock-matchers.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/internal/custom/README.md
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/internal/custom/gmock-port.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/internal/gmock-port.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/internal/gmock-internal-utils.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/internal/gmock-pp.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/gmock-actions.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/gmock-more-matchers.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/gmock-function-mocker.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/gmock-spec-builders.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/gmock.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/gmock-matchers.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/gmock-nice-strict.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/gmock-cardinalities.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gmock/gmock-more-actions.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/lib/libgmockd.a
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/lib/libgmock_maind.a
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/lib/pkgconfig/gmock.pc
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/lib/pkgconfig/gmock_main.pc
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/lib/cmake/GTest/GTestTargets.cmake
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/lib/cmake/GTest/GTestTargets-debug.cmake
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/lib/cmake/GTest/GTestConfigVersion.cmake
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/lib/cmake/GTest/GTestConfig.cmake
-- Up-to-date: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include
-- Up-to-date: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/gtest-message.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/gtest-spi.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/gtest.h
-- Up-to-date: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/internal
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/internal/gtest-port.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/internal/gtest-death-test-internal.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/internal/gtest-param-util.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/internal/gtest-port-arch.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/internal/gtest-type-util.h
-- Up-to-date: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/internal/custom
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/internal/custom/gtest.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/internal/custom/gtest-port.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/internal/custom/gtest-printers.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/internal/custom/README.md
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/internal/gtest-internal.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/internal/gtest-string.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/internal/gtest-filepath.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/gtest-printers.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/gtest-assertion-result.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/gtest-param-test.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/gtest_prod.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/gtest_pred_impl.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/gtest-typed-test.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/gtest-death-test.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/gtest-matchers.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/include/gtest/gtest-test-part.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/lib/libgtestd.a
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/lib/libgtest_maind.a
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/lib/pkgconfig/gtest.pc
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/Install/lib/pkgconfig/gtest_main.pc
loading initial cache file /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest/args.cmake
[100%] Completed 'GTest-Debug'
[100%] Built target GTest-Debug
-- [hunter] Build step successful (dir: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Build/GTest)
-- [hunter] Cache saved: /home/murka2006/projects/hunter/_Base/Cache/raw/14461a96b7951d8abea07ff1d04425f1d27de742.tar.bz2
-- Found GTest: /home/murka2006/projects/hunter/_Base/xxxxxxx/fb15dbb/cf272be/Install/lib/cmake/GTest/GTestConfig.cmake (found version "1.15.2")
-- Configuring done (22.6s)
-- Generating done (0.0s)
-- Build files have been written to: /home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/_builds/default
Execute command: [
  `cmake`
  `--build`
  `/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/_builds/default`
  `--`
]

[/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07]> "cmake" "--build" "/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/_builds/default" "--"

[ 25%] Building CXX object CMakeFiles/print.dir/sources/print.cpp.o
[ 50%] Linking CXX static library libprint.a
[ 50%] Built target print
[ 75%] Building CXX object CMakeFiles/demo.dir/demo/main.cpp.o
[100%] Linking CXX executable demo
[100%] Built target demo
Run tests
Execute command: [
  `ctest`
]

[/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/_builds/default]> "ctest"

*********************************
No test configuration file found!
*********************************
Usage

  ctest [options]

-
Log saved: /home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/_logs/polly/default/log.txt
-
Generate: 0:00:23.584490s
Build: 0:00:01.449737s
Test: 0:00:00.021909s
-
Total: 0:00:25.056490s
-
SUCCESS
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ tools/polly/bin/polly.py --install
Python version: 3.12
Build dir: /home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/_builds/default
Execute command: [
  `which`
  `cmake`
]

[/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07]> "which" "cmake"

/usr/bin/cmake
Execute command: [
  `cmake`
  `--version`
]

[/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07]> "cmake" "--version"

cmake version 3.28.3

CMake suite maintained and supported by Kitware (kitware.com/cmake).

== WARNING ==

Looks like cmake arguments changed. You have two options to fix it:
  * Remove build directory completely by adding '--clear' (works 100%)
  * Run configure again by adding '--reconfig' (you must understand how CMake cache variables works/updated)

- "cmake" "-H." "-B/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/_builds/default" "-DCMAKE_TOOLCHAIN_FILE=/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/tools/polly/default.cmake"
+ "cmake" "-H." "-B/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/_builds/default" "-DCMAKE_TOOLCHAIN_FILE=/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/tools/polly/default.cmake" "-DCMAKE_INSTALL_PREFIX=/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/_install/default"
?                                                                                                                                                                                                   +++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ tools/polly/bin/polly.py --toolchain clang-cxx14
Python version: 3.12
Build dir: /home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/_builds/clang-cxx14
Execute command: [
  `which`
  `cmake`
]

[/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07]> "which" "cmake"

/usr/bin/cmake
Execute command: [
  `cmake`
  `--version`
]

[/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07]> "cmake" "--version"

cmake version 3.28.3

CMake suite maintained and supported by Kitware (kitware.com/cmake).
Execute command: [
  `cmake`
  `-H.`
  `-B/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/_builds/clang-cxx14`
  `-GUnix Makefiles`
  `-DCMAKE_TOOLCHAIN_FILE=/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/tools/polly/clang-cxx14.cmake`
]

[/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07]> "cmake" "-H." "-B/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/_builds/clang-cxx14" "-GUnix Makefiles" "-DCMAKE_TOOLCHAIN_FILE=/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/tools/polly/clang-cxx14.cmake"

CMake Deprecation Warning at CMakeLists.txt:1 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


-- [polly] Used toolchain: clang / c++14 support

clang not found

CMake Error at tools/polly/utilities/polly_fatal_error.cmake:10 (message):
Call Stack (most recent call first):
  tools/polly/compiler/clang.cmake:23 (polly_fatal_error)
  tools/polly/clang-cxx14.cmake:20 (include)
  /usr/share/cmake-3.28/Modules/CMakeDetermineSystem.cmake:170 (include)
  CMakeLists.txt:15 (project)


CMake Error: CMake was unable to find a build program corresponding to "Unix Makefiles".  CMAKE_MAKE_PROGRAM is not set.  You probably need to select a different build tool.
-- Configuring incomplete, errors occurred!
Command exit with status "1": [/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07]> "cmake" "-H." "-B/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/_builds/clang-cxx14" "-GUnix Makefiles" "-DCMAKE_TOOLCHAIN_FILE=/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/tools/polly/clang-cxx14.cmake"

Log: /home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/_logs/polly/clang-cxx14/log.txt
*** FAILED ***

murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ sudo apt-get update
[sudo] пароль для murka2006: 
Сущ:1 http://ru.archive.ubuntu.com/ubuntu noble InRelease
Пол:2 http://ru.archive.ubuntu.com/ubuntu noble-updates InRelease [126 kB]     
Пол:3 http://ru.archive.ubuntu.com/ubuntu noble-backports InRelease [126 kB]   
Пол:4 http://security.ubuntu.com/ubuntu noble-security InRelease [126 kB]      
Пол:5 https://repo.yandex.ru/yandex-browser/deb beta InRelease [4 333 B]       
Ошб:6 https://repo.yandex.ru/yandex-browser/deb beta/main amd64 Packages       
  404  Not Found [IP: 213.180.204.183 443]
Пол:6 https://repo.yandex.ru/yandex-browser/deb beta/main amd64 Packages [889 B]
Пол:7 https://packages.microsoft.com/repos/vscode stable InRelease [3 594 B]   
Пол:8 https://packages.microsoft.com/repos/code stable InRelease [3 590 B]     
Пол:9 http://ru.archive.ubuntu.com/ubuntu noble-updates/main i386 Packages [461 kB]
Пол:10 http://ru.archive.ubuntu.com/ubuntu noble-updates/main amd64 Packages [1 056 kB]
Пол:11 https://packages.microsoft.com/repos/vscode stable/main amd64 Packages [26,9 kB]
Пол:12 http://ru.archive.ubuntu.com/ubuntu noble-updates/main Translation-en [227 kB]
Пол:13 https://packages.microsoft.com/repos/code stable/main amd64 Packages [19,2 kB]
Пол:14 http://ru.archive.ubuntu.com/ubuntu noble-updates/main amd64 Components [161 kB]
Пол:15 http://ru.archive.ubuntu.com/ubuntu noble-updates/main Icons (48x48) [34,7 kB]
Пол:16 https://packages.microsoft.com/repos/code stable/main arm64 Packages [19,4 kB]
Пол:17 http://ru.archive.ubuntu.com/ubuntu noble-updates/main Icons (64x64) [49,6 kB]
Пол:18 http://ru.archive.ubuntu.com/ubuntu noble-updates/restricted i386 Packages [17,8 kB]
Пол:19 http://ru.archive.ubuntu.com/ubuntu noble-updates/restricted amd64 Packages [1 062 kB]
Пол:20 https://packages.microsoft.com/repos/code stable/main armhf Packages [19,5 kB]
Пол:21 http://ru.archive.ubuntu.com/ubuntu noble-updates/restricted Translation-en [220 kB]
Пол:22 http://ru.archive.ubuntu.com/ubuntu noble-updates/restricted amd64 Components [212 B]
Пол:23 http://ru.archive.ubuntu.com/ubuntu noble-updates/universe amd64 Packages [1 060 kB]
Пол:24 http://security.ubuntu.com/ubuntu noble-security/main i386 Packages [270 kB]
Пол:25 http://ru.archive.ubuntu.com/ubuntu noble-updates/universe i386 Packages [640 kB]
Пол:26 http://ru.archive.ubuntu.com/ubuntu noble-updates/universe Translation-en [268 kB]
Пол:27 http://ru.archive.ubuntu.com/ubuntu noble-updates/universe amd64 Components [376 kB]
Пол:28 http://ru.archive.ubuntu.com/ubuntu noble-updates/universe Icons (48x48) [226 kB]
Пол:29 http://ru.archive.ubuntu.com/ubuntu noble-updates/universe Icons (64x64) [350 kB]
Пол:30 http://ru.archive.ubuntu.com/ubuntu noble-updates/multiverse amd64 Packages [21,7 kB]
Пол:31 http://ru.archive.ubuntu.com/ubuntu noble-updates/multiverse i386 Packages [3 800 B]
Пол:32 http://ru.archive.ubuntu.com/ubuntu noble-updates/multiverse amd64 Components [940 B]
Пол:33 http://ru.archive.ubuntu.com/ubuntu noble-backports/main amd64 Components [7 084 B]
Пол:34 http://ru.archive.ubuntu.com/ubuntu noble-backports/restricted amd64 Components [216 B]
Пол:35 http://ru.archive.ubuntu.com/ubuntu noble-backports/universe amd64 Components [16,4 kB]
Пол:36 http://ru.archive.ubuntu.com/ubuntu noble-backports/universe Icons (48x48) [20,4 kB]
Пол:37 http://ru.archive.ubuntu.com/ubuntu noble-backports/universe Icons (64x64) [28,7 kB]
Пол:38 http://security.ubuntu.com/ubuntu noble-security/main amd64 Packages [782 kB]
Пол:39 http://ru.archive.ubuntu.com/ubuntu noble-backports/multiverse amd64 Components [212 B]
Пол:40 http://security.ubuntu.com/ubuntu noble-security/main Translation-en [147 kB]
Пол:41 http://security.ubuntu.com/ubuntu noble-security/main amd64 Components [21,6 kB]
Пол:42 http://security.ubuntu.com/ubuntu noble-security/main Icons (48x48) [13,4 kB]
Пол:43 http://security.ubuntu.com/ubuntu noble-security/main Icons (64x64) [20,0 kB]
Пол:44 http://security.ubuntu.com/ubuntu noble-security/restricted amd64 Packages [931 kB]
Пол:45 http://security.ubuntu.com/ubuntu noble-security/restricted Translation-en [191 kB]
Пол:46 http://security.ubuntu.com/ubuntu noble-security/restricted amd64 Components [212 B]
Пол:47 http://security.ubuntu.com/ubuntu noble-security/universe amd64 Packages [833 kB]
Пол:48 http://security.ubuntu.com/ubuntu noble-security/universe i386 Packages [515 kB]
Пол:49 http://security.ubuntu.com/ubuntu noble-security/universe Translation-en [181 kB]
Пол:50 http://security.ubuntu.com/ubuntu noble-security/universe amd64 Components [52,2 kB]
Пол:51 http://security.ubuntu.com/ubuntu noble-security/multiverse amd64 Components [212 B]
Получено 10,7 MB за 3с (3 595 kB/s) 
Чтение списков пакетов… Готово
N: Пропускается получение настроенного файла «main/binary-i386/Packages», так как репозиторий «https://packages.microsoft.com/repos/vscode stable InRelease» не поддерживает архитектуру «i386»
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ sudo apt-get install -y clang make
Чтение списков пакетов… Готово
Построение дерева зависимостей… Готово
Чтение информации о состоянии… Готово         
Уже установлен пакет make самой новой версии (4.3-4.1build2).
make помечен как установленный вручную.
Следующий пакет устанавливался автоматически и больше не требуется:
  libllvm17t64
Для его удаления используйте «sudo apt autoremove».
Будут установлены следующие дополнительные пакеты:
  clang-18 lib32gcc-s1 lib32stdc++6 libc6-i386 libclang-common-18-dev
  libclang-rt-18-dev libffi-dev libgc1 libncurses-dev libobjc-13-dev libobjc4
  libpfm4 libz3-4 libz3-dev llvm-18 llvm-18-dev llvm-18-linker-tools
  llvm-18-runtime llvm-18-tools
Предлагаемые пакеты:
  clang-18-doc wasi-libc ncurses-doc llvm-18-doc
Следующие НОВЫЕ пакеты будут установлены:
  clang clang-18 lib32gcc-s1 lib32stdc++6 libc6-i386 libclang-common-18-dev
  libclang-rt-18-dev libffi-dev libgc1 libncurses-dev libobjc-13-dev libobjc4
  libpfm4 libz3-4 libz3-dev llvm-18 llvm-18-dev llvm-18-linker-tools
  llvm-18-runtime llvm-18-tools
Обновлено 0 пакетов, установлено 20 новых пакетов, для удаления отмечено 0 пакетов, и 257 пакетов не обновлено.
Необходимо скачать 88,2 MB архивов.
После данной операции объём занятого дискового пространства возрастёт на 564 MB.
Пол:1 http://ru.archive.ubuntu.com/ubuntu noble/main amd64 libgc1 amd64 1:8.2.6-1build1 [90,3 kB]
Пол:2 http://ru.archive.ubuntu.com/ubuntu noble-updates/universe amd64 libobjc4 amd64 14.2.0-4ubuntu2~24.04 [47,0 kB]
Пол:3 http://ru.archive.ubuntu.com/ubuntu noble-updates/universe amd64 libobjc-13-dev amd64 13.3.0-6ubuntu2~24.04 [194 kB]
Пол:4 http://ru.archive.ubuntu.com/ubuntu noble-updates/universe amd64 libclang-common-18-dev amd64 1:18.1.3-1ubuntu1 [736 kB]
Пол:5 http://ru.archive.ubuntu.com/ubuntu noble-updates/universe amd64 llvm-18-linker-tools amd64 1:18.1.3-1ubuntu1 [1 314 kB]
Пол:6 http://ru.archive.ubuntu.com/ubuntu noble-updates/universe amd64 clang-18 amd64 1:18.1.3-1ubuntu1 [80,0 kB]
Пол:7 http://ru.archive.ubuntu.com/ubuntu noble/universe amd64 clang amd64 1:18.0-59~exp2 [5 846 B]
Пол:8 http://ru.archive.ubuntu.com/ubuntu noble-updates/main amd64 libc6-i386 amd64 2.39-0ubuntu8.4 [2 787 kB]
Пол:9 http://ru.archive.ubuntu.com/ubuntu noble-updates/main amd64 lib32gcc-s1 amd64 14.2.0-4ubuntu2~24.04 [92,3 kB]
Пол:10 http://ru.archive.ubuntu.com/ubuntu noble-updates/main amd64 lib32stdc++6 amd64 14.2.0-4ubuntu2~24.04 [814 kB]
Пол:11 http://ru.archive.ubuntu.com/ubuntu noble-updates/universe amd64 libclang-rt-18-dev amd64 1:18.1.3-1ubuntu1 [3 772 kB]
Пол:12 http://ru.archive.ubuntu.com/ubuntu noble/main amd64 libncurses-dev amd64 6.4+20240113-1ubuntu2 [384 kB]
Пол:13 http://ru.archive.ubuntu.com/ubuntu noble-updates/universe amd64 llvm-18-runtime amd64 1:18.1.3-1ubuntu1 [538 kB]
Пол:14 http://ru.archive.ubuntu.com/ubuntu noble/universe amd64 libpfm4 amd64 4.13.0+git32-g0d4ed0e-1 [414 kB]
Пол:15 http://ru.archive.ubuntu.com/ubuntu noble-updates/universe amd64 llvm-18 amd64 1:18.1.3-1ubuntu1 [25,3 MB]
Пол:16 http://ru.archive.ubuntu.com/ubuntu noble/main amd64 libffi-dev amd64 3.4.6-1build1 [62,8 kB]
Пол:17 http://ru.archive.ubuntu.com/ubuntu noble-updates/universe amd64 llvm-18-tools amd64 1:18.1.3-1ubuntu1 [534 kB]
Пол:18 http://ru.archive.ubuntu.com/ubuntu noble/universe amd64 libz3-4 amd64 4.8.12-3.1build1 [5 836 kB]
Пол:19 http://ru.archive.ubuntu.com/ubuntu noble/universe amd64 libz3-dev amd64 4.8.12-3.1build1 [72,2 kB]
Пол:20 http://ru.archive.ubuntu.com/ubuntu noble-updates/universe amd64 llvm-18-dev amd64 1:18.1.3-1ubuntu1 [45,1 MB]
Получено 88,2 MB за 26с (3 343 kB/s)                                           
Выбор ранее не выбранного пакета libgc1:amd64.
(Чтение базы данных … на данный момент установлено 246013 файлов и каталогов.)
Подготовка к распаковке …/00-libgc1_1%3a8.2.6-1build1_amd64.deb …
Распаковывается libgc1:amd64 (1:8.2.6-1build1) …
Выбор ранее не выбранного пакета libobjc4:amd64.
Подготовка к распаковке …/01-libobjc4_14.2.0-4ubuntu2~24.04_amd64.deb …
Распаковывается libobjc4:amd64 (14.2.0-4ubuntu2~24.04) …
Выбор ранее не выбранного пакета libobjc-13-dev:amd64.
Подготовка к распаковке …/02-libobjc-13-dev_13.3.0-6ubuntu2~24.04_amd64.deb …
Распаковывается libobjc-13-dev:amd64 (13.3.0-6ubuntu2~24.04) …
Выбор ранее не выбранного пакета libclang-common-18-dev:amd64.
Подготовка к распаковке …/03-libclang-common-18-dev_1%3a18.1.3-1ubuntu1_amd64.deb …
Распаковывается libclang-common-18-dev:amd64 (1:18.1.3-1ubuntu1) …
Выбор ранее не выбранного пакета llvm-18-linker-tools.
Подготовка к распаковке …/04-llvm-18-linker-tools_1%3a18.1.3-1ubuntu1_amd64.deb …
Распаковывается llvm-18-linker-tools (1:18.1.3-1ubuntu1) …
Выбор ранее не выбранного пакета clang-18.
Подготовка к распаковке …/05-clang-18_1%3a18.1.3-1ubuntu1_amd64.deb …
Распаковывается clang-18 (1:18.1.3-1ubuntu1) …
Выбор ранее не выбранного пакета clang.
Подготовка к распаковке …/06-clang_1%3a18.0-59~exp2_amd64.deb …
Распаковывается clang (1:18.0-59~exp2) …
Выбор ранее не выбранного пакета libc6-i386.
Подготовка к распаковке …/07-libc6-i386_2.39-0ubuntu8.4_amd64.deb …
Распаковывается libc6-i386 (2.39-0ubuntu8.4) …
Выбор ранее не выбранного пакета lib32gcc-s1.
Подготовка к распаковке …/08-lib32gcc-s1_14.2.0-4ubuntu2~24.04_amd64.deb …
Распаковывается lib32gcc-s1 (14.2.0-4ubuntu2~24.04) …
Выбор ранее не выбранного пакета lib32stdc++6.
Подготовка к распаковке …/09-lib32stdc++6_14.2.0-4ubuntu2~24.04_amd64.deb …
Распаковывается lib32stdc++6 (14.2.0-4ubuntu2~24.04) …
Выбор ранее не выбранного пакета libclang-rt-18-dev:amd64.
Подготовка к распаковке …/10-libclang-rt-18-dev_1%3a18.1.3-1ubuntu1_amd64.deb …
Распаковывается libclang-rt-18-dev:amd64 (1:18.1.3-1ubuntu1) …
Выбор ранее не выбранного пакета libncurses-dev:amd64.
Подготовка к распаковке …/11-libncurses-dev_6.4+20240113-1ubuntu2_amd64.deb …
Распаковывается libncurses-dev:amd64 (6.4+20240113-1ubuntu2) …
Выбор ранее не выбранного пакета llvm-18-runtime.
Подготовка к распаковке …/12-llvm-18-runtime_1%3a18.1.3-1ubuntu1_amd64.deb …
Распаковывается llvm-18-runtime (1:18.1.3-1ubuntu1) …
Выбор ранее не выбранного пакета libpfm4:amd64.
Подготовка к распаковке …/13-libpfm4_4.13.0+git32-g0d4ed0e-1_amd64.deb …
Распаковывается libpfm4:amd64 (4.13.0+git32-g0d4ed0e-1) …
Выбор ранее не выбранного пакета llvm-18.
Подготовка к распаковке …/14-llvm-18_1%3a18.1.3-1ubuntu1_amd64.deb …
Распаковывается llvm-18 (1:18.1.3-1ubuntu1) …
Выбор ранее не выбранного пакета libffi-dev:amd64.
Подготовка к распаковке …/15-libffi-dev_3.4.6-1build1_amd64.deb …
Распаковывается libffi-dev:amd64 (3.4.6-1build1) …
Выбор ранее не выбранного пакета llvm-18-tools.
Подготовка к распаковке …/16-llvm-18-tools_1%3a18.1.3-1ubuntu1_amd64.deb …
Распаковывается llvm-18-tools (1:18.1.3-1ubuntu1) …
Выбор ранее не выбранного пакета libz3-4:amd64.
Подготовка к распаковке …/17-libz3-4_4.8.12-3.1build1_amd64.deb …
Распаковывается libz3-4:amd64 (4.8.12-3.1build1) …
Выбор ранее не выбранного пакета libz3-dev:amd64.
Подготовка к распаковке …/18-libz3-dev_4.8.12-3.1build1_amd64.deb …
Распаковывается libz3-dev:amd64 (4.8.12-3.1build1) …
Выбор ранее не выбранного пакета llvm-18-dev.
Подготовка к распаковке …/19-llvm-18-dev_1%3a18.1.3-1ubuntu1_amd64.deb …
Распаковывается llvm-18-dev (1:18.1.3-1ubuntu1) …
Настраивается пакет libncurses-dev:amd64 (6.4+20240113-1ubuntu2) …
Настраивается пакет llvm-18-tools (1:18.1.3-1ubuntu1) …
Настраивается пакет libffi-dev:amd64 (3.4.6-1build1) …
Настраивается пакет libz3-4:amd64 (4.8.12-3.1build1) …
Настраивается пакет libpfm4:amd64 (4.13.0+git32-g0d4ed0e-1) …
Настраивается пакет libclang-common-18-dev:amd64 (1:18.1.3-1ubuntu1) …
Настраивается пакет libgc1:amd64 (1:8.2.6-1build1) …
Настраивается пакет llvm-18-linker-tools (1:18.1.3-1ubuntu1) …
Настраивается пакет libc6-i386 (2.39-0ubuntu8.4) …
Настраивается пакет llvm-18-runtime (1:18.1.3-1ubuntu1) …
Настраивается пакет libz3-dev:amd64 (4.8.12-3.1build1) …
Настраивается пакет libobjc4:amd64 (14.2.0-4ubuntu2~24.04) …
Настраивается пакет lib32gcc-s1 (14.2.0-4ubuntu2~24.04) …
Настраивается пакет lib32stdc++6 (14.2.0-4ubuntu2~24.04) …
Настраивается пакет llvm-18 (1:18.1.3-1ubuntu1) …
Настраивается пакет libclang-rt-18-dev:amd64 (1:18.1.3-1ubuntu1) …
Настраивается пакет libobjc-13-dev:amd64 (13.3.0-6ubuntu2~24.04) …
Настраивается пакет llvm-18-dev (1:18.1.3-1ubuntu1) …
Настраивается пакет clang-18 (1:18.1.3-1ubuntu1) …
Настраивается пакет clang (1:18.0-59~exp2) …
Обрабатываются триггеры для libc-bin (2.39-0ubuntu8.4) …
Обрабатываются триггеры для systemd (255.4-1ubuntu8.4) …
Обрабатываются триггеры для man-db (2.12.0-4build2) …
Обрабатываются триггеры для install-info (7.1-3build2) …
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ clang --version
Ubuntu clang version 18.1.3 (1ubuntu1)
Target: x86_64-pc-linux-gnu
Thread model: posix
InstalledDir: /usr/bin
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ make --version
GNU Make 4.3
Эта программа собрана для x86_64-pc-linux-gnu
Copyright (C) 1988-2020 Free Software Foundation, Inc.
Лицензия GPLv3+: GNU GPL версии 3 или новее <http://gnu.org/licenses/gpl.html>
Это свободное программное обеспечение: вы можете свободно изменять его и
распространять. НЕТ НИКАКИХ ГАРАНТИЙ вне пределов, допустимых законом.

murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab07$ tools/polly/bin/polly.py --toolchain clang-cxx14
Python version: 3.12
Build dir: /home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/_builds/clang-cxx14
Execute command: [
  `which`
  `cmake`
]

[/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07]> "which" "cmake"

/usr/bin/cmake
Execute command: [
  `cmake`
  `--version`
]

[/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07]> "cmake" "--version"

cmake version 3.28.3

CMake suite maintained and supported by Kitware (kitware.com/cmake).
Execute command: [
  `cmake`
  `-H.`
  `-B/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/_builds/clang-cxx14`
  `-GUnix Makefiles`
  `-DCMAKE_TOOLCHAIN_FILE=/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/tools/polly/clang-cxx14.cmake`
]

[/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07]> "cmake" "-H." "-B/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/_builds/clang-cxx14" "-GUnix Makefiles" "-DCMAKE_TOOLCHAIN_FILE=/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/tools/polly/clang-cxx14.cmake"

CMake Deprecation Warning at CMakeLists.txt:1 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


-- [polly] Used toolchain: clang / c++14 support
-- The C compiler identification is Clang 18.1.3
-- The CXX compiler identification is Clang 18.1.3
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Check for working C compiler: /usr/bin/clang - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Check for working CXX compiler: /usr/bin/clang++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- [hunter] Calculating Toolchain-SHA1
-- [hunter] Calculating Config-SHA1
-- [hunter] HUNTER_ROOT: /home/murka2006/projects/hunter
-- [hunter] [ Hunter-ID: xxxxxxx | Toolchain-ID: 71bad34 | Config-ID: cf272be ]
-- [hunter] GTEST_ROOT: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Install (ver.: 1.15.2)
-- [hunter] Building GTest
loading initial cache file /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/cache.cmake
loading initial cache file /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/args.cmake
-- [polly] Used toolchain: clang / c++14 support
-- The C compiler identification is Clang 18.1.3
-- The CXX compiler identification is Clang 18.1.3
-- Check for working C compiler: /usr/bin/clang - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /usr/bin/clang++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Configuring done (0.2s)
-- Generating done (0.0s)
-- Build files have been written to: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Build
[  6%] Creating directories for 'GTest-Release'
[ 12%] Performing download step (download, verify and extract) for 'GTest-Release'
-- verifying file...
       file='/home/murka2006/projects/hunter/_Base/Download/GTest/1.15.2/568d58e/v1.15.2.tar.gz'
-- File already exists and hash match (skip download):
  file='/home/murka2006/projects/hunter/_Base/Download/GTest/1.15.2/568d58e/v1.15.2.tar.gz'
  SHA1='568d58e26bd4e838449ca7ab8ebc152b3cbd210d'
-- extracting...
     src='/home/murka2006/projects/hunter/_Base/Download/GTest/1.15.2/568d58e/v1.15.2.tar.gz'
     dst='/home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Source'
-- extracting... [tar xfz]
-- extracting... [analysis]
-- extracting... [rename]
-- extracting... [clean up]
-- extracting... done
[ 18%] No update step for 'GTest-Release'
[ 25%] No patch step for 'GTest-Release'
[ 31%] Performing configure step for 'GTest-Release'
loading initial cache file /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/cache.cmake
loading initial cache file /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/args.cmake
-- [polly] Used toolchain: clang / c++14 support
-- The C compiler identification is Clang 18.1.3
-- The CXX compiler identification is Clang 18.1.3
-- Check for working C compiler: /usr/bin/clang - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /usr/bin/clang++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD - Success
-- Found Threads: TRUE
-- Configuring done (0.3s)
-- Generating done (0.0s)
-- Build files have been written to: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Build/GTest-Release-prefix/src/GTest-Release-build
[ 37%] Performing build step for 'GTest-Release'
[ 12%] Building CXX object googletest/CMakeFiles/gtest.dir/src/gtest-all.cc.o
[ 25%] Linking CXX static library ../lib/libgtest.a
[ 25%] Built target gtest
[ 50%] Building CXX object googlemock/CMakeFiles/gmock.dir/src/gmock-all.cc.o
[ 50%] Building CXX object googletest/CMakeFiles/gtest_main.dir/src/gtest_main.cc.o
[ 62%] Linking CXX static library ../lib/libgtest_main.a
[ 62%] Built target gtest_main
[ 75%] Linking CXX static library ../lib/libgmock.a
[ 75%] Built target gmock
[ 87%] Building CXX object googlemock/CMakeFiles/gmock_main.dir/src/gmock_main.cc.o
[100%] Linking CXX static library ../lib/libgmock_main.a
[100%] Built target gmock_main
[ 43%] Performing install step for 'GTest-Release'
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/internal
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/internal/custom
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/internal/custom/gmock-generated-actions.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/internal/custom/gmock-matchers.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/internal/custom/README.md
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/internal/custom/gmock-port.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/internal/gmock-port.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/internal/gmock-internal-utils.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/internal/gmock-pp.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/gmock-actions.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/gmock-more-matchers.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/gmock-function-mocker.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/gmock-spec-builders.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/gmock.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/gmock-matchers.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/gmock-nice-strict.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/gmock-cardinalities.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/gmock-more-actions.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/lib/libgmock.a
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/lib/libgmock_main.a
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/lib/pkgconfig/gmock.pc
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/lib/pkgconfig/gmock_main.pc
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/lib/cmake/GTest/GTestTargets.cmake
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/lib/cmake/GTest/GTestTargets-release.cmake
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/lib/cmake/GTest/GTestConfigVersion.cmake
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/lib/cmake/GTest/GTestConfig.cmake
-- Up-to-date: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/gtest-message.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/gtest-spi.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/gtest.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/internal
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/internal/gtest-port.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/internal/gtest-death-test-internal.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/internal/gtest-param-util.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/internal/gtest-port-arch.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/internal/gtest-type-util.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/internal/custom
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/internal/custom/gtest.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/internal/custom/gtest-port.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/internal/custom/gtest-printers.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/internal/custom/README.md
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/internal/gtest-internal.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/internal/gtest-string.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/internal/gtest-filepath.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/gtest-printers.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/gtest-assertion-result.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/gtest-param-test.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/gtest_prod.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/gtest_pred_impl.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/gtest-typed-test.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/gtest-death-test.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/gtest-matchers.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/gtest-test-part.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/lib/libgtest.a
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/lib/libgtest_main.a
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/lib/pkgconfig/gtest.pc
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/lib/pkgconfig/gtest_main.pc
loading initial cache file /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/args.cmake
[ 50%] Completed 'GTest-Release'
[ 50%] Built target GTest-Release
[ 56%] Creating directories for 'GTest-Debug'
[ 62%] Performing download step (download, verify and extract) for 'GTest-Debug'
-- verifying file...
       file='/home/murka2006/projects/hunter/_Base/Download/GTest/1.15.2/568d58e/v1.15.2.tar.gz'
-- File already exists and hash match (skip download):
  file='/home/murka2006/projects/hunter/_Base/Download/GTest/1.15.2/568d58e/v1.15.2.tar.gz'
  SHA1='568d58e26bd4e838449ca7ab8ebc152b3cbd210d'
-- extracting...
     src='/home/murka2006/projects/hunter/_Base/Download/GTest/1.15.2/568d58e/v1.15.2.tar.gz'
     dst='/home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Source'
-- extracting... [tar xfz]
-- extracting... [analysis]
-- extracting... [rename]
-- extracting... [clean up]
-- extracting... done
[ 68%] No update step for 'GTest-Debug'
[ 75%] No patch step for 'GTest-Debug'
[ 81%] Performing configure step for 'GTest-Debug'
loading initial cache file /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/cache.cmake
loading initial cache file /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/args.cmake
-- [polly] Used toolchain: clang / c++14 support
-- The C compiler identification is Clang 18.1.3
-- The CXX compiler identification is Clang 18.1.3
-- Check for working C compiler: /usr/bin/clang - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /usr/bin/clang++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD - Success
-- Found Threads: TRUE
-- Configuring done (0.3s)
-- Generating done (0.0s)
-- Build files have been written to: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Build/GTest-Debug-prefix/src/GTest-Debug-build
[ 87%] Performing build step for 'GTest-Debug'
[ 12%] Building CXX object googletest/CMakeFiles/gtest.dir/src/gtest-all.cc.o
[ 25%] Linking CXX static library ../lib/libgtestd.a
[ 25%] Built target gtest
[ 50%] Building CXX object googletest/CMakeFiles/gtest_main.dir/src/gtest_main.cc.o
[ 50%] Building CXX object googlemock/CMakeFiles/gmock.dir/src/gmock-all.cc.o
[ 62%] Linking CXX static library ../lib/libgtest_maind.a
[ 62%] Built target gtest_main
[ 75%] Linking CXX static library ../lib/libgmockd.a
[ 75%] Built target gmock
[ 87%] Building CXX object googlemock/CMakeFiles/gmock_main.dir/src/gmock_main.cc.o
[100%] Linking CXX static library ../lib/libgmock_maind.a
[100%] Built target gmock_main
[ 93%] Performing install step for 'GTest-Debug'
-- Up-to-date: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include
-- Up-to-date: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock
-- Up-to-date: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/internal
-- Up-to-date: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/internal/custom
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/internal/custom/gmock-generated-actions.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/internal/custom/gmock-matchers.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/internal/custom/README.md
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/internal/custom/gmock-port.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/internal/gmock-port.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/internal/gmock-internal-utils.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/internal/gmock-pp.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/gmock-actions.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/gmock-more-matchers.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/gmock-function-mocker.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/gmock-spec-builders.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/gmock.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/gmock-matchers.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/gmock-nice-strict.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/gmock-cardinalities.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gmock/gmock-more-actions.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/lib/libgmockd.a
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/lib/libgmock_maind.a
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/lib/pkgconfig/gmock.pc
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/lib/pkgconfig/gmock_main.pc
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/lib/cmake/GTest/GTestTargets.cmake
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/lib/cmake/GTest/GTestTargets-debug.cmake
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/lib/cmake/GTest/GTestConfigVersion.cmake
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/lib/cmake/GTest/GTestConfig.cmake
-- Up-to-date: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include
-- Up-to-date: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/gtest-message.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/gtest-spi.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/gtest.h
-- Up-to-date: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/internal
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/internal/gtest-port.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/internal/gtest-death-test-internal.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/internal/gtest-param-util.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/internal/gtest-port-arch.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/internal/gtest-type-util.h
-- Up-to-date: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/internal/custom
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/internal/custom/gtest.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/internal/custom/gtest-port.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/internal/custom/gtest-printers.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/internal/custom/README.md
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/internal/gtest-internal.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/internal/gtest-string.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/internal/gtest-filepath.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/gtest-printers.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/gtest-assertion-result.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/gtest-param-test.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/gtest_prod.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/gtest_pred_impl.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/gtest-typed-test.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/gtest-death-test.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/gtest-matchers.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/include/gtest/gtest-test-part.h
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/lib/libgtestd.a
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/lib/libgtest_maind.a
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/lib/pkgconfig/gtest.pc
-- Installing: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/Install/lib/pkgconfig/gtest_main.pc
loading initial cache file /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest/args.cmake
[100%] Completed 'GTest-Debug'
[100%] Built target GTest-Debug
-- [hunter] Build step successful (dir: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Build/GTest)
-- [hunter] Cache saved: /home/murka2006/projects/hunter/_Base/Cache/raw/096fcd72e8c391a64ae3b565aaa022a1534d7cfb.tar.bz2
-- Found GTest: /home/murka2006/projects/hunter/_Base/xxxxxxx/71bad34/cf272be/Install/lib/cmake/GTest/GTestConfig.cmake (found version "1.15.2")
-- Configuring done (53.9s)
-- Generating done (0.0s)
-- Build files have been written to: /home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/_builds/clang-cxx14
Execute command: [
  `cmake`
  `--build`
  `/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/_builds/clang-cxx14`
  `--`
]

[/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07]> "cmake" "--build" "/home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/_builds/clang-cxx14" "--"

[ 25%] Building CXX object CMakeFiles/print.dir/sources/print.cpp.o
[ 50%] Linking CXX static library libprint.a
[ 50%] Built target print
[ 75%] Building CXX object CMakeFiles/demo.dir/demo/main.cpp.o
[100%] Linking CXX executable demo
[100%] Built target demo
-
Log saved: /home/murka2006/Mari-Mur-Meow/workspace/projects/lab07/_logs/polly/clang-cxx14/log.txt
-
Generate: 0:00:54.966119s
Build: 0:00:01.562125s
-
Total: 0:00:56.528534s
-
SUCCESS
