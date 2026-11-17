# Mission 4 - How programs run

## 1. Task / objective

Create and run a one-line Python program, then compare a compiler and an interpreter.

## 2. Work completed

I created `hello.py` with `print("Hello from Python")`. Running `python3 hello.py` printed:

```text
Hello from Python
```

| Point | Compiler | Interpreter |
| --- | --- | --- |
| When translation or execution happens | Translates the source before the finished program runs. | Reads and executes the program at runtime. |
| Typical output | A compiled program or executable. | The result of running the program. |
| One example | Clang compiling a C program. | Python 3 running `hello.py`. |
| One advantage | The compiled program can be run again without compiling it each time. | I can change a short script and run it again without a separate build step. |

## 3. Commands / tools used

| Command or tool | Purpose |
| --- | --- |
| `python3 hello.py` | Run the Python file. |
| `python3 --version` | Check the Python version, 3.9.6. |
| `clang --version` | Confirm that Clang is available as a compiler example. I did not compile a C file for this mission. |
| `git add`, `git commit`, `git push` | Stage, save and publish the completed mission. |

## 4. My understanding

A compiler translates the code into an executable before it runs, so the finished program can often run faster. An interpreter runs the code at runtime instead of making a separate executable first. Because Python shows the line where an error happened, I find it easier to debug a short script and run it again after changing it.

## 5. Difficulties faced

I mistakenly created a folder ending in `.py` at first. That confused me because Python needed a file to run.

## 6. How I resolved them

I created `hello.py` as a file inside this mission folder and ran it with `python3 hello.py`. It printed the expected message.

## 7. Evidence / files

The `hello.py` file and its observed output are recorded here with the comparison table.

## 8. Commit details

Commit message: `Compare compilers and interpreters`. Pushed to GitHub on the `main` branch.
