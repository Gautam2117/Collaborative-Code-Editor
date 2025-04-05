# Collaborative Code Editor

## Introduction:
Collaborative Code Editor is an online real-time code editing platform designed to enhance pair programming by allowing multiple developers to simultaneously view and edit code files in a distributed environment. This platform eliminates the need for manual file sharing and provides a seamless editing experience, fostering productivity and code quality.

## Features:
- Real-time code editing: Multiple users can edit code simultaneously, and changes are instantly visible to others.
- Pair programming support: Facilitates collaborative coding sessions, enhancing problem-solving and code quality.
- Room-based document management: Each document is identified by a unique RoomID, enabling users to join the same room and collaborate on specific projects.
- Persistent storage: Code changes are saved in a MongoDB cloud instance, ensuring data persistency even after user logouts.

## Tech Stack:
- **SpringBoot (JAVA):** Backend server for document management, user authentication, and WebSocket communication.
- **WebSockets:** Enables real-time communication between clients and the server.
- **MongoDB:** NoSQL database for persistent storage of code documents.
- **ReactJS:** Frontend framework for building a responsive and interactive user interface.
- **CodeMirror:** ReactJS code editor component with features like line gutters, syntax highlighting, and autocompletion.

## System Design:
![system design2](https://github.com/Devang2304/CollaborativeCodeEditor/assets/69463638/48bc7798-4f79-4516-9978-40ac85d31a11)
1. **Client-Server Architecture:** Utilizes a versatile architecture for independent information transfer and easy data management on the server.
2. **SpringBoot Server:** Manages document creation, retrieval, and WebSocket initialization. Handles client-server interactions for document updates.
3. **WebSocket Integration:** Facilitates real-time communication between clients and the server, enabling synchronized code editing.
4. **MongoDB Document Store:** Stores code documents, ensuring data persistency across sessions.

## Backend Implementation:
- **Endpoints:** 
  - `app.get('/roomID')`: Checks and creates a new RoomID if not present in the database.
- **WebSocket Server:** Handles client-side socket events (`project_write`, `project_get`, `project_save`) and server-side events (`connect`, `disconnect`, `connected_to_Room`).

## Frontend Implementation:
- **User Interface:** 
  - Built with ReactJS to provide an intuitive and responsive experience for users.
- **CodeMirror Integration:** Utilizes CodeMirror for the code editor component, offering features such as line gutters, syntax highlighting, and autocompletion.

## 📸 Live Screenshot
![My_code_editor](https://github.com/user-attachments/assets/a4736d90-fe17-4567-877d-7c0b1393e4b1)

