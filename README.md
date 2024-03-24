# ResumeAI

## Overview

The project is a MEAN project and uses node version 18.

###Deploy the Instances for be and fe

- Git clone the backend respository into folder called backend
```bash
  git clone https://github.com/rk630/GCP_Networking_and_Security
```
- Move into the directory
```bash
  cd  backend
```
- Install npm dependencies 
```bash
npm i
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

or

npm start
```
![Screenshot 2024-03-24 164753](https://github.com/rk630/GCP_Networking_and_Security/assets/139606316/6266d260-ae69-4b56-a5c7-bdd75f4b2526)

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
![Screenshot 2024-03-24 164656](https://github.com/rk630/GCP_Networking_and_Security/assets/139606316/3543a24e-3e9c-4df2-b8c0-f517d29fd80e)

### Application is now succesfully deployed
### Use the instances we created to make the Dashboards for monitoring purposes
![Screenshot 2024-03-24 170322](https://github.com/rk630/GCP_Networking_and_Security/assets/139606316/ace9dedc-48e2-46b2-bb40-53f86fccf6b0)

![Screenshot 2024-03-24 171900](https://github.com/rk630/GCP_Networking_and_Security/assets/139606316/a2e4ad25-344f-49e5-9fb1-23ccaa58a37c)
![Screenshot 2024-03-24 171613](https://github.com/rk630/GCP_Networking_and_Security/assets/139606316/a28508ee-3233-4719-b954-49b9ab6b64e6)


