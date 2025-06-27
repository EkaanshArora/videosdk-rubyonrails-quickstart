# Zoom Video SDK Ruby on Rails Quickstart

A simple Ruby on Rails application that demonstrates how to integrate Zoom Video SDK with JWT authentication.

## Features

- JWT token generation for Zoom Video SDK
- Simple form to enter session name and role
- Video session using UIToolkit

## Setup

1. **Install dependencies:**
   ```bash
   bundle install
   ```

2. **Set up environment variables:**
   Create a `.env` file in the root directory with your Zoom SDK credentials:
   ```
   ZOOM_SDK_KEY=your_zoom_sdk_key_here
   ZOOM_SDK_SECRET=your_zoom_sdk_secret_here
   ```

3. **Get Zoom SDK credentials:**
   - Go to [Zoom Marketplace](https://marketplace.zoom.us/)
   - Create a Video SDK app
   - Copy the SDK Key and SDK Secret

4. **Start the server:**
   ```bash
   rails server
   ```

5. **Access the application:**
   - Open http://localhost:3000
   - Enter a session name and select your role
   - Click "Join Session" to start the video call

## Routes

- `GET /` - Main form page
- `POST /zoom/generate_jwt` - Generate JWT token
- `GET /zoom/video_session` - Video session page

## Dependencies

- `jwt` - For JWT token generation
- `dotenv-rails` - For environment variable management

## Notes

- The JWT token is valid for 1 hour
- Make sure to keep your SDK credentials secure
- This is a basic implementation - add authentication and authorization as needed for production use
