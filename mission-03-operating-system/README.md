# Mission 3 - Operating system, processes and permissions

## 1. Task / objective

Check the operating system, account, storage and process activity. Look at paths and file permissions, then explain the main jobs of an operating system.

## 2. Work completed

### System observations

| Information checked | What it tells me | Privacy-safe observation |
| --- | --- | --- |
| Operating system | Which OS runs this computer | `sw_vers` showed macOS 26.6.2; `uname -s` showed Darwin. |
| Current account | Which local account runs the commands | `whoami` returned `[redacted]`. |
| Storage | Capacity, space used and space available for this location | `df -h .` showed 926 GiB total, 108 GiB used and 791 GiB available. |
| Activity snapshot | How many processes were active at that moment | `top` showed 550 processes: 2 running and 548 sleeping. |

### Processes

I checked the process list with `ps` and looked up app PIDs with `pgrep`. At the time of the check, Safari had PID `53838`, Google Chrome had PID `85122` and VS Code had PID `51371`. These numbers can change when apps restart. `launchd` was another process in the list with PID `1`.

### Paths and permissions

The current location shown by `pwd` ended in `digital-detective-8516` from the repository root. After `cd mission-03-operating-system`, it ended in `digital-detective-8516/mission-03-operating-system`. I returned with `cd ..`.

An absolute-path example, with private parts hidden, is `/Users/[redacted]/Documents/[redacted]/[redacted]/digital-detective-8516/terminal-practice/notes.txt`. From the repository root, the relative path to that file is `terminal-practice/notes.txt`.

`ls -l terminal-practice/notes.txt` showed the permission string `-rw-r--r--@`. The owner has `r` and `w`, so the owner can read and change the file. There is no owner `x`, so this text file is not marked executable. The `@` shows that macOS has extended attributes for this file. I did not change any system permission.

### Operating system responsibilities

| OS responsibility | My explanation | Example |
| --- | --- | --- |
| Process management | The OS gives CPU time to running programs so they can work alongside each other. | VS Code and Google Chrome can be open at the same time. |
| Memory management | It allocates RAM to programs while they run. | The code I am editing in VS Code is kept in memory until I save it. |
| Device management | It uses drivers to communicate with hardware. | The keyboard works with the program I am typing in. |
| File management | It organizes files into a structured file system. | `terminal-practice/notes.txt` is in a folder inside this repository. |
| User interface / shell | It provides a GUI or Terminal so I can interact with the computer. | I used Terminal to run `pwd`. |
| Security and permissions | It checks who can read, write or execute a file. | The owner of `notes.txt` has `rw-` permission. |

## 3. Commands / tools used

| Command | Purpose |
| --- | --- |
| `sw_vers` and `uname -s` | Check the OS name and version. |
| `whoami` | Check the current local account, then redact it in this README. |
| `df -h .` | Check storage for the current location in readable units. |
| `top` | Take a brief snapshot of system activity. |
| `ps` and `pgrep` | Inspect running processes and identify app PIDs. |
| `pwd` and `cd` | Check how the current location changes between folders. |
| `ls -l` | Read the permission letters for a practice file. |
| `git add`, `git commit`, `git push` | Stage, save and publish the completed mission. |

## 4. My understanding

A running process is a program currently working in the system. A PID uniquely identifies one active process. The process snapshot showed that many programs and background tasks can exist at the same time.

An absolute path gives the full location starting from the root directory. A relative path is based on my current working directory. I could see this when `pwd` changed after I moved into the Mission 3 folder.

The OS is the middleman between programs and hardware. It allocates RAM and CPU time, talks to devices through drivers, organizes files, gives us a Terminal or GUI, and checks file permissions.

## 5. Difficulties faced

No major difficulty.

## 6. How I resolved them

Not applicable.

## 7. Evidence / files

This README contains privacy-safe observations, path examples and permission details. The file inspected is `terminal-practice/notes.txt`.

## 8. Commit details

Commit message: `Document operating system and file management`. Pushed to GitHub on the `main` branch.
