
# OVERVIEW
This function consolidates the process of setting up a Python project
folder into one command with three yes/no prompts.

# OPERATION
"$ mkproj <directory>" takes an as-to-be-created or existing <directory>
and calls the "$ mkvenv" and "$ mkrepo" functions, which take care of
setting up <directory> as a Python project.

"$ mkproj <directory>"
1. Prepare <directory> as a Python virtual environment.
A) Activate <directory> as a Python virtual environment? y/n
B) Initialize <directory> as a git repository? y/n
C) Create a remote repository for <directory> on GitHub? y/n

# DIRECTORY BEHAVIOR
"$ mkproj <directory>" -- makes <directory> (new or existing) a Python
project folder within the current working directory.
"$ mkproj <path>/<directory>" -- makes <directory> (new or existing) a
Python project folder inside the path destination directory.
"$ mkproj" -- makes the current working directory into a Python project
folder.



# OVERVIEW
This function calls the "$ python venv" module to create a Python virtual environment, and it
gives the option to activate the environment directly after the environment is created.

# OPERATION
"$ mkvenv -a <directory>" installs a .venv folder inside <directory> and calls "$ source" to
run a script named "activate" inside the .venv folder. Running the "activate" script transforms
<directory> into the active Python virtual environment for that shell session. The "activate"
script places "(<directory>) $ " to the left of the command line prompt (as shown), signaling
that all Python calls made when <directory> is active will be routed to the Python interpreter
in /<path>/<directory>/.venv. To return the Python environment to the system-wide Python
install, type "$ deactivate".

"$ mkvenv <directory>" simply installs a .venv folder inside <directory> without activating
<directory> as the Python virtual environment.

For the script to work, python3.8 (or later) and the venv module need to be installed.

# DIRECTORY BEHAVIOR
"$ mkvenv [-a] <directory>" -- makes <directory> (new or existing) a Python environment folder
within the current working directory.
"$ mkvenv [-a] <path>/<directory>" -- makes <directory> (new or existing) a Python environment
folder inside the path destination directory.
"$ mkvenv [-a]" -- makes the current working directory into a Python environment folder.


# OVERVIEW
This function wraps "$ git init <directory>" with a script giving the option to automatically
connect <directory> with a remote repository on GitHub.

# OPERATION
"$ mkrepo -r <directory>" sends a call to the GitHub API to create a new remote repository (called
<directory>) from a pre-defined template. The script then git-initializes a new or existing local
<directory> and links it with its remote counterpart.

"$ mkrepo <directory>" simply initializes <directory> (new or existing) as a local git repository
without connecting to the GitHub API.

For the script to work, git needs to be installed, and the following variables need to be set in
the active shell environment.

GITHUB_USERNAME
GITHUB_TOKEN
GITHUB_TEMPLATE_REPO

# DIRECTORY BEHAVIOR
"$ mkrepo [-r] <directory>" -- makes <directory> (new or existing) a git repository inside the
current working directory.
"$ mkrepo [-r] <path>/<directory>" -- makes <directory> (new or existing) a git repository inside
the path destination directory.
"$ mkrepo [-r]" -- makes the current working directory into a git repository.
