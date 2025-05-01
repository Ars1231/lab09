murka2006@murka:~$ export GITHUB_USERNAME=Mari-Mur-Meow
murka2006@murka:~$ export GITHUB_TOKEN=
murka2006@murka:~$ cd ${GITHUB_USERNAME}/workspace
murka2006@murka:~/Mari-Mur-Meow/workspace$ pushd .
~/Mari-Mur-Meow/workspace ~/Mari-Mur-Meow/workspace
murka2006@murka:~/Mari-Mur-Meow/workspace$ source scripts/activate
murka2006@murka:~/Mari-Mur-Meow/workspace$ git clone https://github.com/${GITHUB_USERNAME}/lab03 projects/lab06
Клонирование в «projects/lab06»...
remote: Enumerating objects: 56, done.
remote: Counting objects: 100% (56/56), done.
remote: Compressing objects: 100% (29/29), done.
remote: Total 56 (delta 19), reused 52 (delta 18), pack-reused 0 (from 0)
Получение объектов: 100% (56/56), 15.59 КиБ | 149.00 КиБ/с, готово.
Определение изменений: 100% (19/19), готово.
murka2006@murka:~/Mari-Mur-Meow/workspace$ cd projects/lab06
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ git remote remove origin
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ git remote add origin https://github.com/${GITHUB_USERNAME}/lab06
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ cat > .travis.yml <<EOF
> language: cpp
> EOF
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ cat >> .travis.yml <<EOF
> script:
- cmake -H. -B_build -DCMAKE_INSTALL_PREFIX=_install
- cmake --build _build
- cmake --build _build --target install
> EOF
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ cat >> .travis.yml <<EOF
> addons:
  apt:
    sources:
      - george-edison55-precise-backports
    packages:
      - cmake
      - cmake-data
> EOF
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ ex -sc '1i|<фрагмент_вставки_значка>' -cx README.md
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ git add .travis.yml
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ git add README.md
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ git commit -m"added CI"
[master 3230758] added CI
 2 files changed, 13 insertions(+)
 create mode 100644 .travis.yml
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ git push origin master
Username for 'https://github.com': Mari-Mur-Meow
Password for 'https://Mari-Mur-Meow@github.com': 
Перечисление объектов: 60, готово.
Подсчет объектов: 100% (60/60), готово.
При сжатии изменений используется до 8 потоков
Сжатие объектов: 100% (32/32), готово.
Запись объектов: 100% (60/60), 16.04 КиБ | 8.02 МиБ/с, готово.
Всего 60 (изменений 21), повторно использовано 54 (изменений 19), повторно использовано пакетов 0
remote: Resolving deltas: 100% (21/21), done.
To https://github.com/Mari-Mur-Meow/lab06
 * [new branch]      master -> master
murka2006@murka:~$ ls
 BMSTU           tasks          Документы     непонятно
 Mari-Mur-Meow  'visual code'   Загрузки      Общедоступные
 reports         бандит         Изображения  'Рабочий стол'
 snap            Видео          Музыка        Шаблоны
murka2006@murka:~$ cd Mari-Mur-Meow
murka2006@murka:~/Mari-Mur-Meow$ ls
workspace
murka2006@murka:~/Mari-Mur-Meow$ cd.
Команда «cd.» не найдена. Возможно, вы имели в виду:
  команда 'cdp' из deb-пакета irpas (0.10-9)
  команда 'cdw' из deb-пакета cdw (0.8.1-3)
  команда 'cdi' из deb-пакета cdo (2.3.0-1)
  команда 'cdb' из deb-пакета tinycdb (0.81-1)
  команда 'cde' из deb-пакета cde (0.1+git9-g551e54d-1.2)
  команда 'cd5' из deb-пакета cd5 (0.1-4)
  команда 'cdo' из deb-пакета cdo (2.3.0-1)
