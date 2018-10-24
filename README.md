# Use-Graphics.h-in-Atom-CodeBlocks-and-DevC-
*How to use graphics.h in latest IDE's &amp; Editors 2018*

### Just Follow the Steps for CODE::BLOCKS :-

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

>For **Dev C++** you have to do the same upto __*Linker*__ step. You need to add linkers with the project, just paste the linkers in ```Project Options > Parameters > Linkers```. __Or__ You can do it every project by pasting it in ```Tools > Compiler Options > General > in second textbox```

### Just Follow the Steps for Atom :-
1. Clone the files from this repository. And download the [Atom](https://atom.io/).
2. Download the GCC compiler [MinGW](https://sourceforge.net/projects/mingw/). And install it. Mark all options for installation.
3. Set the path for the compiler. Go to ```Control Panel > System > Advanced System Settings > Environment   Variables > Path > Edit > New > paste C:\MinGW\bin```
4. Now open the Atom and install a package ```gpp-compiler``` from __*press (ctrl + comma) it'll open settings > Install*__.
5. After that paste those linkers, go to ```Open settings > Packages > Settings of gpp-compiler package > C++ Compiler Options```.
6. Done! Create new file and press *f5* to run the program.

# Graphics in Linux Ubuntu/Mint/Fedora
1. First Download the suitable binary file, according to your Linux OS
The current release of SDL_bgi is  **2.2.3**. To compile it from sources, you will need a compiler (gcc or  [clang](http://clang.llvm.org/) are fine), make, and SDL2. On Debian and Ubuntu-like distributions, you will need the package 'libsdl2-dev' and its dependencies.

Building has been tested on GNU/Linux Mint 18.*, Fedora 26, Windows ([MSYS2](https://www.msys2.org/)  + mingw-w64,  [Code::Blocks](http://codeblocks.org/),  [Dev-C++](http://orwelldevcpp.blogspot.com/)  ), and Mac OS X Yosemite.

-   Sources:  [SDL_bgi-2.2.3.tar.gz](https://sourceforge.net/projects/libxbgi/files/SDL_bgi-2.2.3.tar.gz)
-   Source RPM package:  [SDL_bgi-2.2.3-1.src.rpm](https://sourceforge.net/projects/libxbgi/files/SDL_bgi-2.2.3-1.src.rpm)
-   64 bit binary RPM package (Fedora):  [SDL_bgi-2.2.3-1.x86_64.rpm](https://sourceforge.net/projects/libxbgi/files/SDL_bgi-2.2.3-1.x86_64.rpm)
-   64 bit binary DEB package, for Debian-like Linux distributions:  [sdl_bgi_2.2.3-1_amd64.deb](https://sourceforge.net/projects/libxbgi/files/sdl_bgi_2.2.3-1_amd64.deb)
-   binaries for Windows (MSYS2 + mingw-w64, CodeBlocks, Dev-C++):  
    [SDL_bgi-2.2.3-win.zip](https://sourceforge.net/projects/libxbgi/files/SDL_bgi-2.2.3-win.zip)
-   Previous versions sources:  
    [SDL_bgi-2.2.2.tar.gz](https://sourceforge.net/projects/libxbgi/files/SDL_bgi-2.2.2.tar.gz)  
    [SDL_bgi-1.0.1.tar.gz](https://sourceforge.net/projects/libxbgi/files/SDL_bgi-1.0.1.tar.gz)
    
2. To compile a program using SDL_bgi, make sure that it includes the 'graphics.h' header file. Then:

    ```gcc -o program program.c -lSDL_bgi -lSDL2```
3. If you want to integrate this with your favourite editors the simply add linker. 

    ```-lSDL_bgi```
    ```-lSDL2```

 
   

    
    
    
    
    
    
    
