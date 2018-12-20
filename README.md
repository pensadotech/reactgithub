# Create React project and deploy to GitHub (no DB)

_How to deploy a REACT (with no DB) application in Github_


## Steps

The following are my personal steps when creating a github page

1. Open gitbash and move to a folder in which the project folder will be created as a child folder.

2. Create the React project using the command below. This will create the project folder. Wait until _"Happy hacking"_ message shows in the terminal.
```js
npx create-react-app <projectname> 
```

3. Open the project folder in VS Code.

4. Create a new Githhub repository at your github sapces (https://github.com).

5. In VS Code open the terminal and initialize the project for GitHub:
```js 
git init
```

6. Add everything to git:
```js  
git add -A 
```

7. Make an initial commit: 
```js
git commit -m "my first commit"
```

8. Connect the local project with the remote repository
```js
git remote add origin https://github.com/<your_name>/<your_project>.git
```

9. Push the project to remote repository
```js
git push --set-upstream origin master 
Note: can use 'dev' instead of 'master'

Optional: git push -u origin master
```

10. Pull the report to sync local folder 
```js
git pull 
```

11. Add github pages npm 
```js
   npm i gh-pages
```

12. Refrence the github pages inside **package.json** in the main section,under the _"name"_ property: 
```js
"homepage" : "https://<your_name>.github.io/<your_project>"
```

13. Commit all and push all again throug VS Code or using terminal commands.

14. Build the React project
```js
npm run build
```

15. Add a deploy command inside package.json, under scripts section.
```js 
"deploy": "gh-pages -d build"
```

16. Deploy the project to github,
```js
npm run deploy
```

17. After any changes and when ready for new deployment execute

		a. Build the project: **npm run build**
		b. Commit all changes.
		c. Push the changes
		d. Delpoy: **npm run deploy**


## Additional information

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.<br>
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br>
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.<br>
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.<br>
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br>
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (Webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).


