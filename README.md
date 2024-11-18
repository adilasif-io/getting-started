
# HTML Developer Setup Guide

Welcome to the team! This guide will walk you through setting up your development environment for working on HTML projects. Please follow the steps below carefully.

---

## 1. Install **Visual Studio Code (VS Code)**

VS Code is a popular code editor used in our workflow. Follow the instructions below to install it:

- Download VS Code: [Download Here](https://code.visualstudio.com/download)
- Install it on your machine based on your operating system (Windows, macOS, or Linux).

---

## 2. Install **Git**

Git is a version control system used for tracking changes in our projects. You’ll need Git to clone repositories and contribute code.

- **Windows:**
  - Download and install Git from [Git for Windows](https://git-scm.com/download/win).
- **macOS:**
  - Install Git using Homebrew: `brew install git`
- **Linux:**
  - Install Git via your package manager (e.g., `sudo apt install git` on Ubuntu).

---

## 3. Get **Git Credentials**

To access company repositories, you’ll need Git credentials. Send a request to the **Networking Team** for access:

- Subject: "Request for Git Credentials"
- Include your full name, role, and project you're working on.
- The networking team will share your username and password, or provide SSH keys.

Once you receive the credentials, configure Git on your local machine:
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@company.com"
```

---
## 4. Install Relevant Extensions for **VS Code**

To enhance your productivity, you’ll need to install some VS Code extensions.
-   **Handlebars Navigator**: Helps navigate `.html` files easily (if working with Handlebars templating).
-   **Prettier - Code Formatter**: Formats code automatically.
-   **Live Server**: Provides a local development server with live reload.
-   **GitLens**: Extends Git capabilities in VS Code.

**How to install extensions:**
-   Open VS Code and go to the **Extensions** tab (left sidebar or press `Ctrl+Shift+X`).
-   Search for the extension and click **Install**.
---

## 5. Install **NVM (Node Version Manager)**


NVM allows you to manage multiple versions of Node.js on your system. You will use it to install the latest and older versions of Node.js.

> [!TIP]
> We generally use Node 11.14.0 for Legacy Projects and 21.2.0 for latest.

**Windows**: Install NVM via [nvm-windows](https://github.com/coreybutler/nvm-windows/releases).

**macOS/Linux**: Install NVM via terminal:
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
```
Then restart your terminal or run:
```bash
source ~/.bashrc
```
---

## 6. Install the Latest Version of **Node.js**
Once NVM is installed, you can use it to install the latest version of Node.js:

> [!TIP]
> We generally use Node 11.14.0 for Legacy Projects and 21.2.0 for latest.

- Check the latest Node version with:

```bash

nvm ls-remote

```

- Install the latest version by running:

```bash

nvm install node

```

- Set it as the default version:

```bash

nvm use node

```
---

## 7. Install an Older Version of **Node.js** (e.g., 11.14.0)

Sometimes, older versions of Node are required for certain projects. You can install an older version as follows:

```bash

nvm  install  11.14.0

```

To switch between versions:

```bash

nvm  use  11.14.0

```

To confirm the active version of Node:

```bash

node  -v

```
---

## 8. Intro to and Install **Gulp**

**Gulp** is a task runner that automates repetitive tasks like compiling CSS, minifying files, and optimizing images. It helps streamline the development process.


- Install Gulp globally using npm (Node Package Manager):

```bash

npm install -g gulp-cli

```
Once installed, Gulp can be used in your project by setting up a `gulpfile.js`.

---

## 9. Intro to **Gulp Tasks** (Development & Production)

We use Gulp to automate tasks for both **Development** and **Production** environments.


-  **Development Tasks**:

- These tasks involve compiling SCSS, bundling JS, watching files, and launching a local development server with live-reload. Typically, you will run the following command during development:

```bash
gulp development
```

-  **Production Tasks**:

- Production tasks include minification, optimization, and compiling assets for the live site. This prepares your project for deployment:

```bash
gulp production
```
You can find a detailed list of tasks in the `gulpfile.js` in each project repository.
