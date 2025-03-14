# 👋 Hi there, I'm Lakshitha Wijerathne  

[![Profile Views](https://komarev.com/ghpvc/?username=mlswijerathne&label=Profile%20Views&color=brightgreen&style=flat)](https://github.com/mlswijerathne)

---

## 📊 GitHub Analytics  

<div align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=mlswijerathne&theme=transparent&hide_border=true" width="49%" />
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/stats?username=mlswijerathne&theme=github_dark" width="49%" />
</div>

---

## 🔥 Recent Projects (Auto-Updated)  

<!-- GitHub Action Will Auto-Update This Section -->
<!-- START_SECTION:recent_repos -->
<!-- END_SECTION:recent_repos -->

---

## 🚀 Top Languages  
[![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=mlswijerathne&langs_count=6&layout=compact&theme=github_dark)](https://github.com/mlswijerathne)

---

## 📂 Manually Listed Projects  
[![Auction Management System](https://img.shields.io/badge/GitHub-Auction_Management_System-blue?style=for-the-badge&logo=github)](https://github.com/mlswijerathne/auction-management)  
[![Smart Plate App](https://img.shields.io/badge/GitHub-Smart_Plate_App-green?style=for-the-badge&logo=github)](https://github.com/mlswijerathne/smart-plate)  
[![Jade Restaurant UI/UX](https://img.shields.io/badge/GitHub-Jade_Restaurant_UIX-orange?style=for-the-badge&logo=github)](https://github.com/mlswijerathne/jade-review)  

---

## 🔄 Auto-Update Recent Projects (GitHub Actions)  
To automatically update recent projects in your profile, add the following GitHub Actions workflow:

### 📌 **Create a file:** `.github/workflows/update-readme.yml`
```yaml
name: Update Recent Projects in README

on:
  schedule:
    - cron: "0 0 * * *" # Runs daily
  workflow_dispatch:

jobs:
  update-readme:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout repository
        uses: actions/checkout@v2
        
      - name: Fetch Recent Repos
        uses: Readme-Workflows/recent-activity@v2.1.0
        with:
          GH_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          MAX_REPOS: 5

      - name: Commit and Push Changes
        run: |
          git config --global user.name "GitHub Actions"
          git config --global user.email "actions@github.com"
          git add README.md
          git commit -m "Updated recent projects" || echo "No changes"
          git push