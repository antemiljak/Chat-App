#Chat App

## General Information

### Project Overview

This is a real-time **Chat Application** built with the **MERN** stack (MongoDB, Express.js, React, Node.js). The application enables users to send and receive messages in real-time, with a simple, modern user interface built using **TailwindCSS** and **DaisyUI** for styling. 

The app allows users to create accounts, send messages, view chat history, and receive notifications for new messages. The state management is handled using **Zustand**, and notifications for actions (like sending or receiving messages) are handled with **React-Hot-Toast**.

App is still in progress.

### Key Features
- **Real-time Messaging**: Users can send and receive messages in real-time.
- **User Authentication**: Secure login and registration system.
- **Message History**: Access to a list of past messages with users.
- **Responsive UI**: The app is fully responsive and works on both desktop and mobile devices.
- **Toast Notifications**: Alerts and notifications for actions using React-Hot-Toast.
- **User Profiles**: Users can view and edit their profiles.
- **Interactive UI**: The app utilizes **TailwindCSS** and **DaisyUI** for an intuitive and visually appealing interface.
- **Routing**: The app uses **React Router DOM** for seamless navigation between pages.

### Technologies Used
- ![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white) **MongoDB**: NoSQL database for storing user and chat data.
- ![Express.js](https://img.shields.io/badge/Express.js-000000?style=flat&logo=express&logoColor=white) **Express.js**: Web framework for building the server-side of the app.
- ![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black) **React**: JavaScript library for building the frontend of the app.
- ![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=node.js&logoColor=white) **Node.js**: JavaScript runtime for building the backend of the app.
- ![TailwindCSS](https://img.shields.io/badge/TailwindCSS-38BDF8?style=flat&logo=tailwind-css&logoColor=white) **TailwindCSS**: Utility-first CSS framework for fast and responsive design.
- ![DaisyUI](https://img.shields.io/badge/DaisyUI-0B6E4F?style=flat&logo=tailwindcss&logoColor=white) **DaisyUI**: Component library for building beautiful UI elements with TailwindCSS.
- ![Zustand](https://img.shields.io/badge/Zustand-8E5F5B?style=flat&logo=redux&logoColor=white) **Zustand**: A minimalistic state management library for React.
- ![React-Hot-Toast](https://img.shields.io/badge/React%20Hot%20Toast-000000?style=flat&logo=react&logoColor=white) **React-Hot-Toast**: Library for easy and customizable toast notifications in React.
- ![React Router DOM](https://img.shields.io/badge/React%20Router%20DOM-CA4245?style=flat&logo=react-router&logoColor=white) **React Router DOM**: For handling client-side routing and navigation.

## Database Model
The application uses MongoDB for storing user data and routes. Below are the key schemas:

### User Model:
```javascript
const userSchema = new mongoose.Schema(
  {
    email: {
      type: String,
      required: true,
      unique: true,
    },
    fullName: {
      type: String,
      required: true,
    },
    password: {
      type: String,
      required: true,
      minlength: 6,
    },
    profilePic: {
      type: String,
      default: "",
    },
  },
  { timestamps: true }
);
```

### Message Model:
```javascript
const messageSchema = new mongoose.Schema(
  {
    senderId: {
      type: mongoose.Schema.Types.ObjectId,
      ref: "User",
      required: true,
    },
    receiverId: {
      type: mongoose.Schema.Types.ObjectId,
      ref: "User",
      required: true,
    },
    text: {
      type: String,
    },

    image: {
      type: String,
    },
  },
  { timestamps: true }
);
```
## Deployed Version

Still in progress...
