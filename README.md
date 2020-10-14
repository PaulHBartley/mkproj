# mkproj

This is a family of simple bash scripts to aid in the setup of a Python project.

The family consists of three callable functions:

`$ mkproj`  <-- the parent  
`$ mkvenv`  <-- child #1  
`$ mkrepo`  <-- child #2  
 <br>  
`$ mkproj` relies on its two child functions to operate.  
`$ mkvenv` and `$ mkrepo`, on the other hand, can do things on their own. How convenient.
<br>  
Let's look at what this trio of functions can do for us all together.
<br>  
### Goal: Make a Python project folder.  
What do we need for this folder?  
- A Python virtual environment  
- A local git repository  
- A remote repository connected with the local repository 

Fine.

We can call `$mkproj my-new-python-project` to  
- create a new directory called `my-new-python-project`.
- install a Python virtual environment inside the directory.
- initialize the directory as a git repository.
- connect the local repository to a remote repository on GitHub. 
  
This is a good start. But we can do more.
### Real Goal: Make a Python project folder useful.


With `$ mkproj my-new-python-project` we can also
  
- set `my-new-python-project` as the active Python virtual environment for that shell session.
- use a [GitHub Template Repository](https://docs.github.com/en/free-pro-team@latest/github/creating-cloning-and-archiving-repositories/creating-a-template-repository) to automatically populate the remote `my-new-python-project` repo on GitGub with any number of useful items:  
   - .gitignore  
   - README.md  
   - LICENSE  
   - Install.md
   - whatever else!
- sync the local `my-new-python-project` repo with its remote counterpart on GitHub, thus making the items automatically appear in our local project folder.

### Finally, a Python project folder we can use.
When `$ mkproj my-new-python-project` finishes, we will have  
- a local folder called `my-new-python-project` with
   - an activated Python virtual environment (if we so choose)
   - an initalized git repository ""
   - a connected remote repository on GitHub ""
   - an assortment of preset items for our project ""


