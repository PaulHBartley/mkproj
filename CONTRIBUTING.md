# Contributing to mkproj  
  
  First of all, thanks a lot for taking a look at this project. I hope it can be of use to someone.
  
  My goals with this are to continue to add features and eventually branch out into other languages besides Python. It would be neat if it could be configured to jumpstart projects from a "menu" of languages. To do this properly would require some kind of configuration file with a set of parameters general enough to apply to each language. Along with this, there would have to be a less idiosyncratic way of handling the input arguments. This would most likely mean rebuilding the input around a `case` conditional statement combined with the `$ getopt` utility.
  
  If any of this sparks your interest, please do not hesitate to fork away and have at it!
  
  Here is a list of ideas for future development:
  1) Add additional "child" functions for setting up projects in other languages (beyond Python).
  2) Redo the input scheme to make it less cumbersome to maintain or extend.
  3) Figure out a way of storing configuration parameters that would apply to all languages.
  4) Add the capability to switch between templates from a list of different [template repositories](https://docs.github.com/en/free-pro-team@latest/github/creating-cloning-and-archiving-repositories/creating-a-template-repository).
  5) Make these scripts more portable/less Bash-centric?
  
  Feel free to get in touch with any questions/comments!
