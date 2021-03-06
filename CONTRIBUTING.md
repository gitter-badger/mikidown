# Translating
* Change into the directory where the mikidown source code is
* Run ```pylupdate4 -verbose mikidown.pro```
* Replace all instances of ```filename="mikidown``` with ```filename="../mikidown``` 
in the generated locale/*.ts files
* Open Qt Linguist with those *.ts files.
* Start translating!
* Alternatively, you can visit <https://www.transifex.com/projects/p/mikidown/resources/> 
to see what needs to be translated. Any translations there will be pulled back into 
the github repo.

# Bug Reporting
Please provide a backtrace of the relevant errors like in #43. If it's a logic 
error (as in a variable's set to a wrong value), here's what you can do to help me
find the error (if I haven't found it yet):
* Run ```python -m pdb mikidown.py```
* Set some breakpoints with ```b mikidown/${relevantfile}.py:lineno``` in pdb. lineno
should be the place just before the relevant variable changes to an unexpected value.
* Run the program with ```run``` in pdb
* When you get to the breakpoint, print out the variable values with ```p ${relevantvariable}```

If you don't know how to do this, please describe in detail what you did in the GUI to
trigger the error (as in what buttons you pressed, etc.).

# Coding
Ideally, you should create a pull request so I can see what kinds. Otherwise, you can
put the patch in a pastebin so I can pick it up from there. If you pick the pastebin
option, please link to a pastebin that has syntax highlighting.
