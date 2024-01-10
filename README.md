Step 1: Download graphics.h library from http://winbgim.codecutter.org/ or use this link.

Step 2: Extract the downloaded file. You’ll get three files:

graphics.h
winbgim.h
libbgi.a
Step 3: Copy and paste graphics.h and winbgim.h files into the include folder of your compiler directory. (If you have Code::Blocks installed in C drive of your computer, go through: Disk C >> Program Files >> CodeBlocks >> MinGW >> include. Paste these two files there.)

Step 4: Copy and paste libbgi.a to the lib folder of your compiler directory.

Step 5: Open Code::Blocks. Go to Settings >> Compiler >> Linker settings

Step 6: In that window, click the Add button under the “Link libraries” part, and browse and select the libbgi.a file copied to the lib folder in step 4.

Step 7: Go to “Other linker options” on the right part and paste these commands:

-lbgi -lgdi32 -lcomdlg32 -luuid -loleaut32 -lole32
Step 8: Make sure you got steps 6 and 7 right! Here’s a screenshot of previous two steps. Then, click Ok.

Graphics.h in codeblocks - Compiler Settings
Global Compiler Settings >> Linker Settings
Step 9: If you now try compiling a graphics.h program code in C or C++, you’ll still get error. To solve it, open graphics.h file (pasted in include folder in step 3) with text editor. Go to line number 302, and replace that line with this line:

"int left=0, int top=0, int right=INT_MAX, int bottom=INT_MAX"
if it is correct(same as above) then leave it as it is

Save the file. Done!

Now you can compile any C or C++ program containing graphics.h header file. If you compile C codes, you’ll still get an error saying: “fatal error: sstream : no such file directory”. For this issue, if your file extension is .c, change it to .cpp.
