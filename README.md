# 🎭 Facial Expression Reader

An AI-powered real-time facial expression detection application that uses machine learning to identify and analyze human emotions through webcam feed.

![Status](https://img.shields.io/badge/status-active-success.svg)
![License](https://img.shields.io/badge/license-MIT-blue.svg)

## 📋 Table of Contents

- [About](#about)
- [Features](#features)
- [Demo](#demo)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [How It Works](#how-it-works)
- [Detected Emotions](#detected-emotions)
- [Usage](#usage)
- [Browser Compatibility](#browser-compatibility)
- [Troubleshooting](#troubleshooting)
- [Future Enhancements](#future-enhancements)
- [Contributing](#contributing)
- [License](#license)

## 🎯 About

The Facial Expression Reader is a web-based application that leverages deep learning models to detect and classify human facial expressions in real-time. It uses your device's camera to capture video feed and analyzes facial features to determine emotional states with confidence scores.

## ✨ Features

- **Real-Time Detection**: Instant emotion recognition with live video feed
- **7 Emotion Categories**: Detects Neutral, Happy, Sad, Angry, Fearful, Disgusted, and Surprised
- **Visual Feedback**: 
  - Face bounding box overlay
  - Live emotion confidence bars
  - Dominant emotion display with emoji indicators
- **Privacy-First**: All processing happens locally in your browser
- **No Installation Required**: Run directly in any modern web browser
- **Responsive Design**: Works on desktop and mobile devices
- **Modern UI**: Beautiful glassmorphism design with smooth animations

## 🎬 Demo

1. Open the HTML file in your browser
2. Click "Start Camera" to activate your webcam
3. Allow camera permissions when prompted
4. Watch as the AI detects and analyzes your facial expressions in real-time
5. See confidence scores for all emotions and the dominant emotion highlighted

## 🛠️ Tech Stack

### Core Technologies
- **HTML5**: Structure and video capture
- **CSS3**: Styling with gradients, glassmorphism, and animations
- **JavaScript (ES6+)**: Application logic and real-time processing

### AI/ML Libraries
- **face-api.js** (`@vladmandic/face-api`): Face detection and expression recognition
  - Built on top of TensorFlow.js
  - Pre-trained neural network models
- **TinyFaceDetector**: Lightweight face detection model
- **FaceExpressionNet**: Deep learning model for emotion classification

### CDN Resources
- face-api.js library: `https://cdn.jsdelivr.net/npm/@vladmandic/face-api/dist/face-api.min.js`
- Pre-trained models: `https://cdn.jsdelivr.net/npm/@vladmandic/face-api/model/`

## 🚀 Getting Started

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Webcam access
- Internet connection (for loading libraries and models)

### Installation

1. **Download the HTML file**
   ```bash
   # Clone or download the project
   git clone <repository-url>
   cd facial-expression-reader
   ```

2. **Open in browser**
   - Simply double-click the HTML file, or
   - Use a local server for better performance:
   ```bash
   # Using Python
   python -m http.server 8000
   
   # Using Node.js
   npx http-server
   ```

3. **Access the application**
   - Direct: Open `index.html` in your browser
   - Local server: Navigate to `http://localhost:8000`

### No Build Process Required
This is a standalone HTML application - no npm, webpack, or build tools needed!

## 🧠 How It Works

### 1. Model Loading
The application loads two pre-trained neural network models:
- **TinyFaceDetector**: Detects faces in the video frame
- **FaceExpressionNet**: Analyzes facial features to classify emotions

### 2. Video Capture
Uses the browser's `getUserMedia` API to access the webcam and stream video.

### 3. Real-Time Processing
- Captures frames from video stream
- Detects face locations using TinyFaceDetector
- Extracts facial landmarks and features
- Runs expression classification on detected faces
- Returns confidence scores for each emotion

### 4. Visualization
- Draws bounding boxes around detected faces
- Updates emotion bars with confidence percentages
- Highlights the dominant emotion with emoji and confidence score

## 😊 Detected Emotions

The application recognizes 7 fundamental human emotions:

| Emotion | Emoji | Description |
|---------|-------|-------------|
| Neutral | 😐 | Calm, expressionless face |
| Happy | 😊 | Smiling, joyful expression |
| Sad | 😢 | Downcast, unhappy expression |
| Angry | 😠 | Frowning, hostile expression |
| Fearful | 😨 | Anxious, scared expression |
| Disgusted | 🤢 | Repulsed, distasteful expression |
| Surprised | 😲 | Shocked, astonished expression |

## 📖 Usage

### Basic Usage

1. **Start the Application**
   - Open the HTML file in your browser
   - Wait for "AI models loaded!" message

2. **Activate Camera**
   - Click the "Start Camera" button
   - Grant camera permissions when prompted

3. **View Results**
   - Position your face in front of the camera
   - Observe real-time emotion detection
   - Check confidence scores for all emotions
   - See the dominant emotion highlighted

4. **Stop Detection**
   - Click the "Stop Camera" button when finished

### Tips for Best Results

- **Good Lighting**: Ensure your face is well-lit
- **Face the Camera**: Look directly at the camera
- **Stay in Frame**: Keep your entire face visible
- **Stable Position**: Minimize movement for better accuracy
- **Clear Background**: Avoid cluttered backgrounds
- **Single Face**: Works best with one face at a time

## 🌐 Browser Compatibility

### Fully Supported
- ✅ Google Chrome (v90+)
- ✅ Microsoft Edge (v90+)
- ✅ Firefox (v88+)
- ✅ Safari (v14+)
- ✅ Opera (v76+)

### Requirements
- WebRTC support
- WebGL support
- Camera access permissions
- JavaScript enabled

### Mobile Support
- ✅ iOS Safari (v14+)
- ✅ Chrome for Android
- ⚠️ Performance may vary on older devices

## 🔧 Troubleshooting

### Common Issues and Solutions

#### 1. "Error loading models"
**Problem**: Models failed to load from CDN

**Solutions**:
- Check your internet connection
- Refresh the page
- Clear browser cache
- Try a different browser
- Check if CDN is accessible in your region

#### 2. "Error accessing camera"
**Problem**: Cannot access webcam

**Solutions**:
- Grant camera permissions in browser settings
- Ensure no other application is using the camera
- Check if camera is properly connected
- Try using HTTPS (required by some browsers)
- Restart your browser

#### 3. "faceapi is not defined"
**Problem**: Library not loaded before initialization

**Solutions**:
- This should be fixed in the latest version
- Wait for the page to fully load before clicking buttons
- Check browser console for errors
- Ensure internet connection is stable

#### 4. Low FPS or Laggy Performance
**Problem**: Slow detection speed

**Solutions**:
- Close other browser tabs
- Use a more powerful device
- Reduce video resolution
- Ensure good lighting for faster detection
- Close resource-intensive applications

#### 5. Inaccurate Emotion Detection
**Problem**: Wrong emotions detected

**Solutions**:
- Improve lighting conditions
- Face the camera directly
- Make clearer facial expressions
- Remove glasses or face coverings if possible
- Stay within camera frame

## 🔐 Privacy & Security

- **Local Processing**: All computation happens in your browser
- **No Data Storage**: No images or data are saved
- **No Server Communication**: Video never leaves your device
- **Camera Control**: You have full control over camera access
- **Open Source**: Code is transparent and auditable

## 🎨 Customization

### Modify Emotions
Edit the `emotionEmojis` object to change emoji representations:
```javascript
const emotionEmojis = {
    neutral: '😐',
    happy: '😊',
    // Add or modify emotions
};
```

### Adjust Detection Sensitivity
Modify TinyFaceDetector options:
```javascript
new faceapi.TinyFaceDetectorOptions({
    inputSize: 416,  // Increase for better accuracy
    scoreThreshold: 0.5  // Adjust confidence threshold
})
```

### Change Theme Colors
Update CSS gradient values:
```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

## 🚀 Future Enhancements

- [ ] Multiple face detection and tracking
- [ ] Emotion history graph over time
- [ ] Screenshot and recording functionality
- [ ] Age and gender detection
- [ ] Facial landmarks visualization
- [ ] Export emotion data to CSV
- [ ] Dark/Light theme toggle
- [ ] Mobile app version
- [ ] Integration with video conferencing platforms
- [ ] Advanced analytics dashboard

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Development Guidelines
- Follow existing code style
- Test on multiple browsers
- Update documentation
- Add comments for complex logic
- Ensure privacy and security standards

## 📚 Resources

### Documentation
- [face-api.js Documentation](https://github.com/vladmandic/face-api)
- [TensorFlow.js Guide](https://www.tensorflow.org/js)
- [WebRTC API](https://developer.mozilla.org/en-US/docs/Web/API/WebRTC_API)

### Research Papers
- FaceNet: A Unified Embedding for Face Recognition
- Emotion Recognition in the Wild via Convolutional Neural Networks
- Real-time Face Detection and Emotion Recognition

## 📄 License

This project is licensed under the MIT License - see below for details:

```
MIT License

Copyright (c) 2025

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## 👨‍💻 Author

Created with ❤️ by [Your Name]

## 🙏 Acknowledgments

- **Vladimir Mandic** for the excellent face-api.js library
- **TensorFlow.js Team** for the ML framework
- **Open Source Community** for inspiration and support

## 📞 Support

If you encounter any issues or have questions:

- Open an issue on GitHub
- Check the troubleshooting section
- Review browser console for error messages
- Ensure you're using the latest version

---

**⭐ Star this repository if you find it helpful!**

**📢 Share with others who might benefit from this project!**

---

Made with 🎭 and AI
