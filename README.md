# BlogPlace

A place for memory keeping. We should start a daily writing habit.

The following features are used to create BlogPlace.

```
mongoDB
mongoose
ejs
express
Bootstrap
```

## Installation

Install [node]https://nodejs.org/en/ 

Use the npm package manager to install packages.

```bash
npm install
```

Install [mongoDB]https://www.mongodb.com/try/download/community

Now, we need to create a database folder for mongoDB

```
C:\data\db
```

Next, set up the environment variable in .bash_profile

```bash
# create .bash_profile
touch .bash_profile

# open .bash_profile
vim .bash_profile

# click 'i' to edit .bash_profile

# declare alias in the bash_profile
alias mongod="/c/Program\ Files/MongoDB/Server/4.4/bin/mongod.exe"
alias mongo="/c/Program\ Files/MongoDB/Server/4.4/bin/mongo.exe"

# 4.4 is the version number of your mongoDB, check the version number in C:\Program Files\MongoDB\Server
# :wq! to exit
```
Type the following command to make sure the setup is succeed.

```bash
# return mongoDB version
mongo --version
```

## Usage

Run the following command to connect to mongoDB server.

```bash
# start the mongo process and run in the background
mangod 
```

Run the BlogPlace

```bash
# Node server will run on port 3000
nodemon app.js 
```

Go to http://localhost:3000/ 

Click 'Compose' on the navigation bar and write your first blog post.

Click on the 'Publish' button and your blog post will be published on the homepage.


## Extra Information

Run the following command to get into mongo shell and check your database list.

```bash 
# it defaults to connecting to the localhost on port 27017
mango  

# return a list of available database
show dbs 
```

Run the following command to check your blog content.

```bash
# switch to blogDB
use blogDB

# list out the available collections
show collections

# list out the data (blog title and content)
db.posts.find()
```