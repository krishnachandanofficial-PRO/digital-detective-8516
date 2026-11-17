# Mission 2 - Terminal and file management

## 1. Task / objective

Use Terminal to inspect the repository, practise creating and changing files, compare command options and pipes, and check the installed package manager.

## 2. Work completed

### Command reference

| Operation | Command used | What it does | What I observed |
| --- | --- | --- | --- |
| Current directory | `pwd` | Displays the current folder path. | The path ended in `digital-detective-8516` when I was in the repository. |
| Directory listing | `ls` | Lists the visible items in the folder. | It showed `README.md` and the mission folders. |
| Detailed listing | `ls -l` | Lists more information about each item. | It showed permissions, owner, size and date columns. |
| Change directory | `cd ..` and `cd digital-detective-8516` | Moves to the parent folder and then back to the repository. | The path changed to the parent, then ended in `digital-detective-8516` again. |
| Create directory | `mkdir terminal-practice` | Creates a folder. | `terminal-practice` appeared in the repository. |
| Create empty file | `touch terminal-practice/empty.txt` | Creates an empty file. | `empty.txt` had a size of 0 bytes. |
| Copy file | `cp terminal-practice/empty.txt terminal-practice/empty-copy.txt` | Makes another file with the same contents. | There were two empty files before the copy was renamed. |
| Rename file | `mv terminal-practice/empty-copy.txt terminal-practice/renamed-empty.txt` | Changes the copied file's name. | `renamed-empty.txt` appeared and `empty-copy.txt` disappeared. |
| Display contents | `cat terminal-practice/empty.txt` | Prints the file's contents. | Nothing was printed because the file was empty. |

### File-change practice

Inside `terminal-practice`, I wrote one line to `notes.txt` using `>` and added a second line using `>>`. `cat` showed both lines:

```text
I typed code in VS Code.
I saved the file on my computer.
```

I copied it to `notes-copy.txt` and renamed that copy to `notes-backup.txt`. Both `notes.txt` and `notes-backup.txt` contain the same two lines.

### Flags and pipes

I compared `ls` with `ls -lah` in the repository. The normal listing showed the visible files and folders. The detailed listing also showed hidden `.git` and `.gitignore`, permissions, sizes such as `29B` for `.gitignore`, and dates. I did not copy the owner name into this README. `ls -lah | head -n 5` displayed only the first five lines of that listing.

### Package manager check

Homebrew is installed. `brew --version` displayed `Homebrew 7.0.13`. `brew list` showed 68 entries; some of the listed packages were `git`, `gh` and `ffmpeg`. I did not install or remove any package for this mission.

## 3. Commands / tools used

The command reference above records the file and directory commands. I also used `ls -lah` to show hidden files and readable sizes, `head -n 5` to show the first five lines, `brew --version` to check Homebrew and `brew list` to see its packages. I used `git add`, `git commit` and `git push` to stage, save and publish the mission.

## 4. My understanding

Replacing with `>` overwrites all existing content, while `>>` appends new text to the bottom. Copying with `cp` creates a duplicate. Moving with `mv` transfers a file to a new location and removes the original path; in my practice I used it to rename a copy in the same folder.

`ls` lists visible files, while `ls -lah` also shows hidden files with detailed permissions and sizes. The `-l` flag adds the details, `-a` includes hidden files and `-h` makes sizes easier to read. The `|` sends the detailed listing to `head -n 5`, so I only see its first five lines.

`pwd` outputs my current path, showing exactly where I am in the filesystem. `ls` is useful because it shows the files and folders available in that directory. Homebrew helps me use other commands and tools, which makes bigger tasks easier. It manages packages so I can get, update or remove those tools from one place.

## 5. Difficulties faced

No major difficulty.

## 6. How I resolved them

Not applicable.

## 7. Evidence / files

The command table and safe observations are in this README. The practice files are in `terminal-practice/`.

## 8. Commit details

Commit message: `Complete Terminal and file management mission`. Pushed to GitHub on the `main` branch.
