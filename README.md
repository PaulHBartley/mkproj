# mkproj

## Overview
This is a family of simple bash scripts to aid in the setup of a Python project.

The family consists of three callable functions:

`$ mkproj`  <-- the parent  
`$ mkvenv`  <-- child #1  
`$ mkrepo`  <-- child #2  
 <br>  
The parent function, `$ mkproj`, acts as a "main" function and relies on its two child functions to operate. The child functions, on the other hand, can do things on their own. How convenient.
<br>  
Let's look at what this trio of functions can do together.  
  
  <br>  
  
#### Goal: Make a Python project folder.  
What do we need inside this folder?  
- A Python virtual environment  
- A local Git repository  
- A remote repository connected with the local repository  
  
Fine.  
  
We can call `$ mkproj my-new-python-project` to  
- create a new directory named `my-new-python-project`
- install a Python virtual environment inside the directory
- initialize the directory as a Git repository
- connect the local repository to a remote repository on GitHub 
  
This is a good start. But we can do more.  
  
  <br>  
  
#### Real Goal: Make a Python project folder that we can use right away.


With `$ mkproj my-new-python-project` we can also
  
- set `my-new-python-project` as the active Python virtual environment for that shell session
- use a [GitHub Template Repository](https://docs.github.com/en/free-pro-team@latest/github/creating-cloning-and-archiving-repositories/creating-a-template-repository) to automatically populate the remote `my-new-python-project` repo with any number of useful items:  
   - .gitignore  
   - README.md  
   - LICENSE  
   - INSTALL.md
   - whatever else!
- sync the local `my-new-python-project` repo with its remote counterpart on GitHub, thus making these useful items automatically appear in our local project folder  
  
  <br>  
  
#### Result: a Python project folder ready for use.
When `$ mkproj my-new-python-project` finishes, we will have a local folder with  
   - an activated Python virtual environment (if we so choose)
   - an initalized local Git repository ""
   - a remote repository on GitHub ""
   - a set of starter items for our project ""  
   
<end>  </end>  
  <br>
## `$ mkproj` Operation
`$ mkproj <directory>`

- Calling `$ mkproj <directory>` passes `<directory>` to the `$ mkvenv` and `$ mkrepo` functions, which then handle setting up `<directory>` as a Python project.

- When `$ mkproj <directory>` is called, the command presents three Yes/No prompts:
  1. Activate `<directory>` as a Python virtual environment? y/n
  2. Initialize `<directory>` as a local Git repository? y/n
  3. Set up `<directory>` as a remote repository on GitHub? y/n
  
#### Directory Behavior  
- `$ mkproj <directory>` -- makes `<directory>` (new or existing) a Python project folder inside the current working directory.  
- `$ mkproj <path>/<directory>` -- makes `<directory>` (new or existing) a Python project folder inside the path directory.  
- `$ mkproj` -- makes the current working directory into a Python project folder.  
<end>  </end>  
  <br>
## `$ mkvenv` Operation
`$ mkvenv -a <directory>`  
  
- Calling `$ mkvenv -a <directory>` installs a `.venv` folder inside `<directory>`. It then taps `$ source` to run a script named `activate` found in the `.venv` folder that was just created. Running the `activate` script sets `<directory>` as the active Python virtual environment for that shell session. The `activate` script places `(<directory>) $` to the left of the command line prompt (as shown), signaling that all Python calls made with `<directory>` as the active environment will be routed to the Python interpreter in `/<path>/<directory>/.venv`. To return the Python environment to the system-wide Python install, type `$ deactivate`.

`$ mkvenv <directory>`  

- Calling `$ mkvenv <directory>` simply installs a `.venv` folder inside `<directory>` without activating `<directory>` as the Python virtual environment.
  
#### Directory Behavior  
- `$ mkvenv [-a] <directory>` -- makes `<directory>` (new or existing) a Python environment folder inside the current working directory.  
- `$ mkvenv [-a] <path>/<directory>` -- makes `<directory>` (new or existing) a Python environment folder inside the path directory.  
- `$ mkvenv [-a]` -- makes the current working directory into a Python environment folder.  
<end>  </end>  
  <br>
## `$ mkrepo` Operation
`$ mkrepo -r <directory>`  
  
- Calling `$ mkrepo -r <directory>` sends a call to the GitHub API to create a new remote repository (called
`<directory>`) from a pre-defined template. The script then Git-initializes a new or existing local
`<directory>` and links it with the newly-created remote repository.  
  
`$ mkrepo <directory>`  

- Calling `$ mkrepo <directory>` simply initializes `<directory>` (new or existing) as a local Git repository
without connecting to the GitHub API.  
  
#### Directory Behavior  
- `$ mkrepo [-r] <directory>` -- makes `<directory>` (new or existing) a Git repository inside the current working directory.  
- `$ mkrepo [-r] <path>/<directory>` -- makes `<directory>` (new or existing) a Git repository inside the path directory.  
- `$ mkrepo [-r]` -- makes the current working directory into a Git repository.  
<end>  </end>  
  <br>  
  
## For more information:  
Please see [INSTALL.md](https://github.com/PaulHBartley/mkproj/blob/main/INSTALL.md) for how to install `$ mkproj`, `$ mkvenv`, and `$ mkrepo`.  
Also, for anyone interested, please view [CONTRIBUTING.md](https://github.com/PaulHBartley/mkproj/blob/main/CONTRIBUTING.md) for some ideas on how this project could take shape in the future.



