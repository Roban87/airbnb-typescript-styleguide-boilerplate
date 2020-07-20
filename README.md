# How to automatically apply AirBnB style guide to your TypeScript project

- go to your project's root folder and run `npm init` if no package.json exists in your project's root folder
- run
```shell script
npm install --save-dev @typescript-eslint/eslint-plugin @typescript-eslint/parser eslint eslint-config-airbnb-base eslint-config-prettier eslint-import-resolver-typescript eslint-plugin-import eslint-plugin-json eslint-plugin-prettier prettier
```
- copy `.eslintrc.js` from this repository to your project's root folder
- Add the following to your `package.json`
```text
"scripts": {
  "lint": "eslint . --ext .ts"
}
```

- Install the following Visual Studio Code extensions
```text
dbaeumer.vscode-eslint
esbenp.prettier-vscode
```

- Add the following to your Visual Studio Code `settings.json`
```text
"[typescript]": {
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": false
},
"eslint.autoFixOnSave": true,
"eslint.validate": [
  {
    "autoFix": true,
    "language": "typescript"
  }
],
"prettier.eslintIntegration": true,
```

## Source
More detailed [article](https://levelup.gitconnected.com/setting-up-eslint-with-prettier-typescript-and-visual-studio-code-d113bbec9857)
extended with JS and React.
