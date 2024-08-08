# Finishing for Linux
### Script Installation
- Some hacking tools are developed by some peoples and those peoples make it open-source, that means we can get those scripts/programs from github.
- Syntax: git clone <link_of_the_script_from_github>
##### script modules
-  modules/libraries are needed to run the script as the dependencies.
1. Python: to install python modules we use -> pip install [modulename]
    - For requirements file -> pip install -r requirements.txt
2. Go: to install go modules -> go install [modulename]
3. Ruby:  to install ruby modules -> gem install [modulename]
###### Errors you may encounter
- Don’t close apt while installation
- Repository errors, if this happened you can fix it using
    - sudo apt edit-sources
- man(manual)- gives the whole manual and instruction of a tool or command.
    - ==man [yourcommand]
- help- gives usage options for commands.
    -  ==[yourcommand] -h==
#### Linux Processes & Services
- To get the processes: ==ps [options]
    - ==ps==  -> for process running on my shell
    - ==ps -A== -> view all running process
    - ==ps -u username== -> view users process
- To stop process: ==Kill [options] {PID}
    - ==kill -19 PID==  -> to stop the process
    - ==kill -18 PID== -> to resume the process we stopped
    - ==kill -9 PID== -> to Stop a process immediately
##### Foreground / background
- Use the “&” operator, to run programs in the “background” or press ^ Z. e.g- nano sample.txt&
- To get the background process back to foreground simply type: **fg**
- To stop a process going inside your shell just press ^ C
##### Null device
- **/dev/null** - Redirects output to nowhere.
- The null device is a special file that throws away whatever is fed to it.
- **>** = redirecting symbol
- On shell output there are 2 things.
    - STDERR =  2
    - STDOUT  =  1
- To redirect the errors from a command result we do 
    - command 2 > filename
- To redirect the error-FREE output
    - command 1>filename
##### Symbolic linking
- Symbolic linking is same as Windows shortcut.
- Symbolic linking is a process of creating a linked shortcut form of file to some pre-existed file or folder.
- syntax: ln  -s source_filePATH filename 
##### alias
- Used to give a name to some bunch of commands.
- Example: if I wanted to name ls -la  ‘rex   so any time i want to get output of ls -la I just type rex.
    - **alias rex=’ls -la’**
- to configure alias use:
    - Bash = ~/.bashrc
    - Zsh = ~/.zshrc
    - Fish = ~/.config/fish/config.fish
###### tmux usage
- To split horizontally = ^A then o
- To split vertically = ^A then e
- To exit = ^A then x or just type ‘exit’
- To create tab = ^A then c
- To rename the tab = ^A then ,(comma)
- To switch tabs= ^A then {numbers}
- To switch partitions = ^A  then {arrow}
**Wget -** is a tool used to download files from websites/servers.
- Syntax: wget {options} [link].
**find-** uses for searching files/folders/musics/videos on terminal.
- Syntax: find [search path]  {options} {search word}.
