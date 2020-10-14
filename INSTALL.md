# Installing mkproj  

**mkproj** is a family of three bash functions that work together to set up a Python project folder.

## Compatibility

**mkproj** has been tested on **Ubuntu 20.04** in **GNU bash, version 5.0.17**.
The scripts should work in other bash 5.0+ environments (assuming Python 3.5+ is installed). On other systems and/or shells, however, please exercise caution. If any problems are found, please don't hesitate to open an issue.

## Files to be installed  
`$ mkproj` <-- parent function  
`$ mkvenv` <-- child function #1  
`$ mkrepo` <-- child function #2  
  
### To install `$ mkproj`, `$ mkvenv`, and `$ mkrepo`:  

1) Fork the **mkproj** repo to your GitHub account.

2) Clone the **mkproj** repo from your GitHub account to your local drive.

3) Copy `$ mkproj`, `$ mkvenv`, and `$ mkrepo` into a local directory listed in the PATH environment variable (where the shell looks for executables).
   - If it doesn't already exist, you could create a `~/bin` directory and place the **mkproj** files in `~/bin`.  
   - If you do create a `~/bin` directory, make sure to add `/home/<username>/bin/` to the PATH variable.  
   - Any local `<directory>` can be appended to the PATH variable by adding a line to the `~/.bashrc` file:  
   - `export PATH="$PATH:/home/<username>/<directory>`.
   - You will have to restart the shell for the changes to take effect.
