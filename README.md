notes-to-self
=============

Link to markdown syntax: http://daringfireball.net/projects/markdown/

a couple of dime-a-dozen ideas for interesting weekend projects.

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
