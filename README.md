# Auto Poster Scheduling / APScheduling

A modern platform for scheduling and automating short-form video posts across multiple social media platforms.

![Status](https://img.shields.io/badge/status-in%20development-yellow)

## Overview

This project provides a robust solution for content creators to schedule and automate posting of short-form videos to platforms like YouTube Shorts, TikTok, and Instagram Reels. The system consists of two main components:

1. **React Native Application** - Cross-platform mobile and web interface for content selection, editing, and scheduling
2. **FastAPI Backend** - Powerful API server handling authentication, social media integrations, and scheduled posting

## Features

- 📱 **Cross-Platform Support** - Use on iOS, Android, and web browsers
- 🎬 **Content Management** - Upload, organize, and edit your short-form videos
- 📅 **Flexible Scheduling** - Plan your content calendar with an intuitive interface
- 🔄 **FIFO Queue Processing** - Reliable first-in, first-out posting mechanism
- 🔐 **Secure Authentication** - JWT-based user authentication and authorization
- 🔌 **Platform Integrations** - Currently supports YouTube, with TikTok and Instagram planned

## Project Structure

```
├── backend/                 # FastAPI server
│   ├── app/
│   │   ├── api/             # API endpoints
│   │   ├── services/        # Business logic
│   │   ├── models/          # Database models
│   │   └── utils/           # Helper functions
│   ├── tests/               # Backend tests
│   └── requirements.txt     # Python dependencies
│
└── frontend/                # React Native application
    ├── src/
    │   ├── api/             # API client
    │   ├── components/      # UI components
    │   ├── screens/         # Application screens
    │   ├── navigation/      # Navigation config
    │   └── store/           # State management
    ├── package.json         # JS dependencies
    └── app.json             # React Native config
```

## Getting Started

### Prerequisites

- Python 3.8+
- Node.js 14+
- React Native development environment
- Access to YouTube API (other platforms coming soon)

### Backend Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/social-media-scheduler.git
   cd social-media-scheduler/backend
   ```

2. Set up a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Create a `.env` file with your configuration:
   ```
   DATABASE_URL=sqlite:///./app.db
   SECRET_KEY=your_secret_key
   YOUTUBE_CLIENT_ID=your_client_id
   YOUTUBE_CLIENT_SECRET=your_client_secret
   ```

5. Run the server:
   ```bash
   uvicorn app.main:app --reload
   ```

### Frontend Setup

1. Navigate to the frontend directory:
   ```bash
   cd ../frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm start
   ```

## Development Roadmap

- [x] Project structure setup
- [x] Backend authentication system
- [x] YouTube API integration
- [ ] Video upload and processing
- [ ] Scheduling interface
- [ ] Queue processing system
- [ ] TikTok integration
- [ ] Instagram Reels integration
- [ ] Analytics dashboard

## Acknowledgments

- Inspired by the need for better tools for content creators
- Built with FastAPI and React Native