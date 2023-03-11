---
sidebar_position: 2
---

# Environment Variables

Environment variables provide information about the environment in which the process is running. We use Node environment variables to handle sensitive data like API keys, or configuration details that might change between runs.

```
NODE_ENV = development
```

## Connect to MongoDB

By default, Discuzz will use your local MongoDB server and the `discuzz` database will be created automatically when the app is run in development mode. In production mode, you should use a cloud database like [MongoDB Atlas](https://www.mongodb.com/atlas/database).

```
MONGO_URI = mongodb+srv://{username}:{password}@node.deu00vc.mongodb.net/{dbname}?retryWrites=true&w=majority
```

## Cloudinary

We rely on Cloudinary service to store all media uploaded by users, follow the instructions below to getting started with Cloudinary:

- Create [Cloudinary Account](https://cloudinary.com/) for free and you will get **Product Environment Credentials** like Cloud Name, API Key, and API Secret.
- Open the **Media Library** then create `avatars` and `chat` folders.

```
CLOUDINARY_API_KEY =
CLOUDINARY_API_SECRET =
CLOUDINARY_CLOUD_NAME =
```

## Nodemailer

We use [Nodemailer](https://nodemailer.com/about/) to send OTP code via email, use your email address and App Password to run Nodemailer, follow the instructions below to generate your App Password:

- Go to your [Google Account](https://myaccount.google.com/) > **Security** > **2-Step Verification**
- At the bottom, choose **Select app** and choose Other (custom name) > give this App Password a name, e.g. "Nodemailer" > **Generate**
- Follow the instructions to enter the App Password. The App Password is the 16-character code in the yellow bar on your device
- **Done**

```
EMAIL_USER = your@gmail.com
EMAIL_PASS =
```

## Fake SMTP Server

There are many fake SMTP server services to test your email but I recommend using [Mailtrap](https://mailtrap.io), this variable will only be executed in development mode.

```
TEST_EMAIL_USER =
TEST_EMAIL_PASS =
TEST_EMAIL_HOST = smtp.mailtrap.io
TEST_EMAIL_PORT = 2525
```
