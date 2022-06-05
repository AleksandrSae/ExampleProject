# ExampleProject
Google test example project is got from https://raymii.org/s/tutorials/Cpp_project_setup_with_cmake_and_unit_tests.html

#Also, here is the examples from https://github.com/sandordargo/parameterizedTestExamplesCpp in parametrized_test branch

#To build adn run

###$ git clone --recurse-submodules https://github.com/AleksandrSae/ExampleProject.git

Cloning into 'ExampleProject'...
remote: Enumerating objects: 203, done.
remote: Counting objects: 100% (203/203), done.
remote: Compressing objects: 100% (111/111), done.
remote: Total 203 (delta 75), reused 197 (delta 72), pack-reused 0
Receiving objects: 100% (203/203), 2.49 MiB | 4.40 MiB/s, done.
Resolving deltas: 100% (75/75), done.
Submodule 'lib/googletest' (https://github.com/google/googletest) registered for path 'lib/googletest'
Cloning into '/home/alexander/temp/test_sample/ExampleProject/lib/googletest'...
remote: Enumerating objects: 24457, done.        
remote: Counting objects: 100% (122/122), done.        
remote: Compressing objects: 100% (57/57), done.        
remote: Total 24457 (delta 63), reused 86 (delta 53), pack-reused 24335        
Receiving objects: 100% (24457/24457), 10.46 MiB | 6.36 MiB/s, done.
Resolving deltas: 100% (18075/18075), done.
Submodule path 'lib/googletest': checked out '0320f517fd920866d918e564105d68fd4362040a'


###$ cd ExampleProject/
###$ git fetch origin parametrized_test:parametrized_test

From https://github.com/AleksandrSae/ExampleProject
 * [new branch]      parametrized_test -> parametrized_test
alexander@sap-laptop:~/temp/test_sample/ExampleProject$ git switch parametrized_test
Switched to branch 'parametrized_test'


###$ mkdir build
###$ cd build/
###$ cmake ..

-- The C compiler identification is GNU 9.3.0
-- The CXX compiler identification is GNU 9.3.0
-- Check for working C compiler: /usr/bin/cc
-- Check for working C compiler: /usr/bin/cc -- works
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Detecting C compile features
-- Detecting C compile features - done
-- Check for working CXX compiler: /usr/bin/c++
-- Check for working CXX compiler: /usr/bin/c++ -- works
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Found Python: /usr/local/bin/python3.8 (found version "3.8.12") found components: Interpreter 
-- Looking for pthread.h
-- Looking for pthread.h - found
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD
-- Performing Test CMAKE_HAVE_LIBC_PTHREAD - Failed
-- Looking for pthread_create in pthreads
-- Looking for pthread_create in pthreads - not found
-- Looking for pthread_create in pthread
-- Looking for pthread_create in pthread - found
-- Found Threads: TRUE  
-- Configuring done
-- Generating done
-- Build files have been written to: /home/alexander/temp/test_sample/ExampleProject/build
alexander@sap-laptop:~/temp/test_sample/ExampleProject/build$ make
Scanning dependencies of target ExampleProject_lib
[  3%] Building CXX object src/CMakeFiles/ExampleProject_lib.dir/Formula.cpp.o
[  7%] Building CXX object src/CMakeFiles/ExampleProject_lib.dir/LeapYear.cpp.o
[ 11%] Building CXX object src/CMakeFiles/ExampleProject_lib.dir/main.cpp.o
[ 14%] Linking CXX static library libExampleProject_lib.a
[ 14%] Built target ExampleProject_lib
Scanning dependencies of target ExampleProject_run
[ 18%] Building CXX object src/CMakeFiles/ExampleProject_run.dir/Formula.cpp.o
[ 22%] Building CXX object src/CMakeFiles/ExampleProject_run.dir/LeapYear.cpp.o
[ 25%] Building CXX object src/CMakeFiles/ExampleProject_run.dir/main.cpp.o
[ 29%] Linking CXX executable ExampleProject_run
[ 29%] Built target ExampleProject_run
Scanning dependencies of target gtest
[ 33%] Building CXX object lib/googletest/googletest/CMakeFiles/gtest.dir/src/gtest-all.cc.o
[ 37%] Linking CXX static library ../../libgtest.a
[ 37%] Built target gtest
Scanning dependencies of target ExampleProject_tst
[ 40%] Building CXX object tst/CMakeFiles/ExampleProject_tst.dir/AddTypeParameterizedTests.cpp.o
[ 44%] Building CXX object tst/CMakeFiles/ExampleProject_tst.dir/AddTypishParameterizedTests.cpp.o
[ 48%] Building CXX object tst/CMakeFiles/ExampleProject_tst.dir/Formula_test.cpp.o
[ 51%] Building CXX object tst/CMakeFiles/ExampleProject_tst.dir/LeapYearFixtureCombinedWithParameterizedTests.cpp.o
[ 55%] Building CXX object tst/CMakeFiles/ExampleProject_tst.dir/LeapYearFixtureTests.cpp.o
[ 59%] Building CXX object tst/CMakeFiles/ExampleProject_tst.dir/LeapYearIterationTest.cpp.o
[ 62%] Building CXX object tst/CMakeFiles/ExampleProject_tst.dir/LeapYearMultipleParametersTests.cpp.o
[ 66%] Building CXX object tst/CMakeFiles/ExampleProject_tst.dir/LeapYearParameterizedTestFixture.cpp.o
[ 70%] Building CXX object tst/CMakeFiles/ExampleProject_tst.dir/LeapYearStandaloneTests.cpp.o
[ 74%] Building CXX object tst/CMakeFiles/ExampleProject_tst.dir/main.cpp.o
[ 77%] Linking CXX executable ExampleProject_tst
[ 77%] Built target ExampleProject_tst
Scanning dependencies of target gmock
[ 81%] Building CXX object lib/googletest/googlemock/CMakeFiles/gmock.dir/src/gmock-all.cc.o
[ 85%] Linking CXX static library ../../libgmock.a
[ 85%] Built target gmock
Scanning dependencies of target gmock_main
[ 88%] Building CXX object lib/googletest/googlemock/CMakeFiles/gmock_main.dir/src/gmock_main.cc.o
[ 92%] Linking CXX static library ../../libgmock_main.a
[ 92%] Built target gmock_main
Scanning dependencies of target gtest_main
[ 96%] Building CXX object lib/googletest/googletest/CMakeFiles/gtest_main.dir/src/gtest_main.cc.o
[100%] Linking CXX static library ../../libgtest_main.a
[100%] Built target gtest_main


###$ ./tst/ExampleProject_tst 
[==========] Running 32 tests from 12 test suites.
[----------] Global test environment set-up.
[----------] 1 test from TestPrefix/AddTypedParamTestsFixture/0, where TypeParam = int
[ RUN      ] TestPrefix/AddTypedParamTestsFixture/0.doesAdd
[       OK ] TestPrefix/AddTypedParamTestsFixture/0.doesAdd (0 ms)
[----------] 1 test from TestPrefix/AddTypedParamTestsFixture/0 (0 ms total)

[----------] 1 test from TestPrefix/AddTypedParamTestsFixture/1, where TypeParam = long long
[ RUN      ] TestPrefix/AddTypedParamTestsFixture/1.doesAdd
[       OK ] TestPrefix/AddTypedParamTestsFixture/1.doesAdd (0 ms)
[----------] 1 test from TestPrefix/AddTypedParamTestsFixture/1 (0 ms total)

[----------] 1 test from TestPrefix/AddTypedParamTestsFixture/2, where TypeParam = unsigned long
[ RUN      ] TestPrefix/AddTypedParamTestsFixture/2.doesAdd
[       OK ] TestPrefix/AddTypedParamTestsFixture/2.doesAdd (0 ms)
[----------] 1 test from TestPrefix/AddTypedParamTestsFixture/2 (0 ms total)

[----------] 1 test from blaTest
[ RUN      ] blaTest.test1
[       OK ] blaTest.test1 (0 ms)
[----------] 1 test from blaTest (0 ms total)

[----------] 3 tests from LeapYearTestFixtureToBeParameterized
[ RUN      ] LeapYearTestFixtureToBeParameterized.1996_IsDivisibleBy4_ShouldBeALeapYear
[       OK ] LeapYearTestFixtureToBeParameterized.1996_IsDivisibleBy4_ShouldBeALeapYear (0 ms)
[ RUN      ] LeapYearTestFixtureToBeParameterized.1700_IsDivisibleBy100AndNotBy400_ShouldNotBeALeapYear
[       OK ] LeapYearTestFixtureToBeParameterized.1700_IsDivisibleBy100AndNotBy400_ShouldNotBeALeapYear (0 ms)
[ RUN      ] LeapYearTestFixtureToBeParameterized.1600_IsDivisibleBy400_ShouldBeALeapYear
[       OK ] LeapYearTestFixtureToBeParameterized.1600_IsDivisibleBy400_ShouldBeALeapYear (0 ms)
[----------] 3 tests from LeapYearTestFixtureToBeParameterized (0 ms total)

[----------] 4 tests from LeapYearFixtureTests
[ RUN      ] LeapYearFixtureTests.1IsOdd_IsNotLeapYear
[       OK ] LeapYearFixtureTests.1IsOdd_IsNotLeapYear (0 ms)
[ RUN      ] LeapYearFixtureTests.711IsOdd_IsNotLeapYear
[       OK ] LeapYearFixtureTests.711IsOdd_IsNotLeapYear (0 ms)
[ RUN      ] LeapYearFixtureTests.1989IsOdd_IsNotLeapYear
[       OK ] LeapYearFixtureTests.1989IsOdd_IsNotLeapYear (0 ms)
[ RUN      ] LeapYearFixtureTests.2013IsOdd_IsNotLeapYear
[       OK ] LeapYearFixtureTests.2013IsOdd_IsNotLeapYear (0 ms)
[----------] 4 tests from LeapYearFixtureTests (0 ms total)

[----------] 1 test from LeapYearIterationTest
[ RUN      ] LeapYearIterationTest.OddYearsAreNotLeapYears
[       OK ] LeapYearIterationTest.OddYearsAreNotLeapYears (0 ms)
[----------] 1 test from LeapYearIterationTest (0 ms total)

[----------] 4 tests from LeapYearTests
[ RUN      ] LeapYearTests.1IsOdd_IsNotLeapYear
[       OK ] LeapYearTests.1IsOdd_IsNotLeapYear (0 ms)
[ RUN      ] LeapYearTests.711IsOdd_IsNotLeapYear
[       OK ] LeapYearTests.711IsOdd_IsNotLeapYear (0 ms)
[ RUN      ] LeapYearTests.1989IsOdd_IsNotLeapYear
[       OK ] LeapYearTests.1989IsOdd_IsNotLeapYear (0 ms)
[ RUN      ] LeapYearTests.2013IsOdd_IsNotLeapYear
[       OK ] LeapYearTests.2013IsOdd_IsNotLeapYear (0 ms)
[----------] 4 tests from LeapYearTests (0 ms total)

[----------] 2 tests from AddTests/AddTypishParamTests
[ RUN      ] AddTests/AddTypishParamTests.doesAddNumbers/0
[       OK ] AddTests/AddTypishParamTests.doesAddNumbers/0 (0 ms)
[ RUN      ] AddTests/AddTypishParamTests.doesAddNumbers/1
[       OK ] AddTests/AddTypishParamTests.doesAddNumbers/1 (0 ms)
[----------] 2 tests from AddTests/AddTypishParamTests (0 ms total)

[----------] 5 tests from LeapYearTests/LeapYearParametrizedTestFixtureBasedOnFixture
[ RUN      ] LeapYearTests/LeapYearParametrizedTestFixtureBasedOnFixture.ChecksIfLeapYear/0
[       OK ] LeapYearTests/LeapYearParametrizedTestFixtureBasedOnFixture.ChecksIfLeapYear/0 (0 ms)
[ RUN      ] LeapYearTests/LeapYearParametrizedTestFixtureBasedOnFixture.ChecksIfLeapYear/1
[       OK ] LeapYearTests/LeapYearParametrizedTestFixtureBasedOnFixture.ChecksIfLeapYear/1 (0 ms)
[ RUN      ] LeapYearTests/LeapYearParametrizedTestFixtureBasedOnFixture.ChecksIfLeapYear/2
[       OK ] LeapYearTests/LeapYearParametrizedTestFixtureBasedOnFixture.ChecksIfLeapYear/2 (0 ms)
[ RUN      ] LeapYearTests/LeapYearParametrizedTestFixtureBasedOnFixture.ChecksIfLeapYear/3
[       OK ] LeapYearTests/LeapYearParametrizedTestFixtureBasedOnFixture.ChecksIfLeapYear/3 (0 ms)
[ RUN      ] LeapYearTests/LeapYearParametrizedTestFixtureBasedOnFixture.ChecksIfLeapYear/4
[       OK ] LeapYearTests/LeapYearParametrizedTestFixtureBasedOnFixture.ChecksIfLeapYear/4 (0 ms)
[----------] 5 tests from LeapYearTests/LeapYearParametrizedTestFixtureBasedOnFixture (0 ms total)

[----------] 5 tests from LeapYearTests/LeapYearMultipleParametersTests
[ RUN      ] LeapYearTests/LeapYearMultipleParametersTests.ChecksIfLeapYear/0
[       OK ] LeapYearTests/LeapYearMultipleParametersTests.ChecksIfLeapYear/0 (0 ms)
[ RUN      ] LeapYearTests/LeapYearMultipleParametersTests.ChecksIfLeapYear/1
[       OK ] LeapYearTests/LeapYearMultipleParametersTests.ChecksIfLeapYear/1 (0 ms)
[ RUN      ] LeapYearTests/LeapYearMultipleParametersTests.ChecksIfLeapYear/2
[       OK ] LeapYearTests/LeapYearMultipleParametersTests.ChecksIfLeapYear/2 (0 ms)
[ RUN      ] LeapYearTests/LeapYearMultipleParametersTests.ChecksIfLeapYear/3
[       OK ] LeapYearTests/LeapYearMultipleParametersTests.ChecksIfLeapYear/3 (0 ms)
[ RUN      ] LeapYearTests/LeapYearMultipleParametersTests.ChecksIfLeapYear/4
[       OK ] LeapYearTests/LeapYearMultipleParametersTests.ChecksIfLeapYear/4 (0 ms)
[----------] 5 tests from LeapYearTests/LeapYearMultipleParametersTests (0 ms total)

[----------] 4 tests from LeapYearTests/LeapYearParamTests
[ RUN      ] LeapYearTests/LeapYearParamTests.OddYearsAreNotLeapYears/0
[       OK ] LeapYearTests/LeapYearParamTests.OddYearsAreNotLeapYears/0 (0 ms)
[ RUN      ] LeapYearTests/LeapYearParamTests.OddYearsAreNotLeapYears/1
[       OK ] LeapYearTests/LeapYearParamTests.OddYearsAreNotLeapYears/1 (0 ms)
[ RUN      ] LeapYearTests/LeapYearParamTests.OddYearsAreNotLeapYears/2
[       OK ] LeapYearTests/LeapYearParamTests.OddYearsAreNotLeapYears/2 (0 ms)
[ RUN      ] LeapYearTests/LeapYearParamTests.OddYearsAreNotLeapYears/3
[       OK ] LeapYearTests/LeapYearParamTests.OddYearsAreNotLeapYears/3 (0 ms)
[----------] 4 tests from LeapYearTests/LeapYearParamTests (0 ms total)

[----------] Global test environment tear-down
[==========] 32 tests from 12 test suites ran. (0 ms total)
[  PASSED  ] 32 tests.
