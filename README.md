[![Made with VueJS](https://img.shields.io/badge/-Made%20with%20Vue.js-4fc08d?&logo=vuedotjs&logoColor=white)](https://vuejs.org/)
![GitHub last commit](https://img.shields.io/github/last-commit/thomasbnt/devtoprofile)
[![Depfu](https://badges.depfu.com/badges/e7801f7df617042ea8647068a675fa8c/count.svg)](https://depfu.com/github/thomasbnt/devtoprofile?project_id=36535)
[![Discord](https://img.shields.io/discord/367753345575944221?color=%237289DA&label=Discord%20server&logo=discord&logoColor=white)](https://thomasbnt.dev/discord)
[![GitHub Sponsors](https://img.shields.io/badge/Sponsor%20me%20on%20GitHub%20-%23EA54AE.svg?&logo=github-sponsors&logoColor=white)](https://github.com/sponsors/thomasbnt) 
[![Twitter Follow](https://img.shields.io/twitter/follow/Thomasbnt_?color=%231DA1F2&label=Follow%20me&logo=Twitter)](https://twitter.com/Thomasbnt_)

# Getting data from the API of DEV.TO

An example of getting data from the dev.to API to display its own articles. Work with **VueJS**, **fetch** and the **[API of dev.to](https://developers.forem.com/api)**.

> **Note**
>
> [See the preview of this project here →](https://devtoprofile.netlify.app/)


[![Preview of this project](https://user-images.githubusercontent.com/14293805/181784516-faf7e76c-0215-42cc-9d1e-6efdcde30c67.png)](https://devtoprofile.netlify.app/)

> **Note**
>
> More projects like that ?  [Check this list](https://github.com/stars/thomasbnt/lists/created-api-stuff).
>
> [![See the list of awesome projects with an API](https://img.shields.io/badge/See%20the%20list%20of%20awesome%20projects%20with%20an%20API%20→-informational?style=for-the-badge)](https://github.com/stars/thomasbnt/lists/created-api-stuff)

## How to get my data ? 

Change this lines in the file **src/components/devto.vue** :

```javascript
const USERID_DEVTO = '18254'
const USERNAME_DEVTO = 'thomasbnt'
```

## How to get my ID ?

Get your ID by using the **website**. Press F12, and on the `body` element,
you have a `data-user` attribute. This is your ID.

![How to get my dev.to ID](https://user-images.githubusercontent.com/14293805/181785438-3a7c74ee-63f8-40b0-9f25-836f72289275.png)

____
## How to develop this project
### Project setup
```bash
yarn install
```

### Compiles and hot-reloads for development
```bash
yarn serve
```

### Compiles and minifies for production
```bash
yarn build
```

### Lints and fixes files
```bash
yarn lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
