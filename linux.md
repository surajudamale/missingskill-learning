# <span style = "color:red"> LINUX </span>

#### Basic Information about Linux Environment

- Linux is a free, open-source operating system. All of Digital Ocean’s offered operating systems are Linux distributions.
- Linux has been under active development since 1991. It has evolved to be versatile and is used all over the world, from web servers to cellphones.
- Digital Ocean offers Linux distributions on droplets because Linux is free and easy to use.
- However, newcomers to Linux may find it difficult to approach the structure of an unfamiliar operating system.
  This guide gently introduces key terminal skills and equips newcomers to learn more about Linux.

---

#### The Terminal

- For most of the time you access a cloud server, you’ll be doing it through a terminal shell. The shell allows you to execute commands on the droplet.
- All administrative tasks can be accomplished through the terminal. This includes file manipulation, package - installation, and user management.
- The terminal is interactive. You specify commands to run. The terminal outputs the results of those commands. Executing any command is done by typing it and pressing Enter.

---

#### Navigation (Linux Command)

| Commands                      | Description                                                                                                                    |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| Pwd (print working directory) | To see what directory, you are currently active dir.                                                                           |
| ls                            | To see other files and directories that exist in your current working directory.                                               |
| cd <name of directory>        | To navigate into a directory.                                                                                                  |
| mkdir                         | It uses to make directory in local.                                                                                            |
| rmdir                         | It removes the directory.                                                                                                      |
| rm                            | Which removes file and directory.                                                                                              |
| cp                            | Copy file from one location to another.                                                                                        |
| mv                            | Move file from one location to other or rename the same file.                                                                  |
| who                           | Display the persons who are logged into the current system.                                                                    |
| whoami                        | Display the current logged in user.                                                                                            |
| history                       | Display the history of command that are used in terminal.                                                                      |
| ping                          | To check the internet connection.                                                                                              |
| which                         | Which command gives you the location of various commands paths.                                                                |
| echo                          | Display the terminal whatever is passed.                                                                                       |
| ps                            | Display all running processes.                                                                                                 |
| top                           | Paginating the document/file.                                                                                                  |
| tail                          | Display the live file updates. ex. tail -100F <file-name>                                                                      |
| ltrhf                         | show files and folders in human readable format this will display everything including file type.                              |
| Chmod                         | To protect and secure files and directories in linux we use permissions to control what users can do with a file or directory. |

---

#### Linux System Information:

| Root File system (RFS)             | Information                                                                                 |
| ---------------------------------- | ------------------------------------------------------------------------------------------- |
| /(Root)                            | - Every single file and directory starts from root directory, Entry point for Linux system. |
| /boot - boot loader files          | Entry point for Linux system.                                                               |
| /home - home directory             | users home folders are stored here.                                                         |
| /root                              | home folders for root users.                                                                |
| /sbin - System binaries            | System commands.                                                                            |
| /bin - User binaries               | Contains binary executables.                                                                |
| /var - Variable files              | Non critical files.                                                                         |
| /etc - Configiration Files         | System and application configuration.                                                       |
| /opt - Optional add-on application | Optional root folders.                                                                      |
| /usr - User Program                | Non system application is stored here.                                                      |
| /dev - Devicde file                | Hardware / Firmware are stored here.                                                        |
| /mnt - Mount Directory             | External hard drive or devices are mounted here.                                            |
| /srv - Service Data                | srv stands for Service. Contains server specific services related data.                     |
| / proc - process Information       | Contains information about System Process.                                                  |
| /media                             | used for monitoring cd-drive.                                                               |
