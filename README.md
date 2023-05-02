# MERN Infrastructure

## Using MERN Infrastructure to Create MERN-Stack Projects in the Future

Here's the process to create a new MERN-Stack project that starts with the infrastructure code:

 - Clone the mern-infrastructure repo: git clone <url of mern-infrastructure> <name-of-project>
    Note that the folder created will be same as <name-of-project>instead of mern-infrastructure

 - cd <name-of-project>
 - Install the Node modules: npm i
 - Create a .env (touch .env) and add entries for DATABASE_URLand SECRET
 - Update the "name": "mern-infrastructure"in package.json to the name of your project.
 - Create a new repo on your personal GH account.
 - Copy the new GH repo's URL.
 - Update the remote's URL: git remote set-url origin <paste the copied GH url>
 - Push for the first time: git push -u origin main
 - Have fun coding your new project and don't forget to make frequent commits!

## Deploying MERN Infrastructure


### Let's deploy our app!

 1. First let's install cors `npm i cors`
 2. now require cors in your server.js
 3. Mount the cors middleware `app.use(cors())`
 4. Make sure your are serving the static build folder in server.js:

 `app.use(favicon(path.join(__dirname, 'build', 'favicon.ico')));
  app.use(express.static(path.join(__dirname, 'build')));`
  
  and the route:

  `app.get('/*', (req, res) => {
    res.sendFile(path.join(__dirname, 'build', 'index.html'))
})`

 5. 
 6. 