Попробуйте: sudo apt install <имя_deb-пакета>
murka2006@murka:~/Mari-Mur-Meow$ cd workspace
murka2006@murka:~/Mari-Mur-Meow/workspace$ ls
LICENSE  node  projects  README.md  reports  scripts  tasks
murka2006@murka:~/Mari-Mur-Meow/workspace$ cd projects
murka2006@murka:~/Mari-Mur-Meow/workspace/projects$ ls
AL-Labs-IY8-25  lab_02  lab02  lab03  lab04  lab06
murka2006@murka:~/Mari-Mur-Meow/workspace/projects$ -rm lab06
Команда «-rm» не найдена. Возможно, вы имели в виду:
  команда 'rm' из deb-пакета coreutils (9.4-2ubuntu2)
  команда 'crm' из deb-пакета crm114 (20100106-10)
  команда 'crm' из deb-пакета crmsh (4.5.0-1ubuntu2)
  команда 'frm' из deb-пакета mailutils (1:3.16-1build1)
  команда 'vrm' из deb-пакета atfs (1.4pl6-16)
  команда 'srm' из deb-пакета secure-delete (3.1-8)
Попробуйте: sudo apt install <имя_deb-пакета>
murka2006@murka:~/Mari-Mur-Meow/workspace/projects$ rm lab06
rm: невозможно удалить 'lab06': Это каталог
murka2006@murka:~/Mari-Mur-Meow/workspace/projects$ rf rm lab06
rf: команда не найдена
murka2006@murka:~/Mari-Mur-Meow/workspace/projects$ rm -r lab06
rm: удалить защищённый от записи обычный файл 'lab06/.git/modules/third-party/gtest/objects/pack/pack-c03ec18ed561b02de00d8f6ba4b2e35a9633b3d4.rev'? 
rm: удалить защищённый от записи обычный файл 'lab06/.git/modules/third-party/gtest/objects/pack/pack-c03ec18ed561b02de00d8f6ba4b2e35a9633b3d4.idx'? Y
rm: удалить защищённый от записи обычный файл 'lab06/.git/modules/third-party/gtest/objects/pack/pack-c03ec18ed561b02de00d8f6ba4b2e35a9633b3d4.pack'? rm: невозможно удалить 'lab06/.git/modules/third-party/gtest/objects/pack': Каталог не пуст
rm: удалить защищённый от записи обычный файл 'lab06/.git/objects/8f/b7d98696ab35edf47d228d545b67a17bbb0952'? rm: невозможно удалить 'lab06/.git/objects/8f': Каталог не пуст
rm: удалить защищённый от записи обычный файл 'lab06/.git/objects/aa/d4534c581453812ba1da69486c6993ccf2c870'? rm: невозможно удалить 'lab06/.git/objects/aa': Каталог не пуст
rm: удалить защищённый от записи обычный файл 'lab06/.git/objects/5d/1621009c3fe245e640c80035fe0fa71f7228c9'? rm: невозможно удалить 'lab06/.git/objects/5d': Каталог не пуст
rm: удалить защищённый от записи обычный файл 'lab06/.git/objects/df/4c222cb24549178b8063ecbb5b1e2dcca75ee1'? rm: невозможно удалить 'lab06/.git/objects/df': Каталог не пуст
rm: удалить защищённый от записи обычный файл 'lab06/.git/objects/pack/pack-9c246e8e20035ae175124716d262c4342f9f1364.pack'? rm: удалить защищённый от записи обычный файл 'lab06/.git/objects/pack/pack-9c246e8e20035ae175124716d262c4342f9f1364.idx'? rm: удалить защищённый от записи обычный файл 'lab06/.git/objects/pack/pack-9c246e8e20035ae175124716d262c4342f9f1364.rev'? rm: невозможно удалить 'lab06/.git/objects/pack': Каталог не пуст
murka2006@murka:~/Mari-Mur-Meow/workspace/projects$ rm -rf lab06
murka2006@murka:~/Mari-Mur-Meow/workspace/projects$ ls
AL-Labs-IY8-25  lab_02  lab02  lab03  lab04
murka2006@murka:~/Mari-Mur-Meow/workspace/projects$ export GITHUB_USERNAME=Mari-Mur-Meow
murka2006@murka:~/Mari-Mur-Meow/workspace/projects$ alias gsed=sed
murka2006@murka:~/Mari-Mur-Meow/workspace/projects$ cd
murka2006@murka:~$ export GITHUB_USERNAME=Mari-Mur-Meow
murka2006@murka:~$ alias gsed=sed
murka2006@murka:~$ cd ${GITHUB_USERNAME}/workspace
murka2006@murka:~/Mari-Mur-Meow/workspace$ pushd .
~/Mari-Mur-Meow/workspace ~/Mari-Mur-Meow/workspace
murka2006@murka:~/Mari-Mur-Meow/workspace$ source scripts/activate
murka2006@murka:~/Mari-Mur-Meow/workspace$ git clone https://github.com/${GITHUB_USERNAME}/lab04 projects/lab06
Клонирование в «projects/lab06»...
remote: Enumerating objects: 63, done.
remote: Counting objects: 100% (63/63), done.
remote: Compressing objects: 100% (33/33), done.
remote: Total 63 (delta 23), reused 59 (delta 21), pack-reused 0 (from 0)
Получение объектов: 100% (63/63), 17.42 КиБ | 5.81 МиБ/с, готово.
Определение изменений: 100% (23/23), готово.
murka2006@murka:~/Mari-Mur-Meow/workspace$ cd projects/lab06
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ git remote remove origin
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ git remote add origin https://github.com/${GITHUB_USERNAME}/lab06
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ mkdir third-party
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ git submodule add https://github.com/google/googletest third-party/gtest
Клонирование в «/home/murka2006/Mari-Mur-Meow/workspace/projects/lab06/third-party/gtest»...
remote: Enumerating objects: 28036, done.
remote: Counting objects: 100% (257/257), done.
remote: Compressing objects: 100% (166/166), done.
remote: Total 28036 (delta 164), reused 92 (delta 91), pack-reused 27779 (from 4)
Получение объектов: 100% (28036/28036), 13.53 МиБ | 368.00 КиБ/с, готово.
Определение изменений: 100% (20765/20765), готово.
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ cd third-party/gtest && git checkout release-1.11.0 && cd ../..
Примечание: переключение на «release-1.11.0».

