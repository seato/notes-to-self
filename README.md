notes-to-self
=============

do not readme
-------------
potential employers  
start-ups looking for the next big thing  
grammer nazis  
sensitive to profanity or crude humor  
my mother  

getting started
---------------
Eat a healthy breakfast, the most important meal of the day.  
Done?  
Now check out the .DO_NOT_REAME; if you're not in there, then continue on ahead.  
But if you are on there, then scrolling down will trigger the release of a horde of bees to arrive in 3-5 business days, free shipping and handling!

state of the wiki
-----------------
This is the extended portion of my brain. There's a couple of cool things laying around.  
* a reference to GitHub's [[markdown syntax]]
* [weekend projects](https://github.com/SuitAndThai/notes-to-self/wiki/dime-a-dozen-ideas-for-interesting-weekend-projects) which may or may not get done
* my own personal references to [find](https://github.com/SuitAndThai/notes-to-self/wiki/practical-find), [grep](https://github.com/SuitAndThai/notes-to-self/wiki/practical-grep), and [sed](https://github.com/SuitAndThai/notes-to-self/wiki/practical-sed)
* [programming humor](https://github.com/SuitAndThai/notes-to-self/wiki/don%27t-ask,-don%27t-tell)
http://daringfireball.net/projects/markdown/Flesh out the bash portion of the README.

Example python program
> Sis wants a quick python program doing some simple input > process > output
> Maybe calculating pi, fibonacci numbers, or some obscure equation with a window
> will be good enough.

A new form-filling technology
> Too many forms ask for the same information, when it's needlessly redundant.
> Not only that, but there's a needless middle-man layer to interact with your forms
> assuming that you're not doing it by hand (which you shouldn't, it's the 21st century).
> What needs to happen is a single interface, or form, which directly writes to the
> database (or XML file to be transferred to a database).
> This is mainly concerning the abuse of the .ifm file format, which is used as a way to
> directly write to a form template which can be exported into a .pdf.
> ifm stands for iPrevent fraud management (Brighterion is the company), whose main use
> is the prevention of credit card/account/etc fraud in real-time
> There is no purpose to using it except to directly affect form templates which can be
> exported to PDF, that should not be a reason to use a technology.
> In fact, tt would save a lot of trouble, heartache, and costs if it could be free!

A script to easily pump your 'find' and 'grep' commands without you putting in the flags
> I would absolutely love to try having it parse natural language
> find and grep commands and flags are easy to the person who typed them up
> but they're a pain to read and interpret to anyone else reading them
> and people love just running things they don't understand, a very bad habit of mine too
> Consider:
> $ findme "foo|joo" in goo* for txt/c/cpp, ignore caps, give me 5 lines
> instead of
> $ find -iname "goo*.txt" | grep -vE "txt|c|cpp" | xargs grep -rinEA 5 "foo|joo"
> Admittedly, that's a special use case, but it's easier to understand the first one

Backup script (create .bak versions of files)
> I only need this cause I'm tired of switching computers to CVS revert
> A simple copy, this should be one of my special scripts

Program to sync notes
> This is pretty heavy duty, but a fun exercise
> It would sync (commit + push) with github after editing
> I'm better off using dropbox, but I wanna try syncing to github and then a fileserver
> It's the journey that matters you jerk!

Script to delete trailing whitespace (and then something to constantly check for it)
> It's a common enough task, might as well.
> Could restrict the tool to certain projects/directories.
> May be able to build this up to enforce coding standards
> - Delete trailing whitespace
> - Ensure the author of .c or .h files are listed
> - Spell check README's
> - Check to see that each line is no longer than 80 chars
>
>  FEATURES, FEATURES EVERYWHERE!

Generic cleanup script
> Remove tilde files, calls make cleans, removes objects/bins/exes
> car_wash PROJECT_DIR
>
> And for the wealthy
> car_wash -premium PROJECT_DIR
> Strips out .cvs/.git/.svn/etc files for export
>
> Hell, I'll throw a tarball in there for free!
my most common use cases  

# basic usage  
1. find based off a subset of name  
`$ find -name "*foo*"`  
2. ignore capitalization  
`$ find -iname "foo"`  
3.  match inversion  
`$ find -not -iname "foo" # opposite day!`  

# fun usage  
1. execute command on the files found  
`$ find -iname "foo" -exec rm -rf '{}' ';' # in this case, i'm deleting it all`  

an awesome link for more [find examples](http://www.thegeekstuff.com/2009/03/15-practical-linux-find-command-examples/)  my most common use cases

# basic usage  
1. grep for a string in a directory  
`$ grep "foo" dir/ect/ory # i love it when people pull this off and i never i catch on that it's an example directory`  
`$ grep "foo" * # search ALL of the directories`
2. ignore capitalization with grep  
`$ grep -i "foo" *`  
3. invert the results
`$grep -v "foo" * #anything without foo`
3. grep a specific word  
`$ grep -w "foo" * #not too useful with code if the word is connected to otherdescriptors with an underscore or similar`  
4. see the lines before/after/around a matching term  
`$ grep -B 5 "foo" * #5 lines before match`  
`$ grep -A 5 "foo" * #5 lines after match`  
`$ grep -C 5 "foo" * #5 lines around match`  
5. recursive grep in subdirectories  
`$ grep -r "foo" * #we're going deep!`  
6. count lines containing match  
`$ grep -c "foo" * #LOC is just a number`  
7. display file names  
`$ grep -l "foo" *`  
8. show line number of match  
`$ grep -n "foo" *`  
9. can haz regex plz?  
`$ grep -E "foo|bar * #find foo or bar"`

# fun usage  
1. the only efficient way to use grep is to combine flags for generic search  
`$ grep -rin "foo" * #all directories, ignore the case, and gimme yo numba`  
2. get the files that contain the string, exclude certain files, then store those lines around it in a file  
`$ grep -rilE "programmer|author" * | grep -viE ".pl|.py" | xargs grep -rinEA 5 "programmer|author" > hit_list`  

an awesome link for more [grep examples](http://www.thegeekstuff.com/2009/03/15-practical-unix-grep-command-examples/)  
my most common use cases

# basic usage (90% of the time)  
1. sed substitute one string for another  
`$ echo foobar | sed 's/bar/lish/'`  
2. sed substitute one string for another, and overwrite the file in place  
`$ sed -i 's/bar/lish/' foo.txt`  

an awesome tutorial for more [sed usage](http://www.grymoire.com/Unix/Sed.html)  
`$ grep -rilE "programmer|author" * | grep -viE ".pl|.py" | xargs grep -rinEA 5 "programmer|author" > hit_list`  
Look in all of the files for references to programmers or authors, ignore the python scripts and prolog crap, then store the lines containing the programers/authors in my hit_list.  
If you want to be able to read this for what it is, check out my page on [[practical grep]] commands  