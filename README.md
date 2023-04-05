#### Olá! Eu sou a Jamilly, mas pode me chamar de Mille ☁️

 [![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=millefy&count_private=true&show_icons=true&theme=onedark)](https://github.com/anuraghazra/github-readme-stats)

[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=millefy&layout=compact&theme=onedark)](https://github.com/anuraghazra/github-readme-stats)

name: Generate Datas

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update datas
    runs-on: ubuntu-latest
    steps:
      # Snake Animation
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: millefy
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
  
