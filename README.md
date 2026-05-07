# Songtify - Spotify Playlist Analyzer

An intelligent Spotify playlist analyzer that categorizes songs by vibe and mood, providing data-driven insights into your music taste with real-time visualization and smart playlist creation.

## Features

- **Spotify Integration**: Seamless authentication with Spotify API for playlist access
- **AI-Powered Categorization**: Automatic song categorization based on audio features (energy, valence, acousticness, tempo, and more)
- **Mood-Based Grouping**: Intelligently groups songs into vibes like Chill/Lofi, Hype, Sad/Dark, Happy/Feel Good, Party, Indie/Mellow, and Focus/Instrumental
- **Real-Time Visualization**: Interactive charts powered by Recharts to visualize mood distributions and music analytics
- **Playlist Intelligence**: Analyze existing playlists and create sorted playlists based on mood categories
- **Responsive Design**: Fully responsive UI that works seamlessly on mobile, tablet, and desktop devices
- **TypeScript**: Type-safe codebase for both frontend and backend for better development experience
- **Modern Tech Stack**: Built with React 19 and Express.js for optimal performance

## Tech Stack

### Frontend
- **Frontend Framework**: React 19.2.5
- **Build Tool**: Vite 8.0.10
- **Language**: TypeScript 6.0.2
- **Styling**: Tailwind CSS 4.2.4
- **Routing**: React Router DOM 7.15.0
- **Data Visualization**: Recharts 3.8.1
- **Linting**: ESLint 10.2.1

### Backend
- **Runtime**: Node.js
- **Framework**: Express.js 5.2.1
- **Language**: TypeScript 6.0.3
- **API Client**: Axios 1.16.0
- **CORS**: CORS 2.8.6
- **Environment**: dotenv 17.4.2
- **Development**: ts-node 10.9.2

### External Services
- **Music Data**: Spotify Web API
- **Authentication**: Spotify OAuth 2.0

## Installation

Clone the repository:
```bash
git clone <repository-url>
cd songtify-v1
```

### Frontend Setup

Navigate to the client directory:
```bash
cd client
npm install
```

### Backend Setup

Navigate to the server directory:
```bash
cd ../server
npm install
```

Create a `.env` file in the server directory with your Spotify API credentials:
```env
SPOTIFY_CLIENT_ID=your_client_id_here
SPOTIFY_CLIENT_SECRET=your_client_secret_here
SPOTIFY_REDIRECT_URI=http://localhost:5173/callback
```

## Development

### Run Frontend Development Server

From the `client` directory:
```bash
npm run dev
```

The app will be available at `http://localhost:5173` with hot module reload (HMR) enabled.

### Run Backend Development Server

From the `server` directory:
```bash
npm run dev
```

The backend API will be available at `http://localhost:3000`

## Build

### Build Frontend for Production

From the `client` directory:
```bash
npm run build
```

The optimized build output will be in the `dist/` directory.

### Build Backend for Production

From the `server` directory:
```bash
npm run build
```

The compiled JavaScript will be in the `dist/` directory.

## Preview

To preview the production build locally:

```bash
npm run preview
```

## Linting

### Frontend Linting

From the `client` directory:
```bash
npm run lint
```

### Backend Type Checking

From the `server` directory:
```bash
npm run build
```

## How It Works

### Playlist Analysis
1. Authenticate with your Spotify account using OAuth 2.0
2. Select a playlist to analyze
3. Songtify fetches detailed audio features for each track
4. Songs are categorized based on audio analysis metrics:
   - **Chill / Lofi**: Low energy, high acousticness, instrumental heavy
   - **Hype / Hype**: High energy, high danceability, fast tempo
   - **Sad / Dark**: Low valence, moderate to low energy
   - **Indie / Mellow**: Moderate acousticness, lower energy
   - **Happy / Feel Good**: High valence, moderate to high energy
   - **Party**: Very high energy, high danceability, upbeat tempo
   - **Focus / Instrumental**: High instrumentalness, lower energy

### Visualization
- View mood distribution across your playlist
- See detailed breakdowns of each vibe category
- Track patterns in your music taste

### Playlist Creation
- Create new sorted playlists grouped by mood
- Organize your music library by vibe for different occasions

## Project Structure

```
songtify-v1/
├── client/                    # React frontend application
│   ├── src/
│   │   ├── components/       # Reusable React components
│   │   │   ├── AppView.tsx
│   │   │   ├── CategoryGrid.tsx
│   │   │   ├── HeroSection.tsx
│   │   │   ├── InfoCards.tsx
│   │   │   ├── Navbar.tsx
│   │   │   ├── PlaylistInput.tsx
│   │   │   ├── PlaylistPicker.tsx
│   │   │   ├── SongCard.tsx
│   │   │   └── VibeChart.tsx
│   │   ├── pages/            # Page components
│   │   │   ├── Callback.tsx
│   │   │   └── Home.tsx
│   │   ├── hooks/            # Custom React hooks
│   │   │   └── useSpotify.ts
│   │   ├── types/            # TypeScript type definitions
│   │   │   └── spotify.ts
│   │   ├── utils/            # Utility functions
│   │   │   ├── auth.ts
│   │   │   └── categorize.ts
│   │   ├── App.tsx           # Root application component
│   │   ├── main.tsx          # Entry point
│   │   ├── index.css         # Global styles
│   │   └── assets/           # Static assets
│   ├── vite.config.ts
│   ├── tsconfig.json
│   ├── eslint.config.js
│   └── package.json
├── server/                    # Express.js backend
│   ├── src/
│   │   └── index.ts          # Server entry point
│   ├── tsconfig.json
│   └── package.json
└── README.md
```

## Spotify API Requirements

To use Songtify, you'll need to register your application with Spotify:

1. Go to [Spotify Developer Dashboard](https://developer.spotify.com/dashboard)
2. Create a new application
3. Accept the terms and create the app
4. You'll receive a Client ID and Client Secret
5. Add `http://localhost:5173/callback` as a Redirect URI in your app settings
6. Copy the credentials to your `.env` file

## Environment Variables

### Server (.env)
```env
SPOTIFY_CLIENT_ID=your_spotify_client_id
SPOTIFY_CLIENT_SECRET=your_spotify_client_secret
SPOTIFY_REDIRECT_URI=http://localhost:5173/callback
PORT=3000
```

## Contributing

Contributions are welcome! Feel free to submit issues and enhancement requests.

## License

ISC License

## Author

Kenneth Jhun Balino

Built with React, Vite, Express.js, and ❤️ for music lovers.
