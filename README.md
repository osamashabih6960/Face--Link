# Face--Link
Project Name: Face Link -LIVE_VIDEO_CHATTING
Description:
This is a live video chat application that makes it easy to create or join group video calls. It leverages modern web technologies for real-time communication.

Technologies used:
Node.js — For the server-side logic.
Socket.io — For real-time, bidirectional communication.
PeerJS (WebRTC) — For peer-to-peer video streaming.
Live Demo:
It mentions a live demo hosted on Heroku (though I can’t access external links directly).

Setup Instructions:
Clone the repository.
Install dependencies with:
bash
Copy
Edit
npm install
Start the server:
bash
Copy
Edit
npm start
Access the app in your browser:
http://127.0.0.1:3030
Future Plans:
Rebuild the front end with React.
Looks like a straightforward, full-stack video chat app! Next, I’ll check server.js to understand how the backend handles signaling and connections. 🚀 ​​

Here’s what the server.js file tells us — it handles the backend logic for the live video chat app!

Backend Setup (Node.js + Express + WebSockets):
Server & Routing:

Uses Express.js to serve static files and handle routes.
On accessing the root URL /, it generates a unique room ID using UUID and redirects to that room.
View Engine:
Uses EJS (Embedded JavaScript) for server-side rendering.

WebRTC Peer Server:
Sets up a PeerJS server at /peerjs to facilitate peer-to-peer connections.

Real-Time Communication with Socket.io:
Listens for WebSocket connections:

Room Management: Users join a room via room ID.
Broadcast Events: When a new user joins, an event is broadcast to other users.
Chat Messaging: Handles chat messages in real time within the room.
Port & Deployment:
Listens on port 3030 (or the port defined in the environment).
