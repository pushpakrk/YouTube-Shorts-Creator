# YouTube Shorts Creator

A full-stack web application built with Flask that automatically transforms regular videos into YouTube Shorts format.

## Features

- **Upload Any Video**: Support for MP4, MOV, AVI, and MKV formats
- **Automatic Splitting**: Divides long videos into 60-second segments suitable for YouTube Shorts
- **Vertical Format Conversion**: Transforms videos to 9:16 aspect ratio required for YouTube Shorts
- **Preview and Download**: View and download processed clips directly from your browser
- **YouTube Integration**: Upload processed clips directly to YouTube with OAuth2 authentication
- **Mobile-Friendly Interface**: Beautiful, responsive design works on all devices

## Installation

### Prerequisites

- Python 3.8 or higher
- FFmpeg (included in this repository)

### Setup

1. Clone this repository:
   ```
   git clone https://github.com/yourusername/yt_shorts_creator.git
   cd yt_shorts_creator
   ```

2. Create a virtual environment:
   ```
   python -m venv venv
   venv\Scripts\activate
   ```

3. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

4. YouTube API Setup (Optional, for YouTube upload feature):
   - Create a project in the [Google Developer Console](https://console.developers.google.com/)
   - Enable the YouTube Data API v3
   - Create OAuth 2.0 Client ID credentials
   - Download the client_secret.json file and place it in the `config` directory

## Usage

1. Start the application:
   ```
   python run.py
   ```

2. Open your browser and go to `http://127.0.0.1:5000`

3. Upload a video file

4. Wait for the processing to complete (larger videos will take longer)

5. Preview, download, or upload your YouTube Shorts

## Project Structure

```
project/
├── app/
│   ├── templates/         # HTML templates
│   ├── static/            # CSS, JS, and static assets
│   ├── video_processing/  # Video processing logic
│   ├── api/               # YouTube API integration
│   ├── __init__.py        # Flask app initialization
│   └── routes.py          # Application routes
├── config/                # Application configuration
├── tests/                 # Unit/integration tests
├── ffmpeg.exe             # FFmpeg executable
├── ffprobe.exe            # FFprobe executable
├── requirements.txt       # Python dependencies
├── run.py                 # Application entry point
└── README.md              # This file
```

## Security Considerations

- The application implements secure file upload validation
- YouTube API credentials are stored securely
- File size limits prevent server overload

## Copyright Disclaimer

This application adds a watermark to processed videos and includes a disclaimer to remind users of copyright responsibilities. Users must only upload content they own or have permission to modify.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
