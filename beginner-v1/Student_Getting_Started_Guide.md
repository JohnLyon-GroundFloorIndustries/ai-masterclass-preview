# Getting started with real execution

## What you are installing

Python is the program that reads `.py` instructions and performs them. The terminal is where you ask Python to run a file. A package is reusable software; a package manager installs packages. These labs need no extra packages. A virtual environment is a project-specific Python environment; it becomes useful when you add dependencies, but is not required for the baseline.

## Windows

1. Visit [Python downloads](https://www.python.org/downloads/) and follow the official [Windows installation guide](https://docs.python.org/3/using/windows.html). Current official guidance provides the Python install manager. Install it from the official page or Microsoft Store, then install a supported Python 3 runtime if prompted. Existing Python 3.10+ installations can be used.
2. Open Start, type `PowerShell`, and open it. This is a command interface; you do not need administrator mode for running the labs.
3. Type `python --version` and press Enter. Expect `Python 3.x.x`, where the version is at least 3.10. If `python` is unavailable, try `py --version`; if `py` works, use `py` instead of `python` in the lab commands.
4. If neither works, close and reopen the terminal after installation. Follow the official troubleshooting page rather than editing random system settings. A store shortcut is not proof that a runtime is installed.
5. In File Explorer, extract the lab ZIP. Open the extracted folder containing `hello.py`. Click the address bar and copy its full path.
6. In PowerShell type `cd "C:\your\actual\lab-folder"`, replacing the example path with the copied folder path. Quotes keep spaces together. `cd` means change directory. Type `dir` to list files; confirm `hello.py` is listed.
7. Type `python hello.py`. Do not type a leading `>` or the terminal's existing prompt.

## macOS

1. Visit [Python macOS downloads](https://www.python.org/downloads/macos/) and select a supported Python 3 installer for your machine. Open the `.pkg`, follow the installer steps, and follow its certificate setup instructions. See the [official macOS guide](https://docs.python.org/3/using/mac.html).
2. Open Finder → Applications → Utilities → Terminal. Type `python3 --version`. Expect Python 3.10 or later; use `python3` for all course commands.
3. Double-click the lab ZIP to extract. In Terminal type `cd `, drag the extracted folder into the terminal to insert its path, then press Enter. Alternatively type `cd "/your/actual/lab-folder"`.
4. Type `ls` and confirm `hello.py` is listed. Run `python3 hello.py`.
5. If the command is missing, reopen Terminal and confirm the installer finished. Do not remove the operating system's Python components.

## Linux

1. Open Terminal from your desktop application menu. Run `python3 --version`. Many distributions already include Python.
2. If absent, use your distribution's official package instructions. For Debian/Ubuntu: `sudo apt update` then `sudo apt install python3 python3-venv`. `sudo` asks to perform an administrative operation; review the package list before accepting. Other distributions use different package managers, so do not assume `apt` applies.
3. Extract the ZIP with the archive manager. Run `cd "/your/actual/lab-folder"`, then `ls`, then `python3 hello.py`.

## Expected first output

```text
Hello, learner
1 Read policy
2 Draft response
Ready: 2 tasks
```

The line `name = "learner"` stores text under a name. `tasks = [...]` creates a list. `def greeting(person):` defines a function with one input. Its indented `return` gives text back. `print(greeting(name))` calls the function and displays the answer. `enumerate` pairs each task with a number. The `for` loop visits each pair. `len(tasks)` counts the list. `if ... > 0` chooses a branch; `else` handles an empty list. Change one value, predict output, save, then rerun.

## Running two terminals for the API exercise

In terminal A, enter the lab folder and run `python mock_api.py`. It will stay running; that is expected. In terminal B, enter the same folder and run `python api_client.py`. Expect `status 200` and `total 12`. The address `127.0.0.1` means this computer; `8766` is the service port. Stop terminal A with Ctrl+C when finished. Use `python3` on macOS/Linux.

The client imports JSON conversion and HTTP helpers, creates a dictionary with two numbers, converts it to JSON bytes, prepares a POST request, waits at most three seconds and displays the response. Its exception handler turns a connection error into a useful instruction. Change `5` to `8`; expect total 15. Change it to `"eight"`; expect an HTTP 400 rejection, not a calculation.

## Errors are information

| Symptom | Likely cause | Next action |
|---|---|---|
| Command not recognized/not found | Interpreter unavailable in this terminal | Verify installation; reopen terminal; try the OS-specific command |
| Cannot open file | Wrong folder or filename | List files; check extraction and `.py` versus `.py.txt` |
| SyntaxError | Python cannot parse a line | Check the named line and punctuation; compare to original |
| IndentationError | Misaligned block | Use four spaces consistently for the shown block |
| NameError | Name not defined | Check spelling and assignment order |
| Connection refused | Local server not running | Start it in terminal A; keep it running |
| Address already in use | Another process uses the port | Stop your earlier lab server with Ctrl+C; do not kill unknown processes |
| PermissionError in approval exercise | Expected boundary or expired approval | Inspect tenant, exact content and reviewer; do not bypass the check |

## Optional dependency isolation

Only when adding third-party packages: run `python -m venv .venv`. This creates a project environment. On Windows you can call `.venv\Scripts\python.exe` directly; on macOS/Linux call `.venv/bin/python`. This avoids needing activation or changing execution policy. Run that interpreter with `-m pip install package-name` only after choosing a documented package and version. Record tested versions in a dependency file. Never paste an API key into source code or this course page.

## Optional paid model/cloud work

The baseline requires no account or credentials. A real provider exercise is separate: review data handling, select a supported API/model from official documentation, understand billing units, create a restricted server-side credential, set application request/step budgets and provider limits, and test with fictional data. Environment variables are named settings passed to a process; a secrets manager is preferred for deployed services. Do not commit `.env` files, put secrets in HTML or assume a ChatGPT subscription automatically covers every API charge. Billing and plan availability must be checked for your actual account. No paid resources are provisioned by this kit.
