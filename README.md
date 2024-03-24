# ResumeAI

## Overview

The project is a MEAN project and uses node version 18.

###Deploy the Instances for be and fe

- Git clone the backend respository into folder called backend
```bash
  git clone https://github.com/SaiGovardhana/ResumeBuilderBackend.git backend
```
- Move into the directory
```bash
  cd  backend
```
- Install npm dependencies 
```bash
npm i
```
- If your chrome installed skip this,Install follwing dependencies if your running on EC2, , This is for puppetter.
```bash
sudo apt-get install ca-certificates fonts-liberation libappindicator3-1 
libasound2 libatk-bridge2.0-0 libatk1.0-0 
libc6 libcairo2 libcups2 libdbus-1-3 libexpat1 libfontconfig1 libgbm1 libgcc1 
libglib2.0-0 libgtk-3-0 libnspr4 libnss3 
libpango-1.0-0 libpangocairo-1.0-0 libstdc++6
libx11-6 libx11-xcb1 libxcb1 libxcomposite1 libxcursor1 libxdamage1 libxext6 libxfixes3 
libxi6 libxrandr2 libxrender1 libxss1 libxtst6 lsb-release wget xdg-utils
```

- Compile the typescript code, If typescript installed globally
```bash
  tsc
```
- Create a .env file with following fields
```bash
JWT_SECRET_KEY="MYREALLYSECRETKEY"
MONGO_URL="mongodb://MONGO_URL"
OPENAI_KEY="OPENAI_API_KEY"
GMAIL_USER="THIS EMAIL IS USED TO SEND RESUMES"
GMAIL_PASS="PASSWORD USED BY NODEMAILER"
FRONT_END="URL FOR FRONTEND"
```

- Now run the code
```bash
  nohup node src/main/index.js & 
  
  or

  nohup npm start &
```

### Running The Frontend
- Git clone the frontend respository into folder called frontend
```bash
  git clone https://github.com/SaiGovardhana/ResumeBuilderBackend.git backend
```
- Move into the directory
```bash
  cd  frontend
```
- Install npm dependencies 
```bash
npm i
```

- Make sure angular-cli is installed
```bash
npm install -g @angular/cli
```
- Run the application [ In development mode]
```bash
  #This runs the application in development mode 
  #And the backend must be running on port 4292
  #If the port of backend is changed then
  #Edit it in the proxy.conf.json
  
  npm start
  ```
#### Note: Above steps enough to run the application, for better performance or production use below process
- If you want to deploy the application for production
```bash
  ng build
```
- Install angular-http-server globally
```bash
npm i -g angular-http-server

```
- Move to dist folder
```bash
cd dist
```
- Create proxy.js 
```bash
touch proxy.js
```

- Insert the following into it
#### Note: Target points to the backend URL
#### If deployed in same machine using above commands
#### Use localhost:4292
```js
module.exports = {
    proxy: [
        {
            forward: ["api/"],
            target: "localhost:4292",
            protocol: "http",
        }
    ],
};
```
- Run the application to host the static files on port 80, port 80 requires sudo permissions.
```bash
#If port 80
sudo su

#Run the following command.
nohup angular-http-server  -p 80 --config proxy.js &
```

### You have now succesfully deployed the application
### Got to your browser and navigate to localhost

###Now make dashboard to monitor
- Git clone the backend respository into folder called backend
```bash
  git clone https://github.com/SaiGovardhana/ResumeBuilderBackend.git backend
```
- Move into the directory
```bash
  cd  backend
```
- Install npm dependencies 
```bash
npm i
```
- If your chrome installed skip this,Install follwing dependencies if your running on EC2, , This is for puppetter.
```bash
sudo apt-get install ca-certificates fonts-liberation libappindicator3-1 
libasound2 libatk-bridge2.0-0 libatk1.0-0 
libc6 libcairo2 libcups2 libdbus-1-3 libexpat1 libfontconfig1 libgbm1 libgcc1 
libglib2.0-0 libgtk-3-0 libnspr4 libnss3 
libpango-1.0-0 libpangocairo-1.0-0 libstdc++6
libx11-6 libx11-xcb1 libxcb1 libxcomposite1 libxcursor1 libxdamage1 libxext6 libxfixes3 
libxi6 libxrandr2 libxrender1 libxss1 libxtst6 lsb-release wget xdg-utils
```

- Compile the typescript code, If typescript installed globally
```bash
  tsc
```
- Create a .env file with following fields
```bash
JWT_SECRET_KEY="MYREALLYSECRETKEY"
MONGO_URL="mongodb://MONGO_URL"
OPENAI_KEY="OPENAI_API_KEY"
GMAIL_USER="THIS EMAIL IS USED TO SEND RESUMES"
GMAIL_PASS="PASSWORD USED BY NODEMAILER"
FRONT_END="URL FOR FRONTEND"
```

- Now run the code
```bash
  nohup node src/main/index.js & 
  
  or

  nohup npm start &
```

### Running The Frontend
- Git clone the frontend respository into folder called frontend
```bash
  git clone https://github.com/SaiGovardhana/ResumeBuilderBackend.git backend
```
- Move into the directory
```bash
  cd  frontend
```
- Install npm dependencies 
```bash
npm i
```

