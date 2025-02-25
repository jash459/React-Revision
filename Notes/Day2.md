# Day 2 of revising React

Today, I've first separated the HTML, JS, and CSS files to maintain separation of concerns. Today, I created my own "create_react_app" to make my app production-ready.

To make it production-ready, I needed to minify the code, optimize the app, bundle it, and run it on a server. React is a powerful tool, but it cannot do everything alone. That's why we use bundlers like Vite, Parcel, and Webpack to get the desired functionality.

In this project, I'm using Parcel as my bundler because it is zero-config and provides a lot of features for our app. To use Parcel in our app, we need a package manager, and I'm using npm. npm and yarn are the most commonly used package managers in the market, but I chose npm for this project.

To install npm in our app, we use the command `npm init` or `npm init -y` to skip all the questions. Once npm is installed, we'll see a `package.json` file along with our existing files.

The `package.json` file contains metadata about our project, including the dependencies required for our app. We can use this file to install external packages in our application.

To install Parcel in our app, we use the command `npm install -D parcel`. The `-D` flag installs the package as a dev dependency.

When we install a package, we'll get a `package-lock.json` file in our app, which ensures that our app uses the exact version of the package.

The caret (^) and tilde (~) signs in front of version numbers indicate which versions of a package are compatible with our app.

The `node_modules` file is like a database for npm. It contains all the packages and dependencies installed in our app. It's essential to put the `node_modules` file in the `.gitignore` folder to avoid uploading it to version control.

To install React and React-DOM, we use the command `npm install react react-dom`. We'll remove the CDN links that we used before and use these installed packages.

To run our app, we use the command `npx parcel index.html`, which creates a mini server to run our app on `localhost:1234`.

The `dist` folder contains the production-ready build of our app, and the `parcel_cache` folder contains cached files generated by Parcel during development.

We can make a production build using `npx parcel build index.html` and a development build using `npx parcel index.html`. It's essential to put the `dist` and `parcel_cache` folders in the `.gitignore` folder to avoid uploading them to version control.

I also learned about Browserlist, which is a feature in package.json that allows you to specify which browsers you want to support for your project. By default, it uses a list of commonly used browsers and their versions. However, you can customize this list to better suit your needs. This is important because different browsers may have different capabilities and may require different features or polyfills to work properly. By specifying which browsers you want to support, you can ensure that your project will work correctly for your target audience.

Here's an example of how to specify a Browserlist in your package.json file:

```json
{
  "name": "my-project",
  "version": "1.0.0",
  "browserslist": ["last 2 versions", "not dead"],
  "dependencies": {
    "react": "^17.0.2",
    "react-dom": "^17.0.2"
  }
}
```

In this example, we are specifying that we want to support the last two versions of all major browsers, except for any that are considered "dead" (i.e. no longer supported). You can customize the list to fit your specific needs by specifying different versions or browser names. The Browserslist documentation provides more information on how to use this feature.

Finally, I learned all the features of Parcel, including -

- HMR (Hot Module Replacement): Enables real-time changes to your code without needing to refresh the entire page, making development faster and more efficient.
- File watcher algorithm in C++: A performant file watcher that efficiently tracks changes to your code and rebuilds only what's necessary.
- Bundling: Combines all of your code and dependencies into a single file, making it easier to deploy and reducing page load times.
- Code minification: Reduces the size of your code by removing unnecessary whitespace and renaming variables, making it faster to download and execute.
- Image optimization: Automatically optimizes images to reduce their size without sacrificing quality, improving page load times.
- Caching: Speeds up development by caching assets and only rebuilding when necessary, improving build times.
- Compression: Reduces the size of your assets, making them faster to download and improving page load times.
- Tree shaking: Eliminates unused code from your final build, reducing its size and improving performance.
