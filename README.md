# vscode-mac-c-example
A very simple Visual Studio Code C / C++ project for macOS

### Why ?
I couldn't find a very simple VS Code project for Mac C/C++ development using the Microsoft cpptools extension.  
So I created one.

### Requirements

XCode and the developer command-line tools.  
This project assumes that you already have XCode installed.  
Why ? Well, if you're developing on a Mac you'll need XCode, if only for the macOS SDK and C/C++ header files/libraries.

Visual Studio Code and the Microsoft cpptools extension


### Files

* helloworld.c - a very simple c program (with several lines, so you can try setting breakpoints).

In the .vscode folder (which will be hidden in the Finder) - 3 files required for building and debugging.
* tasks.json - specifies how to build helloworld.c (including debug symbols) 
* launch.json - specifies how to build then debug helloworld.c
* c_cpp_properties.json - specifies the location of c/c++ include files


### To use

Provided you have installed XCode in the default location (i.e. /Applications) and you've already installed the Microsoft cpptools extension in VS Code, the project *should* just work, as follows:

1. Download and unzip the repo or git clone it.
2. In VS Code:  

    2.1 Open the local folder.  
    It'll be called vscode-mac-c-example-master if you've cloned it, or vscode-mac-c-example if you used git clone  
    
    2.2 Open the file helloworld.c  
    I told you it was simple...
    
    2.3 Set a breakpoint on one of the lines (by clicking to the left of one of the line numbers)  
    
    2.4 Click on the "Debug" symbol on the left (or Cmd+Shift+D)  
    
    2.5 Click on the green triangle (i.e. start debugging)  
    The program should build, run in the debugger and stop at your breakpoint with the debug console showing.
    
    2.6 Use the debug control (at the top) to step / run in the debugger.  
    The debug console should show the program's output, like this:  
	
    ~~~~
    @"(i should be 1234) i = 1234\r\n"
    @"(i should be 4321) i = 4321\r\n"
    ~~~~

    Note that the format of the output is weird (spurious '@', '\r' and \n' characters).  
    It's probably a cpptools bug/feature.








