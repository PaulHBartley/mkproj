# Installing mkproj  

**mkproj** is a family of three Bash functions installed as three executable files.

## Files to be installed  
`$ mkproj` <-- parent function  
`$ mkvenv` <-- child function #1  
`$ mkrepo` <-- child function #2  
  
## Compatibility
The functions have been tested in **GNU Bash, version 5.0.17** on **Ubuntu 20.04**.
They should work in other Bash 5.0+ environments (assuming Python 3.5+, Git, and Curl are installed).

## Dependencies  
- Python 3.5+ (tested with Python 3.8.5)
- Python venv module  
- Git
- A GitHub account with
   - a [Personal Access Token](https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/creating-a-personal-access-token)
   - a [Template Repository](https://docs.github.com/en/free-pro-team@latest/github/creating-cloning-and-archiving-repositories/creating-a-template-repository)
- Curl

## Bash environment variables needed for connecting to the GitHub API:
(define these in the `~/.bashrc` file)
- `GITHUB_USERNAME`
- `GITHUB_TOKEN`
- `GITHUB_TEMPLATE_REPO` (the name of a template repository)

## To install `$ mkproj`, `$ mkvenv`, and `$ mkrepo`:  

1) Fork the **mkproj** repo to your GitHub account.

2) Clone the **mkproj** repo from your GitHub account to your local drive.

3) Use `$ chmod +x mkproj mkvenv mkrepo` to make the files executable.

4) Copy the three files into a local directory included in the PATH environment variable (where the shell looks for executables).
   - If it doesn't already exist, you could create a `~/bin` directory and place the **mkproj** files in `~/bin`.  
   - If you do create a `~/bin` directory, make sure to add `/home/<username>/bin` to the PATH variable.  
      - Any local `<directory>` can be appended to the PATH variable by adding this line to the `~/.bashrc` file:  
         - `export PATH="$PATH:/home/<username>/<directory>"`. 
   
5) Add the following to the `~/.bashrc` file:
   - `source ~/<directory>/mkproj`
   - `source ~/<directory>/mkvenv`
   - `source ~/<directory>/mkrepo`

6) You will have to restart the shell for the changes to take effect. 
