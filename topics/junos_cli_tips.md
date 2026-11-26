## these are some CLI tips I picked up while working on Junos
1)  **Keeping your command history intact while switching between different junos modes**
Junos allows you to use normal unix shell along with the operation mode and configuration mode.
Operational mode command line workflow is powerful, in the sense that it lets you use the normal
 emacs-style navigation within the command you are typing and also navigate to previous commands
you typed just like other Unix shells along with a powerful command completion and suggestion with `?` (my favorite one).
 
Now when you are in operational mode and used some specific commands now you want to switch to
Unix shell mode to do some work like using vim to analyze logs or checking processes or files.
you type `exit` and now you are in the unix shell but when you type cli again to enter into
operational mode you will lose your command history that
you previously entererd and now you can't use up arrow key ^ to get your previous
commands.

How to counter this ??

as cli is just a UNIX process you can just suspend the cli process using 
`CTRL-Z` and push it to the background and get your shell 
back (csh by default), now you can 
do your usual work in the unix shell. Now if you want to return to the cli
mode just type `fg` command which will bring the suspended process to foreground and resume it 
with your command history intact now you can use the up/down arrow key to navigate between your previous commands. 
