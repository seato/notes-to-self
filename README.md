notes-to-self
=============

getting started
---------------
eat a healthy breakfast, the most important meal of the day

then check out the .DO_NOT_REAME; if you're not in there, then go on

if you are, then scrolling down will trigger the release of a horde of bees

to arrive in 3-5 business days, free shipping and handling!

markdown syntax
---------------
http://daringfireball.net/projects/markdown/

don't ask, don't tell
---------------------
grep -rilE "programmer|author" * | grep -viE ".pl|.py" | xargs grep -rinEA 5 "programmer|author"

dime-a-dozen ideas for interesting weekend projects
---------------------------------------------------

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
>  FEATURES, FEATURES EVERYWHERE!

Generic cleanup script
> Remove tilde files, calls make cleans, removes objects/bins/exes
> car_wash PROJECT_DIR
>
> And for the wealthy
> car_wash -premium PROJECT_DIR
> Strips out .cvs/.git/.svn/etc files for export
> Hell, I'll throw a tarball in there for free!

Alias backing up directories
> $ bk
> instead of
> $ cd ..
> or
> $ bk 5
> $ cd ../../../../..
