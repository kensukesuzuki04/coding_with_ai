# Pre-Course Preparation Guide

> **Course Use**
> This setup guide is prepared for Clark University Economics Department courses `ECON206` and `ECON10`.
>
> **Document Preparation**
> This README was prepared with GitHub Copilot under Professor Suzuki's instruction and revision.

This guide is for students to complete **before class**.

The goal is to make sure everyone arrives with the required software installed so that, during class, we can focus on running the code, installing Python packages, seeing errors, and fixing them.

## Table of Contents

- [What You Need to Install Before Class](#what-you-need-to-install-before-class)
- [1. Create a GitHub Account and Activate Copilot Student Access](#1-create-a-github-account-and-activate-copilot-student-access)
- [2. Install Visual Studio Code](#2-install-visual-studio-code)
- [3. Install Python](#3-install-python)
- [4. Install Quarto](#4-install-quarto)
- [5. Install a PDF Engine for Quarto](#5-install-a-pdf-engine-for-quarto)
- [6. Install VS Code Extensions](#6-install-vs-code-extensions)
- [7. Confirm Everything Works](#7-confirm-everything-works)
- [8. What Not to Install Yet](#8-what-not-to-install-yet)
- [9. What We Will Do in Class](#9-what-we-will-do-in-class)
- [10. Troubleshooting Before Class](#10-troubleshooting-before-class)
- [11. Recommended Folder Setup](#11-recommended-folder-setup)
- [12. Checklist](#12-checklist)

## What You Need to Install Before Class

Please install the following applications before class:

1. **Visual Studio Code**
2. **Python**
3. **Quarto**
4. **A PDF engine for Quarto**

Do **not** install project-specific Python packages yet. We will do that in class.

---

## 1. Create a GitHub Account and Activate Copilot Student Access

Please complete this step first.
Approval for student access may take time, so it is better to begin early.

Before class, create a GitHub account if you do not already have one.

Sign up:

- https://github.com/signup

If you are eligible for GitHub Student Developer Pack benefits, apply here:

- https://education.github.com/pack

After your student benefits are approved, activate GitHub Copilot through your GitHub account.

Copilot information:

- https://github.com/features/copilot

What to do:

1. Create or sign in to your GitHub account.
2. Apply for the GitHub Student Developer Pack if you are eligible.
3. Confirm that GitHub Copilot is available on your account.
4. In VS Code, sign in with that GitHub account when prompted.

---

## 2. Install Visual Studio Code

Download:

- https://code.visualstudio.com/download

What to do:

1. Download the version for your operating system.
2. Run the installer.
3. During installation on Windows, it is helpful to enable:
   - Add to PATH
   - Open with Code
   - Register Code as an editor for supported file types

![VS Code installer — "Select Additional Tasks" screen. Make sure "Add to PATH (requires shell restart)" is checked.](https://education.launchcode.org/lchs/_images/win-vscode-install.png)

After installation, open VS Code once to make sure it starts normally.

---

## 3. Install Python

Download:

- https://www.python.org/downloads/

What to do:

**On Windows:**

1. Go to https://www.python.org/downloads/
2. Click **"Or get the standalone installer for Python 3.14.3"** — this downloads a `.exe` file.
3. Run the installer.
4. **Check the box that says `Add Python to PATH`** before clicking Install.

![Python download page — click "Or get the standalone installer for Python 3.14.3" to download the .exe file](images/download_python.png)

![Python installer — check "Add Python 3.14 to PATH" at the bottom before clicking Install Now](images/installation_python.png)

5. Finish the installation.

**On Mac:**

1. Go to https://www.python.org/downloads/
2. Click **"Download Python 3.14.3"** — this downloads a `.pkg` file.
3. Open the `.pkg` file and follow the installer steps.
4. No PATH checkbox is needed on Mac — the installer handles it automatically.
5. Finish the installation.

How to test:

If you are using Windows and have never used the command line before:

1. Click the Start menu.
2. Type `cmd`.
3. Open **Command Prompt**.
4. A black or dark window will appear. You can type commands there.

If you are using a Mac and have never used the command line before:

1. Press `Command + Space` to open Spotlight search.
2. Type `Terminal`.
3. Open the **Terminal** application.
4. A window will appear where you can type commands.

Then run:

```bash
python --version
```

If that does not work, try:

```bash
py --version
```

You should see a Python 3 version number.

![Command Prompt showing a successful `python --version` output](images/cmd_python.png)

To keep your test files organized, first create a folder for setup checks.

Example:

```text
Documents/Economics/setup_test/
```

You can create this folder in File Explorer.
For example, open your `Documents` folder, create a folder named `Economics`, and inside it create another folder named `setup_test`.

On a Mac, you can do the same thing in Finder.
Open your `Documents` folder, create a folder named `Economics`, and inside it create another folder named `setup_test`.

Inside that folder, create a file named `test.py` with the following content:

```python
print("Python is working")
```

The easiest way to run this test is in VS Code:

1. Open VS Code.
2. Click `File` > `Open Folder`.
3. Open your `setup_test` folder.
4. In the top menu, click `Terminal` > `New Terminal`.
5. A terminal will open at the bottom of the VS Code window.

![VS Code terminal panel — click "Terminal" > "New Terminal" to open it at the bottom of the window](https://code.visualstudio.com/assets/docs/terminal/getting-started/open-terminal.png)

Then run:

```bash
python test.py
```

If `python` does not work on Windows, try:

```bash
py test.py
```

You should see:

```text
Python is working
```

If you see that message, Python is installed correctly and can run a file.

---

## 4. Install Quarto

Download:

- https://quarto.org/docs/get-started/

Use the **current release v1.9.36** — do not use the pre-release version.

![Quarto download page — select the current release v1.9.36, not the pre-release](images/download_qualto.png)

What to do:

1. Download the **v1.9.36** installer for your operating system (`.msi` on Windows, `.pkg` on Mac).
2. Run the installer.
3. Finish installation.

How to test:

If you already opened the VS Code terminal in the `setup_test` folder, you can use that same terminal.
Otherwise, on Windows, open Command Prompt using the steps above.
If you are using a Mac, open Terminal using the steps above.

Then run:

```bash
quarto --version
```

You should see a version number.

If you see a version number, Quarto is installed correctly.

---

## 5. Install a PDF Engine for Quarto

This is required so that Quarto can render directly to **PDF** during class.

Recommended option:

- TinyTeX through Quarto: https://quarto.org/docs/output-formats/pdf-engine.html

Alternative:

- TeX Live: https://www.tug.org/texlive/
- MiKTeX: https://miktex.org/download

Recommended for students:

- If you are unsure, install **TinyTeX through Quarto**.
- This is the simplest option for most students.

How to install TinyTeX:

Open a terminal (Command Prompt on Windows, Terminal on Mac) and run:

```bash
quarto install tinytex
```

What this command does, step by step:

- `quarto` — calls the Quarto program you installed in Step 4.
- `install` — tells Quarto to download and install something.
- `tinytex` — the name of the PDF engine to install. TinyTeX is a lightweight version of LaTeX, which is the system Quarto uses to create PDF files.

Quarto will download TinyTeX automatically and install it for you. You do not need to visit any other website.

When the installation finishes, you should see a message saying installation was successful.

> **Note:** The download may take a few minutes depending on your internet connection. This is normal.

How to test Quarto and PDF rendering:

In the same `setup_test` folder, create a file named `test.qmd` with the following content:

```markdown
---
title: "Quarto PDF Test"
format: pdf
---

# Test

If you can read this in a PDF file, Quarto and the PDF engine are working.
```

If file extensions are hidden on your computer, make sure the file is really named `test.qmd`, not `test.qmd.txt`.

Then run:

```bash
quarto render test.qmd --to pdf
```

If everything is installed correctly, Quarto should generate a PDF file in the same folder.
You should see a new file named `test.pdf`.

---

## 6. Install VS Code Extensions

After opening VS Code, install these extensions from the Extensions panel:

1. **Python** by Microsoft
   https://marketplace.visualstudio.com/items?itemName=ms-python.python

2. **Jupyter** by Microsoft
   https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter

3. **Quarto**
   https://marketplace.visualstudio.com/items?itemName=quarto.quarto

How to install:

1. Open VS Code.
2. Click the Extensions icon on the left sidebar.
3. Search for each extension by name.
4. Click Install.

---

## 7. Confirm Everything Works

Before class, please verify all of the following:

- VS Code opens normally.
- Python runs in the terminal.
- Quarto runs in the terminal.
- Your GitHub account is ready to use in VS Code.
- The Python extension is installed in VS Code.
- The Jupyter extension is installed in VS Code.
- The Quarto extension is installed in VS Code.
- Your `test.py` file runs successfully.
- Your `test.qmd` file renders to PDF successfully.

You can test with these commands:

```bash
python --version
quarto --version
```

If `python` does not work on Windows, try:

```bash
py --version
```

---

## 8. What Not to Install Yet

Please **do not** install the project Python packages before class.

The packages we need may differ depending on the class exercise.
We will install the required packages together in class and use any installation problems as part of the learning process.

---

## 9. What We Will Do in Class

In class, we will:

1. Open the project in VS Code.
2. Run Python code block by block using `# %%` cells.
3. Install required Python packages.
4. Read error messages.
5. Troubleshoot installation and environment issues.
6. Work through course coding exercises.
7. Render a short Quarto document.

---

## 10. Troubleshooting Before Class

If something does not work, try these checks first.

### Python not found

- Reopen the terminal after installation.
- Restart your computer if needed.
- On Windows, try `py --version` instead of `python --version`.
- If Python still is not found, reinstall Python and make sure `Add Python to PATH` is checked.

### Quarto not found

- Reopen the terminal after installation.
- Restart VS Code.
- Reinstall Quarto if necessary.

### VS Code extensions not working

- Restart VS Code.
- Make sure the extension finished installing.
- Update VS Code if needed.

---

## 11. Recommended Folder Setup

Before class, create a folder on your computer where you will store the project files.

Example:

```text
Documents/Economics/coding_exercises/
```

Or, if you prefer organizing by category first:

```text
Documents/lecture/economics/coding_exercises/
```

Put all class files there once they are distributed.

---

## 12. Checklist

Complete this before class:

- Create a GitHub account and start Copilot student registration
- Install VS Code
- Install Python
- Install Quarto
- Install VS Code extensions: Python, Jupyter, Quarto
- Test `python --version` or `py --version`
- Test `quarto --version`
- Do not install project packages yet

If all items above are done, you are ready for class.
