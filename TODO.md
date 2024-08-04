# GitHub Pages

* Make website using Vue.js and GitHub-Pages.
* Functionalities
  * Login with information: "API-URL", "User-Name", "Password"
  * All possible functionalities like "jjk" script with API.
* In "jjk" script, add option "Publish" to put downloadable "command.json" and "keymap.json" file in a public directory.
* Without login, user can see command reference and keymap.
* [FUTURE] "TODO" script functionalities
  * Make user role.
  * Assign projects to users.
  * User can only make changes to assigned projects/todos that he creates.
  * SuperAdmin can do anything.
  * Use Google-Drive API to upload attachments from website.

# "jjk" script

* "jjk" script getting bigger and more functionalities are coming.
* In project root, create folder "scripts" and place "common", "config", "rsgit", "rsdrive", "rssync", "rsrestore", "gist", "note", "todo", "dbsync", "dbackup", "pcsync", "cmd", "keymap" scripts in it.
  * In "common" script, add Bash-Table code.
  * In "jjk" (main) script
    * Add variable: `script_path=/c/ProgramData/snb/backup-n-sync/scripts`
    * Include/Source scripts: `source ${script_path}/common` [Do this for all scripts]
    * Copy jjk to executable PATH.
    * Check in both Windows-OS and Linux-OS, that existing functionalities are working.
* Currenty `./jjk todo`, `jjk pcsync`, `./jjk cmd` etc. are not working. Make it functional for all scripts.

# CmdRef

* Add one more field: "Command Argument"
* In command option list, do not show command name in every line. Instead show it in header.

# Keymap

* Add new script, named "Keymap" ["Keymap" name comes from "LunarVim GitHub - keymap.lua/keybinding.lua file"]
* Add keyboard-shortcuts of various program

# "CmdRef" and "Keymap"

* Add option "Publish" to put downloadable "command.json" and "keymap.json" file in a public directory.
* Make a general script named "cmdk" to download and get data from these "json" files. [Do not use "cmd", it is used in Windows-OS]
  * Use `./cmdk c` to execute/show commands.
  * Use `./cmdk k` to show keyboard-shortcuts of various programs.

# rsgit

* Archive (.tar.gz/.zip) project source code (or document) and upload to Google-Drive using rclone.

# rsrestore

* If project already exists on local-pc, then do not try to restore (git clone / from google-drive).
* During git repository restore, ask user to use git-clone or to restore from Google-Drive (if available).
* If user want to restore single project then show - which project is on local-pc and which is not.
* Also check database.
* Check "rsrestore" script in VirtualBox.
