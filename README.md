# Shorts Automation Setup Guide

## Comprehensive Setup Guide

Welcome to the Shorts Automation repository! This guide will help you set up the project and configure all necessary components.

### Prerequisites
1. Node.js (version x.x.x)
2. Git
3. An Instagram Account
4. A Google Account for YouTube API access

### Setting Up the Environment

#### 1. Clone the repository:
```bash
git clone https://github.com/BhaveshS04/shorts-automation.git
cd shorts-automation
```

#### 2. Install dependencies:
```bash
npm install
```

### .env Setup

Create a `.env` file in your root directory and add the following configuration:
```.env
INSTAGRAM_USERNAME=your_instagram_username
INSTAGRAM_PASSWORD=your_instagram_password
YOUTUBE_API_KEY=your_youtube_api_key
YOUTUBE_CHANNEL_ID=your_youtube_channel_id
SHORTS_FOLDER_PATH=path/to/your/shorts/folder

# Optional Settings
SCHEDULED_UPLOAD_TIME=HH:mm:ss (24-hour format)
ANALYTICS_TRACKING=true
```  
- Replace placeholders with your actual credentials.

### Instagram Authentication Guide
1. Use the Instagram API to authenticate your account.
2. Ensure that the account has a public profile to automate uploads.
3. Store your credentials in the `.env` file as shown above.

### YouTube API Setup
1. Go to the [Google Cloud Console](https://console.cloud.google.com/).
2. Create a new project.
3. Enable the YouTube Data API v3.
4. Create API Credentials (API Key).
5. Copy your API Key and update it in the `.env` file.
6. Retrieve your YouTube Channel ID from the YouTube settings and update it in the `.env` file.

### Usage Instructions

#### Adding Shorts
To add a short, simply place your video file in the designated folder specified in `.env` under `SHORTS_FOLDER_PATH`. Ensure that the video file is compatible with YouTube Shorts requirements.

#### Scheduling Uploads
You can schedule uploads by setting `SCHEDULED_UPLOAD_TIME` in your `.env`. The bot will automatically pick up the files in the folder and upload them at the defined time.

#### Tracking Analytics
To track analytics, set `ANALYTICS_TRACKING` to `true` in your `.env`. The bot will log video performance and insights into a specified analytics file.

### Examples
- **Adding a Short**: Place `myShort.mp4` in the folder defined by `SHORTS_FOLDER_PATH`.
- **Scheduling**: Set `SCHEDULED_UPLOAD_TIME=14:00:00` for uploads at 2 PM UTC.
- **Analytics Report**: Generated automatically when tracking is enabled.

## Conclusion
You’re now set up to automate your YouTube Shorts uploads! Happy Posting!