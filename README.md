<h1># 💬 Real-Time Chat Application using Socket.IO</h1>

<P>This is a simple real-time chat application built using **Node.js**, **Express**, and **Socket.IO**. It allows multiple users to send and receive messages instantly.</P>

---

## 🚀 Features

* Real-time messaging
* Multiple users support
* Simple and clean UI
* Built with Socket.IO for fast communication

---

## 🛠️ Tech Stack

* Node.js
* Express.js
* Socket.IO
* HTML, CSS, JavaScript

---

## 📂 Project Structure

```
project-folder/
│
├── public/
│   ├── index.html
│
├── index.js
└── README.md
```

---

## ⚙️ Installation & Setup

### 1. Clone the repository

```bash
git clone https://github.com/your-username/your-repo-name.git
```

### 2. Navigate to project folder

```bash
cd your-repo-name
```

### 3. Install dependencies

```bash
npm install
```

### 4. Run the server

```bash
node index.js
```

---

## 🌐 Run the Application

Open your browser and go to:

```
http://localhost:9000
```

---

## 🔌 How it Works

* Server listens for socket connections
* When a user sends a message:

  * Event: `user-message`
  * Server broadcasts it using: `io.emit()`
* All connected clients receive the message instantly

---

## 📌 Important Code Snippet

```javascript
io.on("connection", (socket) => {
    socket.on("user-message", (message) => {
        io.emit("message", message);
    });
});
```

---

## ⚠️ Notes

* Make sure port **9000** is free
* Ensure `public` folder contains `index.html`
* Socket.IO client must be included in frontend

---

## 📈 Future Improvements

* Add usernames
* Private messaging
* Message timestamps
* Database integration

---

## 🤝 Contributing

Feel free to fork and improve this project.

---

## 📄 License

This project is open-source and free to use.
