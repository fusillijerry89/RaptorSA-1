# Super advanced discord bot ![alt text](https://i.imgflip.com/xu2ct.jpg)

![Issues](https://img.shields.io/github/issues/cramenorn/raptorsa.svg)
![Stars](https://img.shields.io/github/stars/cramenorn/raptorsa.svg)
![Forks](https://img.shields.io/github/forks/cramenorn/raptorsa.svg)
[![Build Status](https://dev.azure.com/davidedlc97/RaptorSA/_apis/build/status/Cramenorn.RaptorSA?branchName=master)](https://dev.azure.com/davidedlc97/RaptorSA/_build/latest?definitionId=1&branchName=master)

**RaptorSA** is a multi function bot, you can listen music, manage roles, get various informations and many other things. This Discord bot can be helpful for anyone who wants to learn how to make a discord.js bot, every command has it's own folder so it's more easy to read the entire project. I made this so new users can also look at the methods used for certain commands and get some ideas for their Discord bot.

# Contributing

If you want help, don't worry, there are many ways to do it:

* **Contribute with code**: Setup a development environment, make some changes, and [open a pull request](https://github.com/Cramenorn/RaptorSA/pulls).

* **Contribute with ideas**: Have a great idea, but don't know how to code ? No problem! Open an issue so we can talk about your idea.

## Branching

New Pull Requests should be made upon the **testing** branch. If the code does not have any particular issues, then it will be merged into **master** branch.

## Common Issues & Resolutions

Please see the [Common Issues](https://github.com/Cramenorn/RaptorSA/wiki/Common-Issues) page before posting an issue.

# Api keys and tokens

Some commands require an **Api Key** or a **Token** which can be find on these websites: 

* [Google Custom Search Api Key and CX](https://developers.google.com/custom-search/)
* [Riot Games Developer](https://developer.riotgames.com/)
* [Discord Developer to get the token for the bot](https://discordapp.com/developers/applications/)

# What do I need to make the bot work ?

## To do

Make a config.json file in the jsonFiles directory of the project and add:

```json
{
  "name": "RaptorSA",
  "version": "2.0.0",
  "description": "put something here",
  "main": "index.js",
  "token": "Your-Bot-Token",
  "author": "Cramenorn",
  "prefix": "$"
}
```

At this point you can use **docker** or install manually the **tools**.

### Manual installation

* You will need [python 2.7](https://www.python.org/downloads/) and [FFmpeg](https://www.ffmpeg.org/), **Discord.js now requires Node version greater than or equal to 12.0.0** .
* Make a folder and git clone this repository: [RaptorSA.git](https://github.com/Cramenorn/RaptorSA.git).
* Before typing `npm install`, you should check the **package.json** file. The installation process is different if you choose one of the two packages:
    * If you are going to use the bot in a production environment you should use the `@discordjs/opus`, in this case you do not need to edit the package.json file. Before typing `npm install`, this package requires the C++ tools, on Windows 10 you simply need to download Visual Studio and install the [Windows desktop development with C++ tool](https://devblogs.microsoft.com/cppblog/windows-desktop-development-with-c-in-visual-studio/#installation).
    * For testing purposes you should use the following package `"opusscript": "^0.0.7"` (change **@discordjs/opus** package with **opusscript**, they can't work together, you need to use one of them), you do not need to do anything in particular. You can directly install the packages as specified in the next step below.
* Then type `npm install` to get the needed packages for the bot.
* Check if **ytdl-core** is updated with the following command `npm outdated`, if the current version is not updated to the latest, type `npm update ytdl-core` and update the package.json file.
* Edit json files in jsonFiles folder, you need a discord bot **Token** and various **Api Keys** to get the bot work.
* Launch the `index.js` file.

### Docker

#### How do I install Docker ?

The process is different on every OS, you can check the [official documentation](https://docs.docker.com/get-docker/) for more informations.

#### How do I use Docker ?

If you want to skip the previous steps you can use docker, in this way you do not need to install other tools on your computer. To use the container, run the following commands inside the RaptorSA folder:

* `docker build -t raptorsa .`
* `docker run raptorsa`

# CI/CD with Azure Pipelines

## Do I need to use the Azure Pipelines ?

No you don't, you can delete the **azure-pipelines.yml** file if you do not need it or you want to use another pipeline.

## If I want to use the Azure Pipelines, what do I need to do ?

* Create a repo on **Azure Devops**.
* [Create a pipeline and connect Azure Devops to Github](https://docs.microsoft.com/en-us/azure/devops/pipelines/create-first-pipeline?view=azure-devops&tabs=javascript%2Cyaml%2Cbrowser%2Ctfs-2018-2)
* Copy the pipeline YAML code from the **azure-pipelines.yml** file, and paste it into the YAML editor for your new pipeline on Azure Devops.
* Save and run the pipeline.

# Commands

See the [Commands](https://github.com/Cramenorn/RaptorSA/wiki/Commands) page.

# Built with
* [Discord.js](https://discord.js.org/#/)
* [Node js](https://nodejs.org/en/)