Velo - Virtual ID Card 🪪
An immaculate, 3D-flipping digital business card. Built with a "zero-dependency" philosophy using Tailwind CSS and Vanilla JavaScript for maximum speed and instant deployment.

🚀 1. Command Line Setup & Deployment
If you are setting this up for the first time or fixing a "remote origin already exists" error, run these commands in your terminal:

Bash
# Navigate to your project folder
cd [INSERT_YOUR_FOLDER_NAME]

# Initialize and link to GitHub
git init
git remote add origin https://github.com/[INSERT_GITHUB_USERNAME]/[INSERT_REPO_NAME].git

# IF YOU GET "remote origin already exists", RUN THIS INSTEAD:
git remote set-url origin https://github.com/[INSERT_GITHUB_USERNAME]/[INSERT_REPO_NAME].git

# Push your code
git add .
git commit -m "feat: initial card build with master readme"
git branch -M main
git push -u origin main
🛠 2. How to Edit & Customize
This project is contained entirely within index.html. You do not need to touch any other files to change the design.

A. Changing the Brand Identity
Colors: Locate the tailwind.config section in the <head>. Change the hex code for velo-500 (currently #0044FF) to your brand's primary color.
Logo: The logo is a pure SVG (Line 80). You can replace the <path> data with your own SVG code or replace the entire <svg> tag with an <img> tag pointing to your logo file.
B. Updating Interactive Actions
Contact Button: Search for id="contactButton". In the script section at the bottom, change the string 'admin@velo.com' to your professional email.
External Links: Update the href attributes for the Website, Slack, and FAQ buttons to point to your specific business assets.
C. Social Media Preview (SEO)
To control how the link looks when shared via text (iMessage/WhatsApp), update these tags in the <head>:
og:title: Your Name or Business Name.
og:description: A 1-sentence tagline.
og:image: A URL to a 1200x630px JPG preview of your card.
🤖 3. Automation (CI/CD)
This project uses GitHub Actions to catch errors before they go live.
Create a folder: .github/workflows/
Create a file: ci-cd.yml
Paste this code to enable automatic HTML linting:
YAML
name: Code Quality Check
on: [push]
jobs:
  lint:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: HTML Hint
        run: |
          npm install -g htmlhint
          htmlhint index.html
⚠️ 4. Troubleshooting Guide
Issue	Cause	Solution
"Remote origin already exists"	A GitHub link is already saved.	Run git remote set-url origin [URL]
"Permission denied (publickey)"	SSH keys aren't set up.	Use the HTTPS URL instead of the SSH URL.
"Nothing to commit"	No changes detected.	Ensure you saved your files in your editor first.
Card doesn't flip	Script error or tap conflict.	Check the browser console (F12) for JS errors.
Tailwind styles missing	No internet connection.	The CDN requires an active connection to load styles.
🌐 5. Deployment Options
Option A: GitHub Pages (Free)
Go to Settings > Pages in your GitHub Repo.
Select Branch: main and folder /(root). Click Save.
Your site lives at: https://[USERNAME].github.io/[REPO-NAME]/
Option B: Vercel (Professional)
Install Vercel CLI: npm i -g vercel
Deploy: Type vercel --prod in your terminal.
Maintained by Dusty McLean