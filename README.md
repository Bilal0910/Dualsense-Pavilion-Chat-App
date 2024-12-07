DualSense Pavilion Project - README
Introduction
The DualSense Pavilion is a custom-built interactive communication platform designed to simulate a real-time chat experience, focusing on the use of Socket.IO to enable real-time web functionality. The platform allows users to join rooms, send messages, and share their real-time location with others.

Project Overview
The DualSense Pavilion provides an interactive web chat environment where users can join various rooms and engage in real-time conversations. Each user can send text messages and share their location through the use of Socket.IO and dynamic templates. The platform allows for easy scalability, as new users can join rooms without disrupting the real-time communication between others. While the platform's front-end interface facilitates communication, the main focus of this project is on the Socket.IO setup and server-side logic to handle events, message broadcasting, and user connections.

Core Features:
Real-time Messaging: Messages are sent and received in real-time using Socket.IO.
Location Sharing: Users can share their current location via Socket.IO, which creates a dynamic, interactive experience.
User Management: Each room has a dynamic list of users, which updates in real-time as users join or leave.
Technology Stack
Frontend:
HTML, CSS, and JavaScript for building the user interface.
Socket.IO-client: JavaScript library for real-time web applications.
Backend:
Node.js: Server-side environment to handle Socket.IO connections and user management.
Socket.IO: Real-time communication library used for bi-directional communication between the client and the server.

ey Features
Real-time Chat
The core functionality of the DualSense Pavilion is real-time chat. Using Socket.IO, every message sent is instantly broadcasted to all users connected to the same chat room, allowing for seamless communication.

Room Management
Each user can join a specific room, where the list of users in the room updates dynamically. When a user joins or leaves, the system reflects the change in real-time through the Socket.IO connection.

Location Sharing
Users can also send their current location, which is fetched from the browser's geolocation API. The location is shared as a clickable link, which opens in a new tab showing the user's current position on Google Maps.

Socket.IO Integration
How Socket.IO Works in This Project:
The Socket.IO library plays a pivotal role in enabling real-time interaction between users. Here’s how it’s used in the DualSense Pavilion:

Socket.IO Server:

The Node.js server uses Socket.IO to handle connections and communication. The server listens for events (like user joining a room or sending a message) and emits events back to the connected clients.
It handles broadcasting messages to all users in a room and managing which users are currently online in each room.
Socket.IO Client:

The frontend uses Socket.IO-client to listen for incoming messages and broadcast them to the server. The client connects to the server on page load and listens for any updates to the chat room, such as new messages or user list changes.
For real-time location sharing, the client listens for location-sharing events and displays the location on a Google Maps link.

Installation & Setup
Prerequisites:
Node.js installed on your system.
A package manager like npm or yarn.

Usage
Once the app is running, you can:

Join a chat room by entering a room name.
Send messages in real-time to everyone in the same room.
Send your location, which can be viewed by other users as a clickable link to Google Maps.

Future Enhancements
User authentication: Implement user login and registration to track user identities across rooms.
Private messages: Allow private one-on-one chats between users.
Message history: Store past messages in a database so users can view chat history when rejoining a room.
Message editing and deletion: Allow users to edit or delete their messages after sending them.
