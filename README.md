[snake.yml](https://github.com/user-attachments/files/30622164/snake.yml)
[README.md](https://github.com/user-attachments/files/30622160/README.md)
<div align="center">

<a href="https://git.io/typing-svg">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=28&duration=3000&pause=1000&color=58A6FF&center=true&vCenter=true&multiline=true&width=800&height=100&lines=Hi+there%2C+I'm+Ayush!+%F0%9F%91%8B;In+pursuit+of+elegant+solutions+to+fundamental+problems" alt="Typing SVG" />
</a>

</div>

<br>

## 🚀 About Me

- 🎓 2nd-year **Electronics and Computer Engineering** student at **Thapar Institute of Engineering & Technology**, Patiala
- 🔭 Currently focused on **Data Structures and Algorithms (DSA)**
- 💻 I enjoy building foundational projects — from **C++ logic exercises** to **Python-based image processing**
- 🌱 Always learning and optimizing code for better performance and time complexity

<br>

## 🛠️ Tech Stack & Tools

<div align="center">
  <img src="https://skillicons.dev/icons?i=c,cpp,py,git,github,vscode&theme=dark" />
</div>

<br>

## 📈 GitHub Stats

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=ayushjamdagni&show_icons=true&theme=dark&hide_border=true&bg_color=0D1117&title_color=58A6FF&icon_color=58A6FF&text_color=C9D1D9" alt="Ayush's GitHub Stats" height="165"/>
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=ayushjamdagni&theme=dark&hide_border=true&background=0D1117&stroke=58A6FF&ring=58A6FF&fire=58A6FF&currStreakLabel=58A6FF" alt="Ayush's Streak Stats" height="165"/>
</div>

<br>

## 🐍 Contribution Snake

<div align="center">
  <img src="https://raw.githubusercontent.com/ayushjamdagni/ayushjamdagni/output/github-contribution-grid-snake-dark.svg" alt="Snake animation" />
</div>
name: Generate Snake Animation

on:
  schedule:
    - cron: "0 0 * * *"   # runs once a day at midnight UTC
  workflow_dispatch: {}    # lets you trigger it manually from the Actions tab
  push:
    branches:
      - main               # regenerates whenever you push to main

jobs:
  generate:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    steps:
      - name: Generate snake SVG
        uses: Platane/snk@v3
        with:
          github_user_name: ayushjamdagni
          outputs: |
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark
            dist/github-contribution-grid-snake.svg

      - name: Push snake SVG to the output branch
        uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

</div>
