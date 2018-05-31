# scripts

This repository contains useful c-shell scripts.

## run

This script automates compilation and execution of small - mostly single file - programs.
For larger projects, it can execute makefiles, assuming they are named with a .make file extention.
It works with C/C++/java/Perl/Python/c shell scripts etc.
The whole process depends heavily on the file extention:
It will run gcc for .c files, g++ for .cpp, gfortran for .for, Perl 5 for .pl, Python 3 for .py etc.
The normal behaviour is to delete all created files after execution to preserve space.
The original code files remain intact. The behaviour can be changed by using various command line options:

* -h presents some information on the program and the available options
* -c compiles without running the code
* -k keeps the files after execution
* -q denotes a Qt .cpp code file, from which the script will try to create and run the project
* -b denotes that the code requires linking to the Boost libraries (they should obviously be installed on the system)
* -t compiles a LaTeX project and opens up the postscript file for viewing.

To be noted - the script does not "play well" with filenames which include spaces.
Such files may need to be renamed, eg by executing space2Underscore.cpp which is found in utilities (requires Boost)


## re-encode

This script uses iconv to change the encoding of files.
It presents a list of the encodings, then prompts for the initial and final encodings of the file(s).
The option -h presents a help screen with useful information.
As with the run script above, it doesn't "play well" with filenames that include spaces, so any
such files may need to be renamed, eg by executing space2Underscore.cpp which is found in utilities (requires Boost)
