# WebRTC Video Calling

![WebRTC](https://img.shields.io/badge/WebRTC-Video%20Calling-blue) ![Node.js](https://img.shields.io/badge/Node.js-v16.x-green) ![Socket.IO](https://img.shields.io/badge/Socket.IO-Realtime%20Communication-brightgreen) ![License](https://img.shields.io/badge/license-MIT-green)

## Project Overview

This project implements a **WebRTC**-based video calling application where users can create and join video call rooms for peer-to-peer (P2P) communication. The application uses **Socket.IO** for signaling and **WebRTC** to establish direct, real-time connections between users. By entering a **unique room name** and **email**, users can connect with others, and once two users enter the same room, they can initiate a video call.

### Key Features
- **Room Creation**: Allows users to create a unique room for video calls.
- **Real-Time Signaling**: Utilizes Socket.IO for signaling, room management, and message exchange between users.
- **Peer-to-Peer Communication**: Establishes direct P2P video calls using WebRTC after signaling.
- **Secure Communication**: The video call is encrypted, ensuring secure communication between users.
- **End-to-End Video Call**: Users can see and hear each other in real-time.

## Technologies Used

- **WebRTC** - Peer-to-peer real-time video and audio communication.
- **Socket.IO** - Real-time communication for signaling and room management.
- **Node.js** - Backend runtime for the signaling server.
- **Express.js** - Web framework to handle routing and middleware.
- **HTML5/CSS3/JavaScript** - Frontend technologies for the user interface and WebRTC logic.

## How to Use

1. **Create a Room**:
   - Enter your **email** and a **unique room name**.
   - Click **Join Room** to create and enter the room.

2. **Share the Room**:
   - After joining the room, you can share the room link with the second person.
   - The second person needs to enter the **same room name** and their **email**.

3. **Start the Call**:
   - Once both users are in the room, the video call will be automatically initiated.

4. **End the Call**:
   - Either user can click the **End Call** button or close the browser window to end the call.


## WebRTC Flow (P2P Connection)

1. **User 1** enters the room, and a signaling message is sent to the server.
2. **User 2** enters the same room, and the signaling messages are exchanged via **Socket.IO**.
3. **ICE Candidates** are gathered by WebRTC and exchanged to establish the peer-to-peer connection.
4. Once the signaling and ICE candidates are exchanged, the **P2P connection** is established, and both users can see and hear each other.


## Setup and Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/webrtc-video-call.git
   cd webrtc-video-call
