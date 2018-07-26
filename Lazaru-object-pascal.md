# FreePascal/ObjectPascal Programming Repo for Starters 

# Editor Support
  * Lazarus IDE
  * Visual Studio Code ( using omni pascal Extension)


# How to build Lazarus on Macosx (Using Cocoa)

```
mkdir laz-build 
cd laz-build
svn checkout https://svn.freepascal.org/svn/lazarus/trunk .
make clean && make LCL_PLATFORM=cocoa CPU_TARGET=x86_64 && make install
rm -rf ~/.lazrus/
```

# How to build Lazarus on Linux(Using Qt5)

QT5 bindings for lazarus dependent on library called libqt5pas. This is present in lazarus/lcl/interfaces/qt5/cbindings
but require some handholding to compile without any issues.
checkout lazarus source code
```
mkdir laz-build 
cd laz-build
svn checkout https://svn.freepascal.org/svn/lazarus/trunk .
```

on fedora28 i had to install below packages
```
dnf install -y qt5-qtx11extras-devel
cd laz-build/lcl/interfaces/qt5/cbindings
qmake-qt5 all
make install
```
this should install libqt5pas.so.1 in /usr/lib directory. then we can proceed for actual code compilation of lazarus main ide.

```
cd laz-build
make clean && make LCL_PLATFORM=qt5 CPU_TARGET=x86_64 && make install
rm -rf ~/.lazrus/
```

