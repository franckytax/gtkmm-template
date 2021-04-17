This gtkmm3 project template use cmake to work.

VISUAL STUDIO CODE USERS

If like me, you want that visual studio code detects all gtkmm header files installed after installed the gtkmm3 package of your distribution, execute the following command:
pkg-config --cflags gtkmm-3.0

Then add all the paths beginning with -I in the includePath list inside the c_cpp_properties.json file.
Now Visual studio Code may detect the gtkmm headers like "#include <gtkmm/main.h>".

How to compile with the command line
cd gtkmm-template
mkdir build && cd build
cmake ..
make

An other solution is to use the CMake-Tools extension to configure and compile your project inside Visual Studio Code.
