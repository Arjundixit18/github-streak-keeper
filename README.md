<h1 align="center">🔥 GitHub Streak Keeper 🔥</h1>

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com?user=arjundixit18&theme=radical&card_width=600" alt="GitHub Streak"/>
</p>

<p align="center">
  <img src="https://media.giphy.com/media/Ll22OhMLAlVDb8UQWe/giphy.gif" width="200"/>
</p>

---

## 📌 About
The **GitHub Streak Keeper** is an automated workflow that keeps your GitHub contribution streak alive by committing a small file update every day — even if you forget to code that day.

This project is powered by **GitHub Actions**, and ensures that your contribution graph stays green ✅.

---

## 🚀 Features
- ⏰ **Daily automatic commits** at a fixed time  
- 🛠 Uses `last_commit.txt` to store the latest commit date  
- 🔒 Secure push using `GITHUB_TOKEN`  
- 🌍 Timezone friendly — works in **IST** or any other offset  
- 📈 Perfect for maintaining **profile streaks**

---

## 📂 How It Works
1. A GitHub Action runs every day at **10:30 AM IST**.
2. The action updates `last_commit.txt` with the current date.
3. Changes are committed and pushed to the `main` branch.
4. Your GitHub streak continues without interruption.

---

## 📸 Screenshots

**GitHub Actions Running**
![Workflow Success](https://user-images.githubusercontent.com/000000/000000000-000000000.png)

**Contribution Graph**
![Contribution Graph](https://media.giphy.com/media/3ohzdQ1IynzclJldUQ/giphy.gif)

---

## ⚙️ Setup Guide

### 1️⃣ Fork This Repo
Click the **Fork** button at the top right of this page.

### 2️⃣ Enable GitHub Actions
- Go to **Settings → Actions → General**  
- Under **Workflow permissions**, select **Read and write permissions**  
- Enable **Allow GitHub Actions to create and approve pull requests**

### 3️⃣ Adjust Timezone
In `.github/workflows/streak.yml`:
```yaml
schedule:
  - cron: '0 5 * * *'  # Runs daily at 10:30 AM IST
