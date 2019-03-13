### From site-point book Crud with Vue, Mongo

- Installed latest node 10.15.3, mongo 4.0.6 with Compass
- Add mongo to PATH
- Run with mongod --dbpath="C:\dataMongo\"
- Interactive shell with 'mongo'
- Installed latest Postman, v7.0.5

mkdir -p vocab-builder/server/api/{controllers,models,routes}

```
.
└── server
    ├── api
    │   ├── controllers
    │   │   └── vocabController.js
    │   ├── models
    │   │   └── vocabModel.js
    │   └── routes
    │       └── vocabRoutes.js
    ├── package.json
    └── server.js
```
```
cd server
    npm init -y

npm i express cors body-parser mongoose
npm i nodemon --save-dev

server code
const express = require('express');
const port = process.env.PORT || 3000;
const app = express();

app.listen(port);

app.get('/', (req, res) => {
  res.send('Hello, World!');
});

console.log(`Server started on port ${port}`);
```

Add routes
- GET /words—return a list of all words
- POST /words—create a new word
- GET /words/:wordId—get a single word
- PUT /words/:wordId—update a single word
- DELETE /words/:wordId—delete a single word

Add model, routes and controller code

Can then use Postman to test

//===============

npm install -g @vue/cli

In top directory, vue create client

No vuex
- ? Please pick a preset: Manually select features
- ? Check the features needed for your project: Babel, Router, Linter
- ? Use history mode for router? Yes
- ? Pick a linter / formatter config: ESLint with error prevention only
- ? Pick additional lint features: Lint on save
- ? Where do you prefer placing config for Babel etc.? In dedicated config files
- ? Save this as a preset for future projects? No

rm files generated files in frontend dir

make this structure
```
.
├── App.vue
├── assets
├── components
│   ├── VocabTest.vue
│   └── WordForm.vue
├── helpers
│   └── helpers.js
├── main.js
├── router.js
└── views
    ├── Edit.vue
    ├── New.vue
    ├── Show.vue
    ├── Test.vue
    └── Words.vue
```

npm i axios semantic-ui-css vue-flash-message

will build these
- /words—display all the words in the database
- /words/new—create a new word
- /words/:id—display a word
- /words/:id/edit—edit a word
- /test—test your knowledge

Code added was just pasted in...
