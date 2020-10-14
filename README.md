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
Let's look at what this trio of functions together can do for us.
<br>  
### Goal: Make a Python project folder.  
What do we need for this folder?  
- A Python virtual environment  
- A local git repository  
- A remote repository connected with the local repository 

Fine.

We will call `$mkproj my-new-python-project` to  
- create a new directory called `my-new-python-project`.
- install a Python virtual environment inside the directory.
- initialize the directory as a git repository.
- connect the local repository to a remote repository on GitHub. 
  
This is a good start.  
Taking this a step further, with `$ mkproj my-new-python-project` we can
  
- make `my-new-python-project` the active Python virtual environment for that shell session (if we so choose)






