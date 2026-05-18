# Laboratory work 6: CPack

## Author
Artur

## CI/CD Status
- GitHub Actions: ✅ Passing

## Build and Package
mkdir build && cd build
cmake .. -DBUILD_TESTS=ON
cmake --build .
ctest
cpack -G "TGZ;DEB;RPM"

## Repository
https://github.com/Artur4566/lab06
