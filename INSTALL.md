# Installing mkproj  

**mkproj** is a family of bash functions installed as three executable files.

## Files to be installed  
`$ mkproj` <-- parent function  
`$ mkvenv` <-- child function #1  
`$ mkrepo` <-- child function #2  
  
## Compatibility
The functions have been tested in **GNU bash, version 5.0.17** on **Ubuntu 20.04**.
They should work in other bash 5.0+ environments (assuming Python 3.5+ is installed).

## Dependencies  
- Python 3.5+ (tested with Python 3.8.5)
- Python venv module  

## Bash environment variables that need to be defined for connecting to GitHub:
(set these in the `~/.bashrc` file)
- GITHUB_USERNAME
- GITHUB_TOKEN
- GITHUB_TEMPLATE_REPO

## To install `$ mkproj`, `$ mkvenv`, and `$ mkrepo`:  

1) Fork the **mkproj** repo to your GitHub account.

2) Clone the **mkproj** repo from your GitHub account to your local drive.

3) Use `$ chmod +x mkproj mkvenv mkrepo` to make the files executable.

4) Copy the three files into a local directory listed in the PATH environment variable (where the shell looks for executables).
   - If it doesn't already exist, you could create a `~/bin` directory and place the **mkproj** files in `~/bin`.  
   - If you do create a `~/bin` directory, make sure to add `/home/<username>/bin/` to the PATH variable.  
      - Any local `<directory>` can be appended to the PATH variable by adding a line to the `~/.bashrc` file:  
         - `export PATH="$PATH:/home/<username>/<directory>`.
   - You will have to restart the shell for the changes to take effect.
