# Process_deadlock_with_Mutex
Here we are simulating  a programme which deals mutual exclusion with the pthread.h library to solve de problem of process deadlock in an Os.
Its a c language and am conpiling on CodeBlock Ide you will be set to install the pthread.h library on the Ide.

The idea is that first a thread expresses its desire to acquire a lock and sets flag[self] = 1 and then gives the other thread a chance to acquire the lock.
If the thread desires to acquire the lock, then, it gets the lock and passes the chance to the 1st thread. If it does not desire to get the lock then the while loop breaks and the 1st thread gets the chance.

How to install:

The procedure to incorporate the library into MinGW for CodeBlocks is as follows:

1. unzip pthreads-w32-2-9-1-release.zip into its own directory

2. Go into directory pthreads-w32-2-9-1-release\Pre-built.2

3. Copy all the h files from pthreads-w32-2-9-1-release\Pre-built.2\include  into the MinGW include directory, usually in C:\Program Files (x86)\CodeBlocks\MinGW\include

4. Copy all the library files in pthreads-w32-2-9-1-release\Pre-built.2\lib\x86 into directory C:\Program Files (x86)\CodeBlocks\MinGW\lib

5. Added the -lpthreadGC2 option into Project --> Build Options --> Linker Settings --> Other Linker Options of the CodeBlocks IDE

(also make sure that "jpeg"  is in is in Project --> Build Options --> Linker Settings --> Link Libraries

The project then should compile fine on Windows.

DEVC++ FOR WINDOWS PTHREAD installation 

For this you just need to install the package pthreads_w32-2.8.0-1aj.DevPak. This file is in Resources/LIBS  in the zip file DevC++ Libs.zip

Close DevC++ and double click on the pthreads_w32-2.8.0-1aj.DevPak  agree to installing (the system should recognize .DevPak extension and open the package manager).

Once that is successfully installed, quit the package manager and load DevC++, which should now work fine for compiling pthreads, and should be happy with linking in the libjpeg library that is included in the Prac2 zip file.

