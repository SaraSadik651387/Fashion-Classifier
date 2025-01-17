# Fashion-Classifier
## Overview
The **Fashion Classifier** is a web-based application that uses AI to classify fashion items, such as dresses and T-shirts, in real-time. Built with **Teachable Machine** and integrated with **Firebase**, the project showcases a seamless interaction between machine learning and a real-time database. The application is designed to provide an interactive interface for users while maintaining robust data tracking and logging capabilities.

---

## Key Features

1. **Real-Time Classification:**
   - Utilizes a pre-trained model from Teachable Machine to classify fashion items from a live camera feed.

2. **Database Integration:**
   - Keeps track of total detections in a Firebase Realtime Database.
   - Logs classification details (item type and timestamp).

3. **Interactive Interface:**
   - Provides a user-friendly layout with live video feed, classification results, and a detection counter.

4. **Reset Functionality:**
   - Enables users to reset the detection counter and clear logs directly from the interface.
  
   ![Image](https://github.com/user-attachments/assets/7ac37df4-8696-4bf0-8878-b06e9aeaf271)

---

## How It Works

1. **Live Camera Feed:**
   - Accesses the user's webcam to capture real-time video.
   - Sends the video frames to a Teachable Machine model for classification.

2. **Classification Process:**
   - Predicts the item type based on the model's training (e.g., Dress, T-Shirt).
   - Updates the detection counter and stores the log in Firebase.

3. **Real-Time Updates:**
   - Counter and logs are synchronized with Firebase, ensuring real-time data visibility.

4. **User Actions:**
   - Users can reset the counter and logs via a button on the interface.

---

## Technologies Used

- **HTML/CSS/JavaScript**: Front-end development.
- **Teachable Machine**: AI-based image classification.
- **Firebase**: Realtime Database for storing counters and logs.
- **Live Server**: Local development and testing.

---

## Setup Instructions

### Prerequisites
1. Install **Visual Studio Code** or another code editor.
2. Add the **Live Server** extension to your editor.
3. Set up a Firebase project ([Firebase Console](https://firebase.google.com/)).

### Quick Start Guide

1. **Download or Clone the Project:**
   - Download the ZIP file or use the command:
     ```bash
     git clone https://github.com/SaraSadik651387/Fashion-Classifier.git
     ```

2. **Open the Project in Your Editor:**
   - Use Visual Studio Code or your preferred code editor to open the project folder.

3. **Set Up Firebase Configuration:**
   - Log in to [Firebase Console](https://firebase.google.com/).
   - Create a new project and enable **Realtime Database**.
   - Copy your Firebase configuration and update it in `classifier.html` as follows:
     ```javascript
     const firebaseConfig = {
         apiKey: "YOUR_API_KEY",
         authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
         databaseURL: "https://YOUR_PROJECT_ID.firebaseio.com",
         projectId: "YOUR_PROJECT_ID",
         storageBucket: "YOUR_PROJECT_ID.appspot.com",
         messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
         appId: "YOUR_APP_ID"
     };
     ```

4. **Launch the Application:**
   - Use the Live Server extension in Visual Studio Code:
     - Right-click on `index.html` and select **"Open with Live Server"**.
   - The application will open in your default browser.

5. **Start Classifying:**
   - Use the camera feed to classify items.
   - Watch the results and counters update in real-time.
   - Use the live camera feed to classify items.
   - Observe the real-time counter and logs.

---
## Future Improvements

  - Export Logs: Add functionality to export logs as CSV or PDF.
  - Enhanced UI: Improve the interface with better animations and responsive design.
  - Hosting: Deploy the project on Firebase Hosting or Netlify.
