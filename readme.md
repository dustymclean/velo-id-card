Markdown
# Velo - Virtual ID Card 🪪

An immaculate, 3D-flipping virtual ID card with high-performance CSS animations and built-in toast notifications. 

## 🛠 Project Structure & Dependencies

This project is a **Zero-Dependency Static Web App**. 
* **Tailwind CSS**: Loaded via CDN (no installation required).
* **JavaScript**: Vanilla JS (no frameworks required).
* **Assets**: All icons are inline SVGs (no external image files).

---

## 🚀 Deployment Guide (Step-by-Step)

### 1. Local Environment Setup
Before starting, ensure you have **Git** installed on your machine.

**Open your terminal (Command Prompt, PowerShell, or Terminal) and run these commands:**

```bash
# Create the project directory
mkdir velo-id-card

# Move into the new directory
cd velo-id-card

# Create the index.html file (Paste your code into this file)
touch index.html

# Initialize version control
git init

# Stage all files
git add .

# Commit your changes
git commit -m "Initial commit: Velo Card with 3D Flip"
2. Connect to GitHub

Go to GitHub and create a new repository named velo-id-card.

Do not initialize it with a README (you already have one!).

Copy the Remote URL provided by GitHub.

Run the following in your terminal:

Bash
# Link your local folder to GitHub
git remote add origin [https://github.com/YOUR_USERNAME/velo-id-card.git](https://github.com/YOUR_USERNAME/velo-id-card.git)

# Set the branch to main
git branch -M main

# Push the code
git push -u origin main
3. Activate GitHub Pages

Once the code is pushed, your site is ready to go live:

Navigate to your repository on GitHub.

Click Settings > Pages.

Under Branch, select main and / (root).

Click Save.

Your site will be live at https://YOUR_USERNAME.github.io/velo-id-card/ within 60 seconds.

📖 Features
Double-Toss Animation: A 540-degree mid-air flip with dynamic "glint" lighting effects.

Responsive Design: Mobile-first layout using Tailwind CSS.

Smart Actions: Built-in "Copy to Clipboard" for contact info and native Mobile Share API support.