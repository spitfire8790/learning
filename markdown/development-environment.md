# Development Environment

## 1. Required tools installation

### Integrated development editor (IDE)

Visual Studio Code (VS Code) is a primary code editor, think of it as your workbench where you'll spend most of your time crafting code.

### Node.js and npm

Node.js is like a workshop that lets JavaScript run outside of browsers, and npm (Node Package Manager) is your tool organizer that helps manage project dependencies.

## 2. Project creation

``` bash
# Create project directory
mkdir my-app #mkdir stands for "Make Directory'
cd my-app # Changes directory to my-app
```

``` bash
# Initialise a new project with Vite
npm create vite@latest .
```

When prompted:

1. Choose a project name
2. Select "React" as framework
3. Choose "Javascript" for now

After creation, install dependencies:

`npm install`

## 3. Understanding project structure

    my-app/
    ├── node_modules/    (Your project's dependencies live here)
    ├── public/          (Static files that don't need processing)
    ├── src/             (Your source code goes here)
    │   ├── App.jsx      (Main application component)
    │   ├── main.jsx     (Entry point of your application)
    │   └── index.css    (Global styles)
    ├── index.html       (The single HTML file that loads everything)
    ├── package.json     (Project configuration and dependencies)
    └── vite.config.js   (Build tool configuration)

## 4. Running the app

In the terminal, run:

`npm run dev`

