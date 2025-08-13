## Hi there 👋



Here are some ideas to get you started:

- 🔭  Trabalho atualmente com Ciencia de Dados
- 🌱  Estou aprendendo atualmente Python
- 📫  joaovitormartinsbtos@gmail.com  


<!--
<div> 
  <a href="https://instagram.com/joaoribeiro_mv" target="_blank"><img src="https://img.shields.io/badge/-Instagram-%23E4405F?style=for-the-badge&logo=instagram&logoColor=white" target="_blank"></a>
  <a href="https://www.linkedin.com/in/luizteixeirasantos" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a> 
  <a href = "[mailto:luiz.hh200@gmail.com](https://mail.google.com/mail/u/1/?ogbl#inbox)"><img src="https://img.shields.io/badge/-Gmail-%23333?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a>
</div> 
!-->
### 📊 Estatísticas

<p>
  <img 
    align="left" 
    alt="GitHub Stats" 
    height="200" 
    style="padding-right: 10px;" 
    src="https://github-readme-stats.vercel.app/api?username=JotaVeMr&show_icons=true&theme=tokyonight&include_all_commits=true&locale=pt-br" 
  />

<img 
      align="left" 
      alt="GitHub Stats" 
      height="200" 
      src="https://github-readme-stats.vercel.app/api/top-langs/?username=JotaVeMr&theme=tokyonight&layout=compact&custom_title=Tecnologias&langs_count=9" 
  />

</p>




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
          github_user_name: username #seu username
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
