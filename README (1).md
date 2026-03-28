# The Open Source Audit: Apache HTTP Server

This repository contains a suite of 5 Bash shell scripts developed for the university capstone project **"The Open Source Audit"** with a focus on **Apache HTTP Server (apache2)**. The project demonstrates core Linux administration concepts through shell scripting.

## Project Details
- **Author:** Jyotasana
- **Course:** Open Source Software
- **Software Audited:** Apache HTTP Server (Apache License 2.0)
- **Audit Results:** Available in [output/output.md](output/output.md)
- **Host Environment:** Ubuntu/Debian Linux

## Script Descriptions

1.  **01_sys_identity.sh**: Generates a system identity report including OS details, kernel version, and Apache audit context.
2.  **02_pkg_inspector.sh**: Checks for the installation of the `apache2` package and provides philosophy notes for the LAMP stack.
3.  **03_dir_audit.sh**: Audits permissions and disk usage for critical Apache-related directories like `/etc/apache2`.
4.  **04_log_analyzer.sh**: Analyzes log files (or generates a dummy access log) to count occurrences of specific keywords or status codes like `404`.
5.  **05_manifesto_gen.sh**: An interactive script that gathers user input to generate a personalized "Open Source Manifesto."

## Audit Results

Professional terminal screenshots of all script outputs have been generated and are stored in the `output/` directory.

- **View Report**: [output.md](output/output.md)
- **Format**: High-fidelity terminal simulations (SVG)
- **Verified User:** Jyotasana

## Getting Started

### 1. Make Scripts Executable
Before running the scripts, you must give them execution permissions using the `chmod` command. Open your terminal in the repository directory and run:

```bash
chmod +x 01_sys_identity.sh 02_pkg_inspector.sh 03_dir_audit.sh 04_log_analyzer.sh 05_manifesto_gen.sh
```

Alternatively, you can make all `.sh` files executable at once:
```bash
chmod +x *.sh
```

### 2. Running the Scripts
Run each script by prefixing the filename with `./`:

```bash
# System Identity
./01_sys_identity.sh

# Package Inspector
./02_pkg_inspector.sh

# Directory Audit
./03_dir_audit.sh

# Log Analyzer (Optional: pass a file and keyword)
./04_log_analyzer.sh access.log 404

# Manifesto Generator
./05_manifesto_gen.sh
```

## Windows Setup

Since these scripts are designed for Linux, they will not run directly in Windows PowerShell or Command Prompt. Windows users can follow these steps to set up a compatible environment. You can find more details in the sections below.

### Option 1: Windows Subsystem for Linux (WSL) - Recommended
WSL allows you to run a full Ubuntu terminal alongside your Windows applications.

1.  **Install WSL**: Open PowerShell as Administrator and run:
    ```powershell
    wsl --install
    ```
2.  **Restart your computer** if prompted.
3.  **Open Ubuntu**: Search for "Ubuntu" in the Start menu.
4.  **Navigate to the project**: Use `cd` to go to your project directory (e.g., `cd /mnt/c/Users/YourName/Documents/Linux-Chotu`).
5.  **Run the scripts**: Follow the [Running the Scripts](#2-running-the-scripts) section above.

### Option 2: Git Bash
If you have Git installed, you likely already have Git Bash.

1.  **Open Git Bash**: Right-click in the project folder and select "Git Bash Here".
2.  **Run the scripts**: Git Bash provides a MinGW environment that can execute Bash scripts.
    ```bash
    ./01_sys_identity.sh
    ```

---

## Features Demonstrated
- **Variables & Command Substitution**
- **Conditionals (if-then-else, case statements)**
- **Loops (for, while read)**
- **File I/O (Redirects, Appending, Here-docs)**
- **System Commands (`dpkg`, `ls`, `du`, `grep`, `awk`)**
- **Interactive User Input**

## License
Host OS: GPL | Scripts: MIT | Audit Focus: Apache License 2.0
