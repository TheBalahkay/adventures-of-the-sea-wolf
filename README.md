# The Comet D&D Campaign Party Notes

This repo serves as the hub for the party notes of the players of this campaign. it is made using obsidian notes and Quartz 4. It uses github actions to update the free site whenever a commit is posted to the repo. This site is version controlled using git and github, and is a low maintenance way to host a site for free. Updating the site is as simple as making changes to the notes in obsidian and pushing them to the repo. Set up instructions for updating the site and running it locally can be found below. Try not to be intimidated by the technical jargon, I will walk you through everything step by step, and if you get stuck, feel free to reach out to me for help.

## Live site
The live site can be found at:
- https://thebalahkay.github.io/adventures-of-the-sea-wolf/


## Updating this site
You can update this site by making changes to the notes in the `content` folder of this repo. The content folder is where all the markdown files that make up the site are stored. A markdown file is a plain text file that uses special syntax to format text. Markdown files are easy to read and write, and they can be converted to HTML for display on the web. You can edit these files directly in github, but it is recommended to use obsidian for a better experience. If you want to use obsidian, you can clone this repo to your local machine and open the folder in obsidian. Any changes you make to the files in obsidian will be reflected in the repo when you push the changes. Obsidian uses markdown files natively, so you don't need to worry about converting the files to markdown.

Obsidian is a free note taking app that allows you to create and manage markdown files. You can download obsidian from the official website: https://obsidian.md/

1. Open obsidian and select "Open folder as vault".
2. Select the `content` folder in the root directory of the repo.
3. Make changes to the files in obsidian as you would with any other obsidian vault.
4. When you are ready to push the changes to the repo, open github desktop and select the repo.
5. You should see the changes you made in obsidian listed in github desktop. Add a commit message describing the changes you made and click "Commit to v4".
6. Click "Push origin" to push the changes to the repo on github.

Once you have pushed the changes to the repo, github actions will automatically build and deploy the site. The changes should be reflected on the live site within a few minutes.

### Images
If you want to add images to the site, you can add them to the `content/_media` folder. If you are editing from obsidian then this will just be the `_media` folder. Please just add the images/multimedia to this folder. Quartz will "ignore" this folder when seting up the navigation and graph views. The site will still display them but they will not add additional and unneccessary nodes to the graph or add them as "pages" for the site. You can then reference the images in your markdown files using the following syntax:

`![alt text](./_media/image.png)`


## Cloning this repo (Get the files on your local machine)
Cloning this repo means creating a copy of the repo on your local machine. This is useful if you want to make changes to the files in the repo using obsidian or if you want to run the site locally to preview changes before pushing them to the repo.

To clone this repo, you will need to have git installed on your machine. I recommend that you use the github desktop application for this. It is easier for begginers to get started and has a nice graphical user interface. You can download github desktop from the official website: 
- https://desktop.github.com/

Once you have github desktop installed, you can clone this repo by following these steps:
1. Open github desktop and sign in to your github account.
2. Select "Clone repository from the internet".
3. In the "Repository URL" field, enter the URL of this repo: `https://github.com/TheBalahkay/adventures-of-the-sea-wolf.git`
4. Choose a local path where you want to clone the repo to. This will be the folder that the site files live. 


If you prefer to use the command line interface (CLI), you can follow the guide from gihub below to install git and clone the repo using the CLI:
- https://github.com/git-guides/install-git

## Running this site locally.
Running this site locally is optional, but it can be useful for previewing changes before pushing them to the repo. Most of the time the changes you make to the content folder via obsidian will be reflected on the live site within a few minutes of pushing to the repo, but if you want to be able to see the changes immediately, you can run the site locally.

If you want to run this site locally to preview changes before pushing them to the repo, you will need to have the following dependencies installed on your machine:

### Dependencies
A dependency is a piece of software that is required for another piece of software to work. In this case, the below dependencies are required for Quartz to run on your machine locally. It may sound complicated, but don't worry, I will walk you through the process step by step.

#### Mac 
- Homebrew: https://brew.sh
    - Homebrew is a package manager for macOS. You can install it by running the following command in your terminal:
    - `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
    
- Node JS: https://nodejs.org/en (download and install Node.js)
    - node js is a javascript runtime that allows you to run javascript code outside of a web browser. You can install it using Homebrew by running the following command in your terminal:
    - `brew install node`
- NPM: https://www.npmjs.com
    - npm is a package manager for JavaScript. It is included with Node.js, so if you have installed Node.js, you should already have npm installed as well.
- nvm: nvm is a version manager for Node.js. It allows you to easily switch between different versions of Node.js on your machine. You can install nvm by running the following command in your terminal:
    - `curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash`
    - After installing nvm, you can use it to install and manage different versions of Node.js. For example, to install the latest version of Node.js, you can run:
    - `nvm install node --lts`
    - To switch to a specific version of Node.js, you can run:
    - `nvm use <version>`

#### Windows
- Volta: 
    - Volta is a JavaScript tool manager that makes it easy to install and manage different versions of Node.js and other JavaScript tools. You can install Volta by running the following command in your terminal:
    - `winget install Volta.Volta`

- Node JS: https://nodejs.org/en/dowloads (download and install Node.js)
    - node js is a javascript runtime that allows you to run javascript code outside of a web browser. You can download and install Node.js from the official website or you can paste the following commands into your terminal one at a time:
    - `volta install node@22` (or whatever version quarts requires if this doc is out of date)

- NPM: https://www.npmjs.com/get-npm (download and install npm)
    - npm is a package manager for JavaScript. It is included with Node.js, so if you have installed Node.js, you should already have npm installed as well.


once you have all the dependencies installed, you can clone this repository to your local machine using the github desktop app or by using the cli (command line interface)

I will assume you have cloned the repo and are in the root directory of the repo in your terminal. The root directory is the folder that contains the .git folder.

Once you are there run the following command to install the dependencies for the project:

`npm install`
This will install all the dependencies listed in the package.json file.

Then you can run the following command to build and serve the site locally:
`npx quartz build --serve` 


