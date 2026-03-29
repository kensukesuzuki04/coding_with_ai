# Pre-Class Setup Guide: U.S. State GDP Mapping Project

> **Course Use**
> This setup guide is prepared for Clark University Economics Department course `ECON206`.
>
> **Document Preparation**
> This README was prepared with GitHub Copilot under Professor Suzuki's instruction and revision.

This guide is for students to complete **before class**.

The goal is to make sure everyone arrives with the required software installed so that, during class, we can focus on running the code, installing Python packages, seeing errors, and fixing them.

## What You Need to Install Before Class

Please install the following applications before class:

1. **Visual Studio Code**
2. **Python**
3. **Quarto**
4. **A PDF engine for Quarto**

Do **not** install project-specific Python packages yet. We will do that in class.

---

## 1. Install Visual Studio Code

Download:

- https://code.visualstudio.com/download

What to do:

1. Download the version for your operating system.
2. Run the installer.
3. During installation on Windows, it is helpful to enable:
   - Add to PATH
   - Open with Code
   - Register Code as an editor for supported file types

After installation, open VS Code once to make sure it starts normally.

---

## 2. Install Python

Download:

- https://www.python.org/downloads/

What to do:

1. Download the latest stable Python 3 version.
2. Run the installer.
3. On Windows, **check the box that says `Add Python to PATH`** before clicking Install.
4. Finish the installation.

How to test:

Open a terminal or command prompt and run:

```bash
python --version
```

If that does not work, try:

```bash
py --version
```

You should see a Python 3 version number.

To keep your test files organized, first create a folder for setup checks.

Example:

```text
Documents/ECON206/setup-test/
```

Inside that folder, create a file named `test.py` with the following content:

```python
print("Python is working")
```

Then open a terminal in that folder and run:

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

---

## 3. Install Quarto

Download:

- https://quarto.org/docs/get-started/

What to do:

1. Download the installer for your operating system.
2. Run the installer.
3. Finish installation.

How to test:

Open a terminal and run:

```bash
quarto --version
```

You should see a version number.

---

## 4. Install a PDF Engine for Quarto

This is required so that Quarto can render directly to **PDF** during class.

Recommended option:

- TinyTeX through Quarto: https://quarto.org/docs/output-formats/pdf-engine.html

Alternative:

- TeX Live: https://www.tug.org/texlive/
- MiKTeX: https://miktex.org/download

Recommended for students:

- If you are unsure, install **TinyTeX through Quarto**.
- This is the simplest option for most students.

How to test Quarto and PDF rendering:

In the same `setup-test` folder, create a file named `test.qmd` with the following content:

```markdown
---
title: "Quarto PDF Test"
format: pdf
---

# Test

If you can read this in a PDF file, Quarto and the PDF engine are working.
```

Then run:

```bash
quarto render test.qmd --to pdf
```

If everything is installed correctly, Quarto should generate a PDF file in the same folder.

---

## 5. Create a GitHub Account and Activate Copilot Student Access

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

That means you should wait on packages such as:

- `pandas`
- `numpy`
- `matplotlib`
- `geopandas`
- `mapclassify`
- `shapely`
- `pyproj`

We will install these together in class and use any installation problems as part of the learning process.

---

## 9. What We Will Do in Class

In class, we will:

1. Open the project in VS Code.
2. Run Python code block by block using `# %%` cells.
3. Install required Python packages.
4. Read error messages.
5. Troubleshoot installation and environment issues.
6. Generate maps of U.S. state GDP.
7. Render a short Quarto draft.

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
Documents/ECON206/gdp-mapping-project/
```

Or, if you prefer organizing by category first:

```text
Documents/lecture/econ206/gdp-mapping-project/
```

Put all class files there once they are distributed.
- Google Sites does **not** natively render Markdown files.

For Google Sites, the best options are:

1. Copy and paste the content from the Markdown file into a Google Sites page.
2. Convert the Markdown to a Google Doc and embed or link it.
3. Render the Quarto file to HTML or PDF and link that output from Google Sites.

---

## 12. Checklist

Complete this before class:

- Install VS Code
- Install Python
- Install Quarto
- Install VS Code extensions: Python, Jupyter, Quarto
- Test `python --version` or `py --version`
- Test `quarto --version`
- Do not install project packages yet

If all items above are done, you are ready for class.
