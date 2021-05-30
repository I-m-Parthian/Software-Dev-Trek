# Node.js
JavaScript outside the browser

## What is node.js ?

[Official Docs](https://nodejs.org/en/docs/)

Well in 1-line, Node.js® is a JavaScript runtime built on Chrome's V8 JavaScript engine.

Huh?

Historically, JavaScript could be executed only in a web browser. Things changed in 2009 when node.js came into being. Using node.js we can execute JavaScript outside the browser environment.

Go through the videos below to understand more about how it works.  
* [What is Node js?](https://www.youtube.com/watch?v=uVwtVBpw7RQ&feature=emb_imp_woyt)  
* [Node.js Architecture](https://www.youtube.com/watch?v=XUSHH0E-7zk&feature=emb_imp_woyt)  
* [How Node.js Works](https://www.youtube.com/watch?v=jOupHNvDIq8&feature=emb_imp_woyt)  


## Node Version Manager (NVM)

It is a tool used to manage multiple active Node.js versions.

The Node.js platform, Node.js ​community of tools, and Node.js libraries are fast-moving targets – what might work under one Node.js version is not guaranteed to work for another version of Node.js. Hence, users need ways to switch between multiple versions of Node.js

**Why use NVM?**

NVM allows users to:

- Locally download any of the remote Long Term Support (LTS) versions of Node.js with a simple command.
- Easily switch between multiple versions of Node.js, right from the command line.
- Set up aliases to switch between different downloaded versions of Node.js with ease.  

[Learn more about nvm](https://github.com/nvm-sh/nvm)

## For Linux and Mac users only
1. Run the NVM installer using either of the following commands:
```sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash
```
or
```sh
wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash
```

**2. Verify Installation**
To verify that nvm has been installed, do:
```sh
command -v nvm
```
which should output ```nvm``` if the installation was successful. Please note that which nvm will not work, since nvm is a sourced shell function, not an executable binary.  
**3. Using NVM**  
Once NVM is installed it allows users to install any version of Node.js through a simple command:
```sh
nvm install <SPECIFIC_NODE_VERSION>
```
*Recommended:* To install the latest LTS (Long Term Support) version of Node.js, use the following command:
```sh
nvm install --lts
```
To use any specific version of Node.js for your code, use the following command:
```
nvm use <SPECIFIC_NODE_VERSION>
```

## npm - the node package manager

***npm***, short for Node Package Manager (well, not really), is two things:

- it is an online repository for the publishing of open-source Node.js projects
- and, it is a command-line utility for interacting with said repository that aids in package installation, version management, and dependency management.

A majority of Node.js libraries and applications are published on npm, and many more are added every day. These applications can be searched for on [npmjs](http://npmjs.org/). Once you have a package you want to install, it can be installed with a single CLI command.

Let's say you're hard at work one day, developing the Next Great Application. You come across a problem, and you decide that it's time to use that cool library you keep hearing about - let's use Caolan McMahon's **async** as an example. Thankfully, **npm** is very simple to use: you only have to run **npm install async**, and the specified module will be installed in the current directory under **./node_modules/**. Once installed to your node_modules folder, you'll be able to use **require()** on them just like they were built-ins.

Let's look at an example of a global install - let's say coffee-script. The npm command is simple: **npm install coffee-script -g**. This will typically install the program and put a symlink to it in **/usr/local/bin/**. This will then allow you to run the program from the console just like any other CLI tool. In this case, running coffee will now allow you to use the coffee-script REPL.

Another important use of npm is dependency management. When you have a node project with a package.json file, you can run npm install from the project root and npm will install all the dependencies listed in the package.json. This makes installing a Node.js project from a git repo much easier! For example, **vows**, a Node.js testing framework, can be installed from git, and its single dependency, **eyes**, can be automatically handled:

Example:
```sh
git clone https://github.com/cloudhead/vows.git

cd vows

npm install
```

After running those commands, you will see a node_modules folder containing all of the project dependencies specified in the package.json.

[NPM crash course](https://www.youtube.com/watch?v=jHDhaSSKmB0&feature=emb_imp_woyt)