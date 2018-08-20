# Use-Graphics.h-in-Atom-CodeBlocks-and-DevC-
*How to use graphics.h in latest IDE's &amp; Editors 2018*

##### Just Follow the Steps for CODE::BLOCKS :-

1. Clone the files from this repository. And download the [Code::Blocks](http://sourceforge.net/projects/codeblocks/files/Binaries/17.12/Windows/codeblocks-17.12mingw-setup.exe). 
2. Now copy the __*graphics.h*__ & __*winbgim.h*__ header files in ```C:\Program Files\CodeBlocks\MinGW\include``` directory.
3. Now copy the __*libbgi.a*__ library file in ```C:\Program Files\CodeBlocks\MinGW\lib``` directory. 
> ```Note:``` It may possible that your codeblocks installation is in another folder like **Program Files(x86)** by default codeblocks is installed in this directory. So find your path accordingly.
4. Now open your codeblocks and go to ```Settings > Compiler Settings > Linker Settings```. Click on ```Add``` to **link libraries** and browse your __*libbgi.a*__ library file; should be like ```C:\Program Files\CodeBlocks\MinGW\lib\libbgi.a```.
5. In Linker Settings paste these linkers in __*Other linker options*__.

        -lbgi
        -lgdi32
        -lcomdlg32
        -luuid
        -loleaut32
        -lole32
6. Cheers :tada: :metal: Now run any graphics program. Remember that your program should be like __*name_of_file*__.```cpp```. Because ```C``` doesn't support *sstream*.
    

    
    
    
    
    
    
    
