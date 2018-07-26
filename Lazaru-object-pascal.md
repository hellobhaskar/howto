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
```
mkdir laz-build 
cd laz-build
svn checkout https://svn.freepascal.org/svn/lazarus/trunk .
make clean && make LCL_PLATFORM=qt5 CPU_TARGET=x86_64 && make install
rm -rf ~/.lazrus/
```