- Make sure angular-cli is installed
```bash
npm install -g @angular/cli
```
- Run the application [ In development mode]
```bash
  #This runs the application in development mode 
  #And the backend must be running on port 4292
  #If the port of backend is changed then
  #Edit it in the proxy.conf.json
  
  npm start
  ```
#### Note: Above steps enough to run the application, for better performance or production use below process
- If you want to deploy the application for production
```bash
  ng build
```
- Install angular-http-server globally
```bash
npm i -g angular-http-server

```
- Move to dist folder
```bash
cd dist
```
- Create proxy.js 
```bash
touch proxy.js
```

- Insert the following into it
#### Note: Target points to the backend URL
#### If deployed in same machine using above commands
#### Use localhost:4292
```js
module.exports = {
    proxy: [
        {
            forward: ["api/"],
            target: "localhost:4292",
            protocol: "http",
        }
    ],
};
```
- Run the application to host the static files on port 80, port 80 requires sudo permissions.
```bash
#If port 80
sudo su

#Run the following command.
nohup angular-http-server  -p 80 --config proxy.js &
```

### You have now succesfully deployed the application
### Got to your browser and navigate to localhost
- Git clone the backend respository into folder called backend
```bash
  git clone https://github.com/SaiGovardhana/ResumeBuilderBackend.git backend
```
- Move into the directory
```bash
  cd  backend
```
- Install npm dependencies 
```bash
npm i
```
- If your chrome installed skip this,Install follwing dependencies if your running on EC2, , This is for puppetter.
```bash
sudo apt-get install ca-certificates fonts-liberation libappindicator3-1 
libasound2 libatk-bridge2.0-0 libatk1.0-0 
libc6 libcairo2 libcups2 libdbus-1-3 libexpat1 libfontconfig1 libgbm1 libgcc1 
libglib2.0-0 libgtk-3-0 libnspr4 libnss3 
libpango-1.0-0 libpangocairo-1.0-0 libstdc++6
libx11-6 libx11-xcb1 libxcb1 libxcomposite1 libxcursor1 libxdamage1 libxext6 libxfixes3 
libxi6 libxrandr2 libxrender1 libxss1 libxtst6 lsb-release wget xdg-utils
```

- Compile the typescript code, If typescript installed globally
```bash
  tsc
```
- Create a .env file with following fields
```bash
JWT_SECRET_KEY="MYREALLYSECRETKEY"
MONGO_URL="mongodb://MONGO_URL"
OPENAI_KEY="OPENAI_API_KEY"
GMAIL_USER="THIS EMAIL IS USED TO SEND RESUMES"
GMAIL_PASS="PASSWORD USED BY NODEMAILER"
FRONT_END="URL FOR FRONTEND"
```

- Now run the code
```bash
  nohup node src/main/index.js & 
  
  or

  nohup npm start &
```
![Screenshot 2024-03-24 164753](https://github.com/rk630/GCP_Networking_and_Security/assets/139606316/9c3ff4db-67cd-4bc8-868c-3ef2b49faec4)


### Running The Frontend
- Git clone the frontend respository into folder called frontend
```bash
  git clone https://github.com/SaiGovardhana/ResumeBuilderBackend.git backend
```
- Move into the directory
```bash
  cd  frontend
```
- Install npm dependencies 
```bash
npm i
```

- Make sure angular-cli is installed
```bash
npm install -g @angular/cli
```
- Run the application [ In development mode]
```bash
  #This runs the application in development mode 
  #And the backend must be running on port 4292
  #If the port of backend is changed then
  #Edit it in the proxy.conf.json
  
  npm start
  ```
![Screenshot 2024-03-24 164656](https://github.com/rk630/GCP_Networking_and_Security/assets/139606316/6dde51a3-e5f3-44e0-9fb5-b94b6ab6cfa3)

#### Note: Above steps enough to run the application, for better performance or production use below process
- If you want to deploy the application for production
```bash
  ng build
```
- Install angular-http-server globally
```bash
npm i -g angular-http-server

```
- Move to dist folder
```bash
cd dist
```
- Create proxy.js 
```bash
touch proxy.js
```

- Insert the following into it
#### Note: Target points to the backend URL
#### If deployed in same machine using above commands
```js
module.exports = {
    proxy: [
        {
            forward: ["api/"],
            target: "localhost:4292",
            protocol: "http",
        }
    ],
};
```
- Run the application to host the static files on port 80, port 80 requires sudo permissions.
```bash
#If port 80
sudo su

#Run the following command.
nohup angular-http-server  -p 80 --config proxy.js &
```

### You have now succesfully deployed the application
###Use the instances we created above ro make the Dashboards for monitoring purposes
  ![Screenshot 2024-03-24 171326](https://github.com/rk630/GCP_Networking_and_Security/assets/139606316/b337270b-b624-4b65-bb61-1f02fee97a8a)
![Screenshot 2024-03-24 171900](https://github.com/rk630/GCP_Networking_and_Security/assets/139606316/a2e4ad25-344f-49e5-9fb1-23ccaa58a37c)
![Screenshot 2024-03-24 171613](https://github.com/rk630/GCP_Networking_and_Security/assets/139606316/96c6f993-0f14-45c3-bc83-39ef8541d626)