Вы сейчас в состоянии «отсоединённого указателя HEAD». Можете осмотреться,
внести экспериментальные изменения и зафиксировать их, также можете
отменить любые коммиты, созданные в этом состоянии, не затрагивая другие
ветки, переключившись обратно на любую ветку.

Если хотите создать новую ветку для сохранения созданных коммитов, можете
сделать это (сейчас или позже), используя команду switch с параметром -c.
Например:

  git switch -c <новая-ветка>

Или отмените эту операцию с помощью:

  git switch -

Отключите этот совет, установив переменную конфигурации
advice.detachedHead в значение false

HEAD сейчас на e2239ee6 Googletest export
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ git add third-party/gtest
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ git commit -m"added gtest framework"
[master 6c01ef0] added gtest framework
 2 files changed, 4 insertions(+)
 create mode 100644 .gitmodules
 create mode 160000 third-party/gtest
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ gsed -i '/option(BUILD_EXAMPLES "Build examples" OFF)/a\
option(BUILD_TESTS "Build tests" OFF)
> ' CMakeLists.txt
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ cat >> CMakeLists.txt <<EOF
> 
if(BUILD_TESTS)
  enable_testing()
  add_subdirectory(third-party/gtest)
  file(GLOB \${PROJECT_NAME}_TEST_SOURCES tests/*.cpp)
  add_executable(check \${\${PROJECT_NAME}_TEST_SOURCES})
  target_link_libraries(check \${PROJECT_NAME} gtest_main)
  add_test(NAME check COMMAND check)
endif()
> EOF
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ mkdir tests
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ cat > tests/test1.cpp <<EOF
> #include <print.hpp>

#include <gtest/gtest.h>

TEST(Print, InFileStream)
{
  std::string filepath = "file.txt";
  std::string text = "hello";
  std::ofstream out{filepath};

  print(text, out);
  out.close();

  std::string result;
  std::ifstream in{filepath};
  in >> result;

  EXPECT_EQ(result, text);
}
> EOF
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ cmake -H. -B_build -DBUILD_TESTS=ON
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
CMake Deprecation Warning at third-party/gtest/CMakeLists.txt:4 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


CMake Deprecation Warning at third-party/gtest/googlemock/CMakeLists.txt:45 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


CMake Deprecation Warning at third-party/gtest/googletest/CMakeLists.txt:56 (cmake_minimum_required):
  Compatibility with CMake < 3.5 will be removed from a future version of
  CMake.

  Update the VERSION argument <min> value or use a ...<max> suffix to tell
  CMake that the project does not need compatibility with older versions.


-- Found Python: /usr/bin/python3 (found version "3.12.3") found components: Interpreter 
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD - Success
-- Found Threads: TRUE  
-- Configuring done (1.1s)
-- Generating done (0.0s)
-- Build files have been written to: /home/murka2006/Mari-Mur-Meow/workspace/projects/lab06/_build
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ cmake --build _build
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
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ cmake --build _build --target test
Running tests...
Test project /home/murka2006/Mari-Mur-Meow/workspace/projects/lab06/_build
    Start 1: check
1/1 Test #1: check ............................   Passed    0.01 sec

100% tests passed, 0 tests failed out of 1

Total Test time (real) =   0.01 sec
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ _build/check
Running main() from /home/murka2006/Mari-Mur-Meow/workspace/projects/lab06/third-party/gtest/googletest/src/gtest_main.cc
[==========] Running 1 test from 1 test suite.
[----------] Global test environment set-up.
[----------] 1 test from Print
[ RUN      ] Print.InFileStream
[       OK ] Print.InFileStream (0 ms)
[----------] 1 test from Print (0 ms total)

[----------] Global test environment tear-down
[==========] 1 test from 1 test suite ran. (0 ms total)
[  PASSED  ] 1 test.
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ cmake --build _build --target test -- ARGS=--verbose
Running tests...
UpdateCTestConfiguration  from :/home/murka2006/Mari-Mur-Meow/workspace/projects/lab06/_build/DartConfiguration.tcl
UpdateCTestConfiguration  from :/home/murka2006/Mari-Mur-Meow/workspace/projects/lab06/_build/DartConfiguration.tcl
Test project /home/murka2006/Mari-Mur-Meow/workspace/projects/lab06/_build
Constructing a list of tests
Done constructing a list of tests
Updating test list for fixtures
Added 0 tests to meet fixture requirements
Checking test dependency graph...
Checking test dependency graph end
test 1
    Start 1: check

1: Test command: /home/murka2006/Mari-Mur-Meow/workspace/projects/lab06/_build/check
1: Working Directory: /home/murka2006/Mari-Mur-Meow/workspace/projects/lab06/_build
1: Test timeout computed to be: 10000000
1: Running main() from /home/murka2006/Mari-Mur-Meow/workspace/projects/lab06/third-party/gtest/googletest/src/gtest_main.cc
1: [==========] Running 1 test from 1 test suite.
1: [----------] Global test environment set-up.
1: [----------] 1 test from Print
1: [ RUN      ] Print.InFileStream
1: [       OK ] Print.InFileStream (0 ms)
1: [----------] 1 test from Print (0 ms total)
1: 
1: [----------] Global test environment tear-down
1: [==========] 1 test from 1 test suite ran. (0 ms total)
1: [  PASSED  ] 1 test.
1/1 Test #1: check ............................   Passed    0.00 sec

100% tests passed, 0 tests failed out of 1

Total Test time (real) =   0.01 sec
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ gsed -i 's/lab04/lab06/g' README.md
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ gsed -i 's/\(DCMAKE_INSTALL_PREFIX=_install\)/\1 -DBUILD_TESTS=ON/' .travis.yml
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ gsed -i '/cmake --build _build --target install/a\
- cmake --build _build --target test -- ARGS=--verbose
> ' .travis.yml
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ travis lint 
Команда «travis» не найдена, но может быть установлена с помощью:
sudo snap install travis  # version 1.8.9, or
sudo apt  install travis  # version 220729-1
См. 'snap info travis', чтобы посмотреть дополнительные версии.
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ git add .travis.yml
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ git add tests
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ git add -p
diff --git a/CMakeLists.txt b/CMakeLists.txt
index 96a361e..aa7a323 100644
--- a/CMakeLists.txt
+++ b/CMakeLists.txt
@@ -4,6 +4,7 @@ set(CMAKE_CXX_STANDARD 11)
 set(CMAKE_CXX_STANDARD_REQUIRED ON)
 
 option(BUILD_EXAMPLES "Build examples" OFF)
+option(BUILD_TESTS "Build tests" OFF)
 
 project(print)
 
(1/2) Индексировать этот блок [y,n,q,a,d,j,J,g,/,e,?]? y
@@ -34,3 +35,12 @@ install(TARGETS print
 
 install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/include/ DESTINATION include)
 install(EXPORT print-config DESTINATION cmake)
+
+if(BUILD_TESTS)
+  enable_testing()
+  add_subdirectory(third-party/gtest)
+  file(GLOB ${PROJECT_NAME}_TEST_SOURCES tests/*.cpp)
+  add_executable(check ${${PROJECT_NAME}_TEST_SOURCES})
+  target_link_libraries(check ${PROJECT_NAME} gtest_main)
+  add_test(NAME check COMMAND check)
+endif()
(2/2) Индексировать этот блок [y,n,q,a,d,K,g,/,e,?]? n

diff --git a/README.md b/README.md
index 3af970a..a5c5d2d 100644
--- a/README.md
+++ b/README.md
@@ -4,27 +4,27 @@ murka2006@murka:~$ cd ${GITHUB_USERNAME}/workspace
 murka2006@murka:~/Mari-Mur-Meow/workspace$ pushd .
 ~/Mari-Mur-Meow/workspace ~/Mari-Mur-Meow/workspace
 murka2006@murka:~/Mari-Mur-Meow/workspace$ source scripts/activate
-murka2006@murka:~/Mari-Mur-Meow/workspace$ git clone https://github.com/${GITHUB_USERNAME}/lab03 projects/lab04
-Клонирование в «projects/lab04»...
+murka2006@murka:~/Mari-Mur-Meow/workspace$ git clone https://github.com/${GITHUB_USERNAME}/lab03 projects/lab06
+Клонирование в «projects/lab06»...
 remote: Enumerating objects: 56, done.
 remote: Counting objects: 100% (56/56), done.
 remote: Compressing objects: 100% (29/29), done.
 remote: Total 56 (delta 19), reused 52 (delta 18), pack-reused 0 (from 0)
 Получение объектов: 100% (56/56), 15.59 КиБ | 149.00 КиБ/с, готово.
 Определение изменений: 100% (19/19), готово.
-murka2006@murka:~/Mari-Mur-Meow/workspace$ cd projects/lab04
-murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab04$ git remote remove origin
-murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab04$ git remote add origin https://github.com/${GITHUB_USERNAME}/lab04
-murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab04$ cat > .travis.yml <<EOF
+murka2006@murka:~/Mari-Mur-Meow/workspace$ cd projects/lab06
+murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ git remote remove origin
+murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ git remote add origin https://github.com/${GITHUB_USERNAME}/lab06
+murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ cat > .travis.yml <<EOF
 > language: cpp
 > EOF
-murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab04$ cat >> .travis.yml <<EOF
+murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ cat >> .travis.yml <<EOF
 > script:
 - cmake -H. -B_build -DCMAKE_INSTALL_PREFIX=_install
 - cmake --build _build
 - cmake --build _build --target install
 > EOF
-murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab04$ cat >> .travis.yml <<EOF
+murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ cat >> .travis.yml <<EOF
 > addons:
   apt:
     sources:
(1/3) Индексировать этот блок [y,n,q,a,d,j,J,g,/,s,e,?]? a

murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ git commit -m"added tests"
[master 593e103] added tests
 4 files changed, 36 insertions(+), 15 deletions(-)
 create mode 100644 tests/test1.cpp
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ git push origin master
Username for 'https://github.com': 
Password for 'https:: 
Перечисление объектов: 74, готово.
Подсчет объектов: 100% (74/74), готово.
При сжатии изменений используется до 8 потоков
Сжатие объектов: 100% (40/40), готово.
Запись объектов: 100% (74/74), 18.94 КиБ | 6.31 МиБ/с, готово.
Всего 74 (изменений 28), повторно использовано 60 (изменений 23), повторно использовано пакетов 0
remote: Resolving deltas: 100% (28/28), done.
To https://github.com/Mari-Mur-Meow/lab06
 * [new branch]      master -> master
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ mkdir artifacts
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ sleep 20s && gnome-screenshot --file artifacts/screenshot.png
Команда «gnome-screenshot» не найдена, но может быть установлена с помощью:
sudo apt install gnome-screenshot
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ ^C
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ sudo apt install gnome-screenshot
[sudo] пароль для murka2006: 
в
Попробуйте ещё раз.
[sudo] пароль для murka2006: 
Попробуйте ещё раз.
[sudo] пароль для murka2006: 
Чтение списков пакетов… Готово
Построение дерева зависимостей… Готово
Чтение информации о состоянии… Готово         
Следующий пакет устанавливался автоматически и больше не требуется:
  libllvm17t64
Для его удаления используйте «sudo apt autoremove».
Следующие НОВЫЕ пакеты будут установлены:
  gnome-screenshot
Обновлено 0 пакетов, установлено 1 новых пакетов, для удаления отмечено 0 пакетов, и 233 пакетов не обновлено.
Необходимо скачать 174 kB архивов.
После данной операции объём занятого дискового пространства возрастёт на 1 115 kB.
Пол:1 http://ru.archive.ubuntu.com/ubuntu noble/universe amd64 gnome-screenshot amd64 41.0-2build2 [174 kB]
Получено 174 kB за 0с (421 kB/s)           
Выбор ранее не выбранного пакета gnome-screenshot.
(Чтение базы данных … на данный момент установлено 245899 файлов и каталогов.)
Подготовка к распаковке …/gnome-screenshot_41.0-2build2_amd64.deb …
Распаковывается gnome-screenshot (41.0-2build2) …
Настраивается пакет gnome-screenshot (41.0-2build2) …
Обрабатываются триггеры для man-db (2.12.0-4build2) …
Обрабатываются триггеры для libglib2.0-0t64:amd64 (2.80.0-6ubuntu3.2) …
Обрабатываются триггеры для mailcap (3.70+nmu1ubuntu1) …
Обрабатываются триггеры для desktop-file-utils (0.27-2build1) …
Обрабатываются триггеры для hicolor-icon-theme (0.17-2) …
Обрабатываются триггеры для gnome-menus (3.36.0-1.1ubuntu3) …
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ sleep 20s && gnome-screenshot --file artifacts/screenshot.png
murka2006@murka:~/Mari-Mur-Meow/workspace/projects/lab06$ 
