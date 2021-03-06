*UPDATE Sept 2016:* lol literally a day after I did this, create-react-app updated w/ Jest support, so this isn't necessary for new create-react-app projects. But will keep this up anyway.


# How to use Jest with `create-react-app`

This repo contains an example of how you can modify the output of [create-react-app](https://facebook.github.io/react/blog/2016/07/22/create-apps-with-no-configuration.html) to use Jest for testing.

1. Use create-react-app [like normal](https://facebook.github.io/react/blog/2016/07/22/create-apps-with-no-configuration.html)
```
npm install -g create-react-app
create-react-app hello-world
```

2. Install Jest dependencies
```
npm install --save-dev jest babel-jest babel-preset-es2015 babel-preset-react react-test-renderer jest-cli
```

3. Update your hello-world app with the following to make it match the contents of this repo:

  - [`.babelrc`](.babelrc): Add this file to the directory that also contains `package.json`
  - [`package.json`](package.json): Update the `"test"` line and add the `"jest"` section to the existing `package.json` file
  - [`test/`](test/): Add this directory to the directory that also contains `package.json` 
  - [`src/__tests__`](src/__tests__): Add this directory `__tests__` to the `src/` directory

4. Run tests

```
npm test
```

That should do it!
