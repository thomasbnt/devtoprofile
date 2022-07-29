# Getting data from the API of DEV.TO

> An example of getting data from the dev.to API to display its own articles.


| [Preview the project](https://thomasbntdevto.netlify.app/) |
|------------------------------------------------------------|

[![Preview of this project](https://user-images.githubusercontent.com/14293805/181784516-faf7e76c-0215-42cc-9d1e-6efdcde30c67.png)](https://thomasbntdevto.netlify.app/)

Work with **VueJS**, **fetch** and the **[API of dev.to](https://developers.forem.com/api)**.

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
```
yarn install
```

### Compiles and hot-reloads for development
```
yarn serve
```

### Compiles and minifies for production
```
yarn build
```

### Lints and fixes files
```
yarn lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
