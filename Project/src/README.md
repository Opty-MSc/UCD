# Alexandria's Library

## Prerequisites:
- **Postgresql**: Installation [link](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-20-04) on Ubuntu 20.04 (Used `psql` version: 12.9);
- **Nodejs**: Installation [link](https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-20-04) (Option 3) on Ubuntu 20.04 (Used `node` version: 14.18.2) (Used `npm` version: 6.14.15);
- **Expo CLI**: Installation [link](https://docs.expo.dev/get-started/installation/) (Used `expo` version: 5.0.1).

## Steps to get the system running:
To run the Backend:
- [Generate](https://console.firebase.google.com/project/_/settings/serviceaccounts/adminsdk) a private key file for your Firebase service account and place it in the `Backend/config/serviceAccountKey.json` file;
- After that, run the following commands in the *Backend* directory:
```s
sh resources/newDB.sh
npm install
npm start
```
To run the Frontend:
- Create an `.env` file in the *Frontend* directory and set the variable:
    - `SERVER_BASE_URL`: Match `http://<P>:3000` where `<P>` is the private IP of the PC where the Backend is running;
    - `FIREBASE_WEB_API_KEY`: [Firebase Web API Key](https://console.firebase.google.com/project/_/settings/general/).
- After that, run the following commands in the *Frontend* directory:
```s
npm install
npm start
```
