---
title: "How to run Nodemon on Windows"
date: 2024-03-22T12:53:27+08:00
draft: false
---

### Installation

To your current working directory then open terminal.

```
npm install nodemon --save-dev
```

If you install nodemon globally on windows it will require more step to let it works, So...we want to install nodemon locally with the `--save-dev` argument.


### Configuration

Open the package.json file. The content may look like this

```json
{
  "devDependencies": {
    "nodemon": "^3.1.0"
  },
  "dependencies": {
    "dotenv": "^16.4.5"
  }
}
```

Then Add the scrips attribute like this.

*Make sure you main program file name is matched with the content.*

`nodemon ${YOUR_MAIN_PROGRAM's FILE NAME}`

```json
{
  "devDependencies": {
    "nodemon": "^3.1.0"
  },
  "dependencies": {
    "dotenv": "^16.4.5"
  },
  "scripts": {
    "start": "nodemon app.js"
  }
}
```

### Start!

That's all! Now you can start the app with command `npm start` and nodemon will detect any file change in the current working directory, if any file changes, it will restart the application.

![](https://i.imgur.com/dTsYzFV.gif)