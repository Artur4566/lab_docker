# Laboratory work VI: CPack

## Author
Artur
GitHub: Artur4566

## Tutorial

### Step 1. Setup project
Cloned lab05, added version variables to CMakeLists.txt.

### Step 2. Create CPackConfig.cmake
Created configuration for DEB, RPM, TGZ, WIX, DragNDrop packages.

### Step 3. Build and package locally
cmake -H. -B_build
cmake --build _build
cpack -G "TGZ"

text

### Step 4. GitHub Actions CI/CD
Workflow builds packages automatically on tags:
- Linux: TGZ, DEB, RPM
- macOS: DragNDrop (.dmg)
- Windows: WIX (.msi)

### Step 5. Release
Tag v0.2.0.1 triggered automatic build.
Release includes 5 packages:
- print-0.1.0.0-Linux.deb
- print-0.1.0.0-Linux.rpm
- print-0.1.0.0-Linux.tar.gz
- print-0.1.0.0-Darwin.dmg
- print-0.1.0.0-win64.msi

## Links
- [CPack DEB](https://cmake.org/cmake/help/latest/cpack_gen/deb.html)
- [CPack RPM](https://cmake.org/cmake/help/latest/cpack_gen/rpm.html)
- [CPack WIX](https://cmake.org/cmake/help/latest/cpack_gen/wix.html)
- [CPack DragNDrop](https://cmake.org/cmake/help/latest/cpack_gen/dmg.html)
