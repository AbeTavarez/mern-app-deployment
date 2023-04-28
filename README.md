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

### First let's click up the app a bit.

- Remove server-favicon `npm remove server-favicon`

- In server.js delete the server-favicon import `const favicon = require('serve-favicon');`

- Remove the app.use statement `app.use(favicon(path.join(__dirname, 'build', 'favicon.ico')));`

- Remove the build folder statement: `app.use(express.static(path.join(__dirname, 'build')));`

- Finally remove the 'catch all route': 
<code>
app.get('/*', (req, res) => {
    res.sendFile(path.join(__dirname, 'build', 'index.html'))
})
</code>

- Save your files, commit and push.

### Let's deploy our app!

 1. Go to  https://www.cyclic.sh/ and sign-up using your Github Account.
 2. Click on Create a new app or Deploy now.
 3. Click on Link Your Own
 4. Select your repo name.
 5. Click on Connect Cyclic
 6. Allow Cyclic to connect to your Github repo.