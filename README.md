#### This is a simple application of basic calculator which adds two numbers.
#### The source code is tested using one of the UNIT TEST FRAME WORK called "gtest".
#### Also, the complete application is created  using build generator CMake.

#### explicitly setting the variables 

    set  BasicCalculatorApp_BUILD_DIR="C:/BasicCalculatorApp"
    set CONFIG = RELEASE

#### clone the repository using 
  #### creating a build folder 

    cd  %BasicCalculatorApp_BUILD_DIR%
    mkdir build 
    cd build 

  #### compling the application
    cmake -Ax64 -DCMAKE_WINDOWS_EXPORT_ALL_SYMBOLS=ON -DBUILD_SDK_PKG=ON -DGTEST_CMAKE_DIR="%BasicCalculatorApp_BUILD_DIR%\googletest" -Dgtest_force_shared_crt=TRUE -DCMAKE_INSTALL_PREFIX="%BasicCalculatorApp%\install" ..

  #### building the  application
    cmake --build . --clean-first --config %CONFIG% --target INSTALL

#### Now to run the application

    cd  %BasicCalculatorApp_BUILD_DIR%\install\bin_src 
    and run .exe file 

#### To run the test

    cd  %BasicCalculatorApp_BUILD_DIR%\install\bin_test
    and runthe .exe file

