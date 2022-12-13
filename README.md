# AutoGate animated jetway and docking guidance system kit

### Note
This a a fork of the original AutoGate 1.72 that was abandoned 2017 with changes to make in usable on XP12.
So the main goal is to just compile the plugin code for XP12.

The only verified working part of the build system is *../src/Makefile.mgw64* for the mingw64 system on Windows and *../src/Makefile.lin64* for Linux.
A linkable OpenAL32.dll for Windows was obtained as follows:
- get copy of libOpenAL32.dll e.g. from FlyWithLua
- pick libOpenAL's *include/AL* header files, e.g. from the msys2 system
- run within a mgw64 shell:
```
gendef OpenAL32.dll
dlltool -d OpenAL32.def -D OpenAL32.dll -k -a -l libopenal32.a -v
```
- link against libopenal32.a and put OpenAL32.dll into the plugin

### Original README
This kit allows [X-Plane](http://www.x-plane.com/) scenery designers to add animated jetways and docking guidance systems (DGS) to scenery packages. Two types of jetway and four types of DGS are included.
 
The jetway animates to dock with the plane's main door when the pilot shuts down the plane's engines with the plane within ½m of the correct stopping position. The DGS guides the pilot to the correct stopping position.

An example scenery package that uses these boarding bridges and DGSs can be found [here](http://marginal.org.uk/x-planescenery/tutorials.html#autogate).
 
## License

The plugin code in the `src` directory is licensed under the GNU [LGPL v2.1](http://www.gnu.org/licenses/lgpl-2.1-standalone.html) license.

The rest of the kit is licensed under the Creative Commons [Attribution](http://creativecommons.org/licenses/by/3.0/) license. In short, you can use any part of this kit (including the 3D objects and their textures) in original or modified form in a free or commerical scenery package, but you must give the author credit.
