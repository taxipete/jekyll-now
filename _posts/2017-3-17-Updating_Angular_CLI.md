---
layout: post
title: Updating the Angular2 CLI
---

Recently had some issues when I updated the angular2 CLI. Should have followed the instructions!
I got the error message “Module build failed: TypeError: Cannot read property ‘newLine’ of undefined”.

When you update the Angular2 CLI you need to update any of the projects you are working on as well.
Full instructions can be found [here](https://github.com/angular/angular-cli#updating-angular-cli)

To update Angular CLI to a new version, you must update both the global package and your project's local package.

Global package:
```bash
npm uninstall -g @angular/cli
npm cache clean
npm install -g @angular/cli@latest
```

Local project package:
You need to remove you node_modules and any old dist files
```bash
rmdir /S/Q node_modules
npm install --save-dev @angular/cli@latest
npm install
```
