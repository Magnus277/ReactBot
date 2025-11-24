# Chatbot Project

A modern, interactive chatbot application built with React and Vite. This project demonstrates a clean component-based architecture with real-time chat interactions powered by the SuperSimpleDev Chatbot API.

## Features

- **Real-time Chat Interface**: Send and receive messages instantly
- **User-Friendly Design**: Clean, intuitive UI with user and robot message differentiation
- **Loading States**: Visual feedback while waiting for bot responses
- **Keyboard Shortcuts**: 
  - Press `Enter` to send messages
  - Press `Escape` to clear the input field
- **Profile Images**: Display user and robot avatars for better visual distinction
- **Welcome Message**: Friendly greeting message on first load

## Tech Stack

- **Frontend Framework**: React 19.1.0
- **Build Tool**: Vite 6.3.5
- **Package Manager**: npm
- **Chatbot API**: SuperSimpleDev (v8.6.4)
- **Development Tools**: ESLint 9.25.0

## Project Structure

```
chatbot-project/
├── src/
│   ├── components/
│   │   ├── ChatInput.jsx       # Message input component
│   │   ├── ChatInput.css       # Input styling
│   │   ├── ChatMessage.jsx     # Individual message display
│   │   ├── ChatMessage.css     # Message styling
│   │   ├── ChatMessages.jsx    # Message list container
│   │   └── ChatMessages.css    # Messages container styling
│   ├── assets/                 # Images (robot.png, user.png)
│   ├── App.jsx                 # Main application component
│   ├── App.css                 # App styling
│   ├── main.jsx                # React entry point
│   └── index.css               # Global styles
├── public/                     # Static assets
├── package.json                # Project dependencies
├── vite.config.js              # Vite configuration
├── eslint.config.js            # ESLint rules
├── index.html                  # HTML template
└── README.md                   # This file
```

## Getting Started

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd chatbot-project
```

2. Install dependencies:
```bash
npm install
```

### Running the Application

#### Development Mode
Start the development server with hot module replacement (HMR):
```bash
npm run dev
```

The application will typically run at `http://localhost:5173`

#### Build for Production
Create an optimized production build:
```bash
npm run build
```

#### Preview Production Build
Preview the production build locally:
```bash
npm run preview
```

### Code Quality

Run ESLint to check code quality:
```bash
npm run lint
```

## Component Overview

### App Component
The main component that manages chat message state and renders the chat interface.

### ChatInput Component
- Handles user text input
- Manages loading state during API calls
- Sends messages to the chatbot via SuperSimpleDev API
- Supports keyboard shortcuts (Enter to send, Escape to clear)

### ChatMessage Component
- Displays individual messages with styling based on sender (user/robot)
- Shows profile images for visual differentiation
- Responsive message layout

### ChatMessages Component
- Renders the list of all chat messages
- Displays the welcome message when no messages exist

## Usage

1. Open the application in your browser
2. Type a message in the input field
3. Press Enter or click the Send button
4. Wait for the chatbot to respond
5. Continue the conversation

## State Management

The app uses React's built-in `useState` hook for state management:
- `chatMessages`: Array of message objects with structure: `{ message, sender, id }`
- `inputText`: Current user input text
- `isLoading`: Loading state while waiting for bot response

## Future Enhancements

- Message history persistence (localStorage/database)
- User authentication
- Chat history export
- Theme customization
- Message reactions/emojis
- Typing indicators
- Message timestamps

## License

This project is open source and available for educational purposes.

## Author

Created as a learning project for full-stack React development.
