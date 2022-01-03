#EOS ICONS 

### EOS ICONS - It picks up the icons that you want 
[![Open Source Love svg2](https://badges.frapsoft.com/os/v2/open-source.svg?v=103)](https://github.com/ellerbrock/open-source-badges/)


## Discription:
When an icon is picked in the frontend ,a trigger is created and the middleware lets us connect to our database when the icon is fetched .Our backend/database is Mongodb and middleware is redis .

## Pre-requisites :
- Docker , MongoDB , MongoDB Compass ,Redis 



- Any IDE tool that lets you edit and run different types of files. I used _VisualStudio Code_ as my IDE tool.

## Steps to run the project

- Cloning the repo:
````
git clone https://github.com/EOS-uiux-Solutions/eos-icons-api
````
- Once the repository is cloned, You can choose the way you prfer: 
- We can run the project in two ways , throught docker or through npm.
- If running throught docker make sure to have the version that is compatable with the OS you are working with .

### | Using Docker: 
  By using our docker image, we will take care of everything</br> 
  - **Steps**:
    - Make sure that docker is installed in your device
    - Modify the `REDISCLOUD_URL` enviroment variable to `redis://redis:6379` (For the server to connect to the redis image)
    - Modify the `MongoURI` enviroment variable to `mongodb://mongo:27017/eosiconsdb` (For the server to connect to the mongo image)
    - From within the cloned respository run the following command to build the image: </br>
  ````
  docker-compose up
  ````
  - Your server container will be started at `http://localhost:3131`
  - Mongo database can be accessed from MongoDB compass at `mongodb://mongo:27017/eosiconsdb`

### | Running on your machine:
  - **Steps**:
    - Install the required python dependencies:
      - On OSX: 
        ```
        brew install ttfautohint fontforge --with-python
        ```
        You will need to have Xcode installed. First install the command line tool:

        ```
        xcode-select --install
        ```

        And then download the latest version from:

        https://developer.apple.com/xcode/
      
      - On Linux: 
        ```
        sudo apt-get install fontforge ttfautohint
        ```
    - Install MongoDB: 
      https://docs.mongodb.com/manual/installation
    - Install Redis: 
      https://redis.io/topics/quickstart
    - Install the dependenices and run the server: 
    1. Install dependencies using `npm install`
    2. Install grunt globally `npm install -g grunt-cli`
    3. Start the server using `npm start`
    - Your server will be started at `http://localhost:3131`


## Contributing: 

- Follow the instructions in the previous section for the installation 
- Make sure to run the tests after any modification, or add new one for any addition. 
1. For `V1` APIs we're using Postman tests, which can be started using `npm run test:v1`
2. For `V2` APIs we're using Mocha tests, which can be started using `npm run test:v2`
3. You can test All the APIs using `npm run test` 
4. Make sure all the dependencies mentioned in the _package.json file_ are getting installed while running  npm .


## Learn more about the EOS Design System

* [EOS Design System](https://www.eosdesignsystem.com/)

* [EOS Icons](icons.eosdesignsystem.com/)

* [Follow us on Twitter](https://twitter.com/eosdesignsystem)

* [Join us in Slack](https://slack.eosdesignsystem.com)



## notes:
I implemented this project using/on:
- Ubuntu 20.4 Debian
- VisualStudio code version - 1.63.0
- Docker version -20.10.11, build dea9396
- MongoDB - db version v5.0.4
- Redis - Redis server v=5.0.7 sha=00000000:0 malloc=jemalloc-5.2.1 bits=64 build=636cde3b5c7a3923
- npm version - 6.14.4




