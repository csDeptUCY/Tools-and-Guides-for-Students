# Development Environment: VS Code and Git

Throughout your studies at the Department of Computer Science, we recommend using Visual Studio Code (VS Code) as your main development environment for writing and running programs in Java, C, and Python (standard python files and Jupyter Notebooks).

VS Code is a lightweight, yet powerful general-purpose IDE widely used in both industry and academia. Through extensions, it provides code completion, debugging tools, version control integration, and project management capabilities.

In addition to programming, you will manage your code using Git, the most widely used version control system in software development, storing your repositories on GitHub. Using Git and GitHub will help you:

- Keep a record of your development progress

- Safely store your code online

- Work on different features without losing previous versions

- Share your work with instructors and collaborators

## Departmental Laboratories

The following tools are available in the Department of Computer Science laboratories:

- **Linux/UNIX laboratories (103, 101):** VS Code, JDK, GCC, Anaconda, Git

- **Windows laboratories (B103, B121, B123, 201):** VS Code, MinGW, JDK, Anaconda, Git

  You can start working immediately on any departmental machine without installing any additional software.

## Table of Contents

- [Departmental Laboratories](#departmental-laboratories)
- [1. VS Code Installation](#1-vs-code-installation)
- [2. VS Code & Java](#2-vs-code--java)
  - [Step 1: Install VS Code Java Extensions](#step-1--install-vs-code-java-extensions)
  - [Step 2: Install the JDK](#step-2--install-the-java-development-kit-jdk)
  - [Recommended Folder Structure](#recommended-folder-structure)
- [3. VS Code & C](#3-vs-code--c)
  - [Step 1: Install the C/C++ Extension](#step-1--install-vs-code-cc-extension)
  - [Step 2: Install GCC / MinGW](#step-2--install-the-gcc--mingw-compiler)
- [4. VS Code & Python / Jupyter Notebook](#4-vs-code--python--jupyter-notebook)
- [5. VS Code & Git](#5-vs-code--git)

# 1. VS Code Installation

To work on your personal computer, you need to download and install VS Code.

Download VS Code from: <https://code.visualstudio.com/download>

Choose the version appropriate for your operating system and follow the official installation guide for your platform:

- **Windows:** <https://code.visualstudio.com/docs/setup/windows>

- **macOS:** <https://code.visualstudio.com/docs/setup/mac>

- **Linux:** <https://code.visualstudio.com/docs/setup/linux>

After installation, open VS Code and install the appropriate extensions for your programming language using the Extensions Marketplace, as described in the relevant chapter below.

# 2. VS Code & Java

To develop Java programs using VS Code, you must have both VS Code and the Java Development Kit (JDK) installed. Follow the two steps below to set up your personal computer.

## Step 1 — Install VS Code Java Extensions

Open VS Code and install the Extension Pack for Java provided by Microsoft from the Extensions Marketplace. This extension pack provides tools for:

- Compiling and running Java programs

- Debugging Java applications

- Code completion and navigation

- Testing support

## Step 2 — Install the Java Development Kit (JDK)

Install a recent Long Term Support (LTS) version of the JDK provided by Oracle from <https://www.oracle.com/europe/java/technologies/downloads/>

Choose the installer for your operating system and follow the installation instructions. After installation, verify that Java is correctly installed by opening a terminal and running:

```console
java -version
javac -version
```

If successful, both commands will display the installed Java version. The first confirms the runtime (JRE), the second confirms the compiler (JDK). Once the JDK is installed, VS Code will automatically detect it.

## Recommended Folder Structure

Organise your work as follows to avoid issues with the Java extension:

1.  Create a workspace folder (e.g., EPL131/) as the root for all your projects.

2.  Inside it, create one folder per lab or assignment:

```text
EPL131/
├── Labs/
│   ├── Lab1/
│   ├── Lab2/
│   └── Lab3/
└── Assignments/
    ├── Assignment1/
    └── Assignment2/
```

3.  Open only the specific lab folder in VS Code, do not open the root EPL131 folder. This prevents the Java extension from generating an unwanted project structure.

4.  Create your .java files directly inside the lab folder:

```text
Lab1/
├── Hello.java
└── Exercise1.java
```

5.  Do not use package statements in your programs:

```java
public class Hello {
    public static void main(String[] args) {
        System.out.println("Hello World");
    }
}
```

6.  Compile and run the program. You can use the Run button in VS Code, or open the integrated terminal and run:

```console
javac Hello.java # compile
java Hello       # run
```

# 3. VS Code & C

The GNU Compiler Collection (GCC) is commonly used to compile C programs in Linux. Unlike Linux, macOS and Windows do not include GCC by default. In macOS, GCC can be installed, whereas in Windows there is MinGW as alternative solution. Follow the steps below to set up your personal computer.

## Step 1 — Install VS Code C/C++ Extension

Open VS Code and install the C/C++ Extension (not necessarily the full C/C++ Extension Pack) from the Extensions Marketplace. This extension provides tools for:

- Code completion and intelligent suggestions

- Debugging tools

- Code navigation and error detection

- Integration with compilers such as GCC or Clang

## Step 2 — Install the GCC / MinGW Compiler

**macOS** users:

1.  Install Homebrew. Open the Terminal (via Spotlight or Launchpad) and run:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

2.  Install GCC:

```bash
brew install gcc
```

3.  Confirm the installation:

```console
gcc --version
```

**Windows** users:

Since GCC is not available for Windows machines, there are two alternative options:

**A) Use GCC which can be installed in WSL (Windows Subsystem for Linux):**

The recommended approach for Windows is to install WSL, which provides a Linux environment inside Windows identical to the departmental Linux labs.

1.  Launch Windows PowerShell as Administrator and run:

```powershell
wsl --install
```

This enables WSL and automatically downloads and installs Ubuntu. At the end, create a new Linux user (username and password).

2.  Open VS Code and install the WSL extension from the Extensions Marketplace. This allows VS Code to open folders inside the Ubuntu environment and use Linux tools.

3.  Connect VS Code to the Ubuntu environment. Click the 'Open a remote window' button (\>\<) in the bottom-left corner of VS Code, then select Connect to WSL. After a successful connection, the bottom-left will show: WSL: Ubuntu.

4.  Launch the Ubuntu terminal inside VS Code (Terminal → New Terminal) and install GCC:

```bash
sudo apt update
sudo apt install build-essential
```

The `build-essential` package installs GCC, the C/C++ compiler, and essential development tools.

5.  Verify the installation:

```console
gcc --version
```

**B) Use MinGW:**

An alternative solution for Windows is the installation of MinGW (Minimalist GNU for Windows). Usually, it includes:

- gcc → compiler for C

- g++ → compiler for C++

- gdb → debugger

- make / mingw32-make → build tool

- basic libraries and headers for Windows

You can follow the guidelines found [here](https://code.visualstudio.com/docs/cpp/config-mingw) to download, install and use MinGW with VSCode. MinGW is also available in all workstations in departmental Windows labs.

**C) Use GCC which is installed on departmental Linux labs.**

You can install [Remote – SSH](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-ssh) VSCode extension and then connect remotely (if you are not connected to CS network via ethernet or CS WiFi you need to connect to CS VPN in advance) to any machine of lab 103 (103wsX.in.cs.ucy.ac.cy) or lab B103 (b103wsX.in.cs.ucy.ac.cy) where X is an integer number from 1 to 30.

Go to VSCode Extensions and search for Remote – SSH, and install it.

![Installing the Remote SSH extension](media/images/image1.png)

Go to the Remote – SSH tab (red square in the following figure), and in SSH, click on + to add a new remote connection as for example:

```console
ssh username@b103wsX.in.cs.ucy.ac.cy
```

where username is your username (provided by the university) and X is the number of the remote host you want to connect to.

![Adding a new remote SSH connection](media/images/image2.png)

Press enter to proceed, and then again enter to save the connection to the ssh config file. The new connection will be made available under SSH. Click on the arrow to initiate the connection to the remote host.

![Selecting the remote SSH connection](media/images/image3.png)

When you are asked to choose the operating system of the remote host, select Linux and then enter.

![Selecting Linux as the remote operating system](media/images/image4.png)

The remote host presents its public key fingerprint and asks if you want to continue. Click "Continue" and the fingerprint is stored in your known_hosts file. Future connections will not ask again unless the remote host key changes.

![Confirming the remote host public key fingerprint](media/images/image5.png)

Next, you will be asked to provide your password (given by the university)

![Entering the remote account password](media/images/image6.png)

In the next figure you can see the VS Code Remote SSH status indicator in the bottom-left corner. This means that VS Code is currently connected to the remote Linux machine b103ws5.in.cs.ucy.ac.cy through SSH.

![Active VS Code Remote SSH connection](media/images/image7.png)

Finally, you need to go to the Explorer tab and "Open Folder" on the remote host. If you choose to open a folder that does not exist, it will be automatically created.

![Opening a folder on the remote host](media/images/image8.png)

When you want to disconnect from the remote host, click on the status indicator (bottom left corner) and click on "Close Remote Connection".

## Recommended Folder Structure

Follow the same organisational approach as for Java:

1.  Create a workspace folder (e.g., EPL232/).

2.  Create one folder per lab or assignment:

```text
EPL232/
├── Labs/
│   ├── Lab1/
│   └── Lab2/
└── Assignments/
    └── Assignment1/
```

3.  Open only the specific lab folder in VS Code.

4.  Create your .c files inside the lab folder:

```text
Lab1/
├── hello.c
└── exercise1.c
```

5.  Open the integrated terminal in VS Code, compile and run:

```console
gcc hello.c -o hello # compile
./hello              # run (Linux / macOS / WSL)
```

# 4. VS Code & Python / Jupyter Notebook

For Python programming and working with Jupyter Notebooks, we recommend installing Anaconda, a widely used Python distribution that includes the Python interpreter, many scientific libraries, Jupyter support, and the Conda package manager.

## Step 1 — Install VS Code Python Extensions

Open VS Code and install the following extensions from the Extensions Marketplace:

- **Python extension for VS Code** (by Microsoft)

- **Jupyter extension for VS Code** (by Microsoft)

These extensions provide code completion, syntax highlighting, debugging, execution of Python scripts, and the ability to create and run Jupyter Notebooks (.ipynb files) directly inside VS Code.

## Step 2 — Install Anaconda

- **Download:** <https://www.anaconda.com/download/success>

Choose the version for your operating system and follow the installation instructions. The installation includes the Python interpreter, Jupyter Notebook environment, Conda package manager, and many commonly used data science libraries.

- **Jupyter Notebooks in VS Code (usage examples):** <https://code.visualstudio.com/docs/datascience/jupyter-notebooks>

## Step 3 — Select the Python Interpreter in VS Code

After installing Anaconda, you must tell VS Code which Python interpreter to use. Without this step, VS Code may use a system Python instead of Anaconda, causing missing libraries.

1.  Open the Command Palette: Ctrl+Shift+P (Windows/Linux) or Cmd+Shift+P (macOS).

2.  Type and select: Python: Select Interpreter

3.  Choose the Anaconda Python entry (it will include 'anaconda' or 'conda' in the path, e.g., ~/anaconda3/bin/python).

    **NOTE:** You may need to repeat this step each time you open a new project folder in VS Code.

## Recommended Folder Structure

Organise your Python and Jupyter work as follows:

1.  Create a workspace folder (e.g., EPL335/) and one folder per lab or project:

```text
EPL335/
├── Labs/
│   ├── Lab1/
│   └── Lab2/
└── Assignments/
    └── Assignment1/
```

2.  Open only the specific lab folder in VS Code.

3.  Create your .py and .ipynb files directly inside the lab folder:

```text
Lab1/
├── analysis.ipynb
└── utils.py
```

4.  Run Python scripts using the Run button or the integrated terminal:

```console
python script.py
```

5.  Open and run Jupyter Notebooks (.ipynb) directly in VS Code by clicking on the file.

# 5. VS Code & Git

Version control is an essential tool for managing source code and tracking changes during software development. VS Code includes built-in Git integration, allowing you to perform common version control operations directly from the editor.

## 5.1 Installing Git on Your Personal Computer

To use Git on your personal computer, download and install Git:

- **Windows:** Download and install from <https://git-scm.com/download/win>

- **macOS:** Download from <https://git-scm.com/download/mac> or install via Homebrew: brew install git

- **Linux (Ubuntu/Debian):** sudo apt update && sudo apt install git

Full installation instructions for all platforms: <https://git-scm.com/book/en/v2/Getting-Started-Installing-Git>

## 5.2 Initial Git Configuration

Before using Git, you must configure it with your name and email address. These details identify the author of each commit. This configuration is required on both departmental and personal computers.

Open a terminal (departmental labs: any terminal; personal computer: Command Prompt / PowerShell / Git Bash on Windows, or Terminal on macOS/Linux) and run:

```console
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

**NOTE:** On departmental Linux labs, your home directory is shared across all workstations. The .gitconfig file created by these commands will be available on any lab machine you log into.

## 5.3 Using Git in VS Code

Once Git is installed, VS Code automatically detects it. You can manage version control from the Source Control panel (Ctrl+Shift+G). Typical operations include:

- **Clone:** Download a remote repository (e.g., from GitHub) to your local machine.

- **Stage:** Select which changed files to include in the next commit.

- **Commit:** Record a snapshot of your staged changes locally, with a descriptive message.

- **Push:** Upload your local commits to the remote repository on GitHub.

- **Pull:** Download and integrate changes from the remote repository.

- **View history:** Browse file history and compare differences between versions.

More information: <https://code.visualstudio.com/docs/sourcecontrol/overview>

## 5.4 Working with GitHub Classroom

Your assignments will be distributed using GitHub Classroom. The typical workflow for each assignment is:

1.  Open the assignment invitation link provided by your instructor. Login to GitHub with your credentials and choose your identifier.

2.  Accept the assignment. GitHub Classroom will automatically create a personal repository for you. In case of a **<u>Repository Access Issue</u>**, check your email for an assignment acceptance invitation and open the link provided to create the repository.

3.  After you gain access to your assignment, click on the green button and copy the repository URL.

4.  Clone the repository to your local machine. In VS Code, open the Command Palette (Ctrl+Shift+P), select Git: Clone, and paste the repository URL. Choose a local folder to save it.

5.  Work on your assignment inside the cloned folder. Use the standard Git workflow: Stage → Commit → Push.

6.  Push your work to GitHub regularly. Your instructor will see your latest pushed commits.

    **NOTE:** Always use your personal GitHub account so that your contributions are correctly attributed in the commit history.

## 5.5 Working with .gitignore

Not all files in a project should be tracked by Git. Compiled binaries, temporary files, and IDE-specific configuration files are typically generated automatically and do not need to be stored in a repository. To prevent Git from tracking such files, create a file named .gitignore in the root folder of your project.

- **Java projects:**

```gitignore
# Compiled class files and build artifacts
*.class
*.jar
*.war

# Build output directories
target/
bin/

# macOS metadata
.DS_Store

# VS Code workspace settings
.vscode/settings.json
```

- **C projects:**

```gitignore
# Compiled object files and executables
*.o
*.out
*.exe
a.out

# macOS metadata
.DS_Store

# VS Code workspace settings
.vscode/settings.json
```

- **Python projects:**

```gitignore
# Bytecode cache
__pycache__/
*.pyc
*.pyo

# Jupyter Notebook checkpoints
.ipynb_checkpoints/

# macOS metadata
.DS_Store

# VS Code workspace settings
.vscode/settings.json
```

A complete collection of .gitignore templates: <https://github.com/github/gitignore>

## 5.6 Best Practices

For detailed best practices on commit messages, branching strategies, code review, and assessment criteria, refer to the **GitHub Best Practices Guide**.

Key reminders:

- Commit frequently with descriptive messages; every completed change deserves its own commit.

- Pull before you start, push as soon as you finish.

- Do not leave your work until the last minute, consistent progress avoids deadline panic.

- Communicate with your team so that you do not work on the same files simultaneously.

- Never commit sensitive information (passwords, API keys).

If you have followed the instructions in this guide and still encounter issues, ask the instructors or the lab assistants.
