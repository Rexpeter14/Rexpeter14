### Hi there 👋

<!--
**Rexpeter14/Rexpeter14** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
<p align="center">

  <img src="https://capsule-render.vercel.app/api?text=Hey Everyone!🕹️&animation=fadeIn&type=waving&color=gradient&height=100"/>

</p>
<h2> 🚀 &nbsp;Some Tools I Have Used and Learned</h2>

<p align="left">

<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg" alt="vscode" width="45" height="45"/>

<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bash/bash-original.svg" alt="bash" width="45" height="45"/>

<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/php/php-original.svg" alt="php" width="45" height="45"/>

</p>

5. Your GitHub History 📈

Finally, at the end of your Profile README, you can practically include anything. Some developers put up what’s currently playing on their Spotify profile, some add their GitHub stats or some add a fun little snake game on your GitHub contribution graph like me which I’ll show you guys how to put up!

My GitHub Stats!

I begin with two GitHub ReadMe Stat Cards. One shows my total number of stars, commits and pull requests, etc. And the other one displays my most used Programming languages in percentages. You guys can get these cards from the popular GitHub ReadMe Stats Repo and the best part about these is that they are fully customizable with different settings and themes!

Next up is probably my favorite thing out of all of my profile elements. Making a Snake Game out of your GitHub Contribution Graph. It’s fairly easy to set up and looks extremely satisfying when the snake gobbles up your commit graph.

To set it up for your profile, we are going to use something called GitHub Actions. GitHub Actions are CI/CD tools in GitHub where you can initiate workflows that automatically run, deploy and build your stuff.

![Snake animation](https://github.com/thepiyushmalhotra/thepiyushmalhotra/blob/output/github-contribution-grid-snake.svg)

The first step is to copy this line above and add it to your profile’s README. Make sure to change the username to yours instead of mine.

Now we need to create a GitHub workflow so that the contribution graph in the snake animation will get updated according to the cronjob that we will set up.

Go to your “Actions” tab in your README repository and create a New Workflow. This will generate a new folder in your repository called “.github/workflows” and after that, it will make a new file inside of it called “main.yml”.

Setup a New Workflow

main.yml file

Delete everything inside of the newly created main.yml file and add this code to it below:

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

          github_user_name: thepiyushmalhotra

          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3

        with:

          target_branch: output

          build_dir: dist

        env:

          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

Make sure to replace my username with yours. We use a cronjob here that updates every 12 hours so whenever you have a new commit, it's going to get added to your snake animation.

The final step is to go back to your “Actions” page of your README file, click the newly created workflow “Generate Datas” or any name that you give it, and click the “Run Workflow” button.

Run Your Workflow

Et voila! Your Snake GitHub Contribution Graph is active now. Enjoy watching that snake eat up your hard work! To wrap it all up, I just added another capsule render animation at the footer which looked nice to me as you can see in the GIF above.

I’ve also mentioned some extra collated list of resources for your individual design needs:

Awesome-GitHub-Profile-Readme — A list of amazing Readmes from many talented developers!

GitHub Readme Generator — An easy way to quickly generate a basic design template for your profile.

Read up more on GitHub Actions if you’re interested in automation.

Generate various GitHub metrics that can be embedded anywhere.

If you want a quick and simple way to create cronjobs and learn more about them, then Crontab Guru is a pretty good resource and you get to know the exact time that your workflow will run.

And that was it for my GitHub Profile Design. Hope you guys liked this blog post on how to design an attractive GitHub Profile Readme that’s aesthetically pleasing as well as functional. Let me know if I can make some additions or changes to this article or if I missed some other fun stuff on GitHub. I do plan to add a blog post workflow as well which can show your latest blog posts from Dev.to but I’ll leave that for another short article.

Thank you for reading! If you liked my writing, here are some of my other informative articles:

Most Important Things to Learn Other than Coding…

Hard to swallow pills every new Developer should take.

Revisiting Atomic Habits — My First Book of 2021 and 2022

The Analysis Paralysis of Learning to Code…

The Beginner-friendly way to learn from FreeCodeCamp on YouTube.

Let’s have a Chat! Connect with me on GitHub, Twitter, and LinkedIn. Ciao!

