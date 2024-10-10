# Mern-Tutorial-
# MERN Stack Application Deployment Guide

## 1. Clone the Repository

First, clone the repository from GitHub:

```bash
git clone https://github.com/bradtraversy/mern-tutorial
```

## 2. Install Node.js

Install Node.js using Node Version Manager (NVM). Follow these steps:

### Install NVM (Node Version Manager)
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.0/install.sh | bash
```

### Install Node.js (v20.x)
After installing NVM, restart your terminal, then run:
```bash
nvm install 20
```

### Verify Node.js and NPM Versions
To confirm installation, check the versions:
```bash
node -v    # should print v20.18.0
npm -v     # should print 10.8.2
```

## 3. Setup Environment File

Rename the `.envexample` file to `.env`:

```bash
mv .envexample .env
```

Then, edit the `.env` file and add the following:

```bash
NODE_ENV = production
PORT = 5000
MONGO_URI = mongodb://localhost:27017
JWT_SECRET = abc123
```

## 4. Install MongoDB

Follow the MongoDB installation guide for Ubuntu from the official MongoDB documentation:  
[Install MongoDB on Ubuntu](https://www.mongodb.com/docs/manual/tutorial/install-mongodb-on-ubuntu/)

You can also install it using these commands:

### Step-by-Step Installation

1. Install prerequisites:

    ```bash
    sudo apt-get install gnupg curl
    ```

2. Add MongoDB GPG Key:

    ```bash
    curl -fsSL https://www.mongodb.org/static/pgp/server-8.0.asc | \
    sudo gpg -o /usr/share/keyrings/mongodb-server-8.0.gpg --dearmor
    ```

3. Add MongoDB to your source list:

    ```bash
    echo "deb [ arch=amd64,arm64 signed-by=/usr/share/keyrings/mongodb-server-8.0.gpg ] https://repo.mongodb.org/apt/ubuntu noble/mongodb-org/8.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-8.0.list
    ```

4. Update the package database:

    ```bash
    sudo apt-get update
    ```

5. Install MongoDB:

    ```bash
    sudo apt-get install -y mongodb-org
    ```

6. Start MongoDB:

    ```bash
    sudo systemctl start mongod
    ```

7. Enable MongoDB to start on boot:

    ```bash
    sudo systemctl enable mongod
    ```

8. Check the MongoDB status:

    ```bash
    sudo systemctl status mongod
    ```

--- 
