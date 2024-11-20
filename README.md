# AstroChat - Real-time Messaging App

AstroChat is a multi-platform messaging application designed to replicate the functionality and user interface of popular messaging apps like WhatsApp. It integrates real-time messaging, group and private chat spaces, message reactions, and more. The app is built using **Android Studio** for the mobile app and **Python with Firebase** for the desktop version, offering seamless communication between the two.

## Features

### 1. **Mobile App (Android)**
   - **User Authentication**: The app uses Firebase Authentication for secure login and registration, allowing users to sign up and log in with their Google or email credentials.
   - **Real-time Messaging**: Leveraging Firebase Realtime Database, messages are instantly sent and received across users.
   - **Message Reactions**: Users can react to messages with emojis, creating a more interactive and engaging chat experience.
   - **Group and Private Chats**: Users can create and join chat groups or engage in private one-on-one conversations.
   - **Firebase Integration**: Firebase Cloud Firestore is used for data storage, Firebase Analytics tracks app usage, and Firebase Cloud Messaging handles notifications.
   - **Encryption**: All messages are encrypted using Firebase’s security rules and stored securely in the Firebase database. While Firebase itself does not encrypt messages by default, encryption can be handled before storing data on Firebase (e.g., AES encryption) to ensure user data remains secure.

### 2. **Desktop App (AstroChat Desktop)**
   - **Group Chat Integration**: AstroChat also supports a desktop group chat interface built using **Python** and Firebase. The desktop app is fully integrated with Firebase to allow real-time updates across platforms.
   - **Cross-Platform Messaging**: Messages sent from the Android app are immediately available on the desktop, and vice versa, ensuring a consistent user experience across devices.
   - **Firebase Integration**: Firebase is used for both message storage and synchronization across the mobile and desktop platforms.

### 3. **Encrypted Message Storage in Firebase**
   - **Encryption Process**: 
     - Before messages are stored in Firebase, they are encrypted using **AES (Advanced Encryption Standard)** or other encryption techniques to protect user data.
     - Firebase Security Rules are used to restrict access to messages, ensuring only authorized users can read or write messages.
   - **How Encryption Works**:
     - When a user sends a message, the message is encrypted on the client side (Android or Desktop).
     - The encrypted message is then sent to Firebase and stored in Firestore or Realtime Database.
     - When the recipient receives the message, the client application decrypts the message locally, ensuring that no one (including Firebase) can read the content of the messages during transmission.
   - **Firebase Security**: Firebase provides built-in security features, including data encryption during transmission (SSL/TLS) and the ability to define granular access rules via Firebase Security Rules.

## Demo Application View

[View Demo Application]([view_hyperlink](https://github.com/GunaShankar0213/AstroChat_Android/blob/main/Astrochat%20Android%20demo.mp4))

### GitHub Repository: AstroChat Desktop

For the desktop group chat implementation, visit the [AstroChat Desktop]([Astrochat_desktop](https://github.com/GunaShankar0213/AstroChat_Desktop)) repository for the Python code and Firebase integration details.

## Technologies Used
- **Android Studio** for mobile app development
- **Firebase** for authentication, real-time messaging, analytics, and cloud storage
- **Python** and **Firebase SDK** for the desktop chat application
- **AES Encryption** for message security

## How It Works
1. **Message Flow**: 
   - User sends a message through either the Android or Desktop app.
   - The message is encrypted locally and sent to Firebase.
   - Firebase stores the encrypted message in the database.
   - The recipient’s app fetches the message from Firebase, decrypts it, and displays it in the chat.

2. **Real-Time Sync**: 
   - The Firebase Realtime Database enables real-time synchronization of messages across all connected devices.
   - When a user sends a message, it immediately appears in the chat for both the sender and recipient(s).

---

This project demonstrates the integration of **Firebase** and **encryption techniques** in building a cross-platform, real-time messaging app that prioritizes both functionality and security.
