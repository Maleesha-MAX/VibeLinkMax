# 🎥 Video Conferencing App (ZEGOCLOUD + Next.js)

A modern **video conferencing web application** built with **ZEGOCLOUD UIKit SDK**, inspired by tools like **Google Meet** and **Zoom**.  
It supports **1-to-1 calls, group meetings, screen sharing, and real-time messaging**, with a clean and responsive UI.

---

## ✨ Features

- 🔹 **1-to-1 Video Call**
- 👥 **Group Video Meetings**
- 🖥️ **Screen Sharing**
- 💬 **Real-time Messaging (Chat)**
- 🔐 **Unique Meeting Rooms (UUID-based)**
- ⚡ **Fast & Optimized UI**
- 🎨 **Modern UI with Tailwind CSS**
- 🌐 **Client-side State Management with Zustand**

---

## 🛠 Tech Stack

- **Framework:** Next.js  
- **Styling:** Tailwind CSS  
- **Video SDK:** ZEGOCLOUD UIKit SDK  
- **State Management:** Zustand  
- **Utilities:** UUID  
- **Language:** TypeScript / JavaScript  

---


## 📦 Installation

Clone the repository:

```bash
git clone https://github.com/your-username/video-conferencing-app.git
cd video-conferencing-app
Install dependencies:

npm install
# or
yarn install
Run the development server:

npm run dev
Open your browser at:

http://localhost:3000
🔑 Environment Variables
Create a .env.local file in the root directory and add:

NEXT_PUBLIC_ZEGO_APP_ID=your_app_id
NEXT_PUBLIC_ZEGO_SERVER_SECRET=your_server_secret
You can get these credentials from the ZEGOCLOUD Dashboard.

🧠 App Flow
User enters Name and Room ID

User can:

Join an existing meeting

Create a new meeting

ZEGOCLOUD handles:

Video streams

Audio streams

Screen sharing

In-meeting chat

Zustand manages UI and meeting state

🧩 UI Template (Meeting Join Screen)
This is the basic UI template used for joining or creating a meeting:

export default function Home() {
  return (
    <div className="min-h-screen flex items-center justify-center bg-gradient-to-br from-gray-950 via-gray-900 to-gray-950 text-white">
      <div className="w-full max-w-md bg-gray-900/70 backdrop-blur-xl shadow-2xl rounded-2xl p-8 border border-gray-800">

        <h1 className="text-3xl font-bold text-center mb-2">
          Video Meeting
        </h1>
        <p className="text-gray-400 text-center mb-6">
          Connect instantly with your team
        </p>

        <div className="mb-4">
          <label className="text-sm text-gray-400">Your Name</label>
          <input
            type="text"
            placeholder="Enter your name"
            className="w-full mt-1 px-4 py-2 rounded-lg bg-gray-800 border border-gray-700 focus:outline-none focus:ring-2 focus:ring-blue-500"
          />
        </div>

        <div className="mb-6">
          <label className="text-sm text-gray-400">Room ID</label>
          <input
            type="text"
            placeholder="Enter room ID"
            className="w-full mt-1 px-4 py-2 rounded-lg bg-gray-800 border border-gray-700 focus:outline-none focus:ring-2 focus:ring-blue-500"
          />
        </div>

        <button className="w-full bg-blue-600 hover:bg-blue-700 transition rounded-lg py-2 font-medium">
          Join Meeting
        </button>

        <div className="flex items-center my-5">
          <div className="flex-1 h-px bg-gray-700"></div>
          <span className="px-3 text-gray-500 text-sm">OR</span>
          <div className="flex-1 h-px bg-gray-700"></div>
        </div>

        <button className="w-full bg-green-600 hover:bg-green-700 transition rounded-lg py-2 font-medium">
          Create New Meeting
        </button>
      </div>
    </div>
  );
}