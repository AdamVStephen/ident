# ident
Demonstration of techniques for putting git version information back into code files for run time provenance.

See blog post : avstephen.wordpress.com

See StackOverflow discussion : 3442874


# scripts


# workflow

This repo will use two permanent branches :

1. master for tested, working, stable examples
1. dev for development/experimental code


Feature branches will be transitory for adding features and will be merged into dev, then dev merged into master.


# pre-commit
The pre-commit script executes before the commit if installed in the .git/hooks/ directory.
