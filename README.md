# Random Video Chat Platform

A modern, feature-rich video and text chat platform similar to Omegle but with significant improvements in UI, security, and functionality.

## Features

- **Video & Text Chat**: Seamless peer-to-peer communication using WebRTC
- **Interest-Based Matching**: Find people with similar interests for more engaging conversations
- **User Authentication**: Sign in with Google or continue as a guest
- **Mobile-Responsive Design**: Works well on all device types
- **Chat Features**: 
  - Switch between video and text chat modes on mobile
  - Text chat alongside video on desktop
  - Toggle video/audio controls
- **Security Features**:
  - Session management
  - Simple moderation capabilities

## Tech Stack

- **Frontend**: Next.js, React, TailwindCSS
- **Real-time Communication**: Socket.io, WebRTC
- **Authentication**: NextAuth.js
- **State Management**: React Hooks
- **Media**: WebRTC with simple-peer

## Getting Started

### Prerequisites

- Node.js (16.x or later)
- npm or yarn
- Google OAuth credentials (for Google sign-in)

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd my-omegle-app
```

2. Install dependencies:
```bash
npm install
# or
yarn install
```

3. Create a `.env.local` file in the root directory with the following variables:
```
# NextAuth Configuration
NEXTAUTH_URL=http://localhost:3000
NEXTAUTH_SECRET=your-secret-key-here

# Google OAuth credentials
GOOGLE_CLIENT_ID=your-google-client-id
GOOGLE_CLIENT_SECRET=your-google-client-secret

# Socket.io Configuration
NEXT_PUBLIC_SOCKET_URL=http://localhost:3001
SOCKET_PORT=3001
```

4. Start the development server:
```bash
npm run dev
# or
yarn dev
```

5. Open [http://localhost:3000](http://localhost:3000) in your browser to see the application.

## How It Works

1. **Authentication**: Users can sign in with Google or continue as a guest
2. **Matching**: Users set their preferences (interests, language, etc.) and click "Start Matching"
3. **Chat**: Once matched, users can communicate through video and text chat
4. **Features During Chat**:
   - Toggle video on/off
   - Toggle audio on/off
   - Send and receive text messages
   - End chat and find a new partner

## Deployment

### For Production

1. Build the application:
```bash
npm run build
# or
yarn build
```

2. Start the production server:
```bash
npm start
# or
yarn start
```

### Scaling Considerations

- For production, consider using a more robust TURN server solution
- For high traffic, implement Redis for Socket.io state management
- Set up proper monitoring and logging

## Future Improvements

- Add language translation features
- Implement AI content moderation for text and video
- Add premium features (filters, themes, etc.)
- Implement group chat functionality
- Add end-to-end encryption

## License

This project is licensed under the MIT License - see the LICENSE file for details.
