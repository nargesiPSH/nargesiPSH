
👩‍💻 About Me :
I am a machine learning researcher currently working on machine learning and Deep learning for healthcare
- 🔭 I’m interested in: 
  *  Machine learning for Healthcare
  *   Digital Twin
  *  Synthetic Data Generation
  *  Learning from Noisy Data 
              
- 🌱 I’m learning Unreal engine and modelling and animate on Blender

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
          github_user_name: nargesiPSH
          svg_out_path: dist/github-contribution-grid-snake.svg
      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

