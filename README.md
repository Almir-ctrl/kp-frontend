<div align="center">
<img width="1200" height="475" alt="Frontend" src="https://github.com/user-attachments/assets/0aa67016-6eaf-458a-adb2-6e31a0763ed6" />
</div>

# 🦁 Frontend

> **An advanced, AI-powered karaoke studio with vocal separation, real-time scoring, and comprehensive audio controls.**

[![React](https://img.shields.io/badge/React-19.2.0-61DAFB?logo=react)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.8.2-3178C6?logo=typescript)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-4.1.14-38B2AC?logo=tailwind-css)](https://tailwindcss.com/)
[![Vite](https://img.shields.io/badge/Vite-6.2.0-646CFF?logo=vite)](https://vitejs.dev/)
[![Python](https://img.shields.io/badge/Python-3.8+-3776AB?logo=python)](https://python.org/)

## ✨ Features

### 🎵 **Core Karaoke Experience**
- **Real-time Scoring**: Advanced pitch detection and vocal analysis
- **Timestamped Lyrics Display**: AI-generated synchronized lyrics with precise timing
- **Karaoke-style Highlighting**: Dynamic word-by-word lyric progression
- **Audio Visualizer**: Dynamic waveform visualization during performance
- **Performance History**: Track your singing progress over time

### 🤖 **AI-Powered Audio Processing**
- **Smart Vocal Separation**: Replace songs with instrumental versions for perfect karaoke
- **Advanced Stem Separation**: Isolate drums, bass, vocals, and other instruments into separate tracks
- **Timestamped Lyric Transcription**: Generate accurate lyrics with precise timing using OpenAI Whisper
- **Instant Processing**: Optimized AI pipeline with immediate results
- **Smart Library Management**: Automatic song replacement and organization

### 🎚️ **Professional Audio Controls**
- **Advanced Mixer**: 10-band EQ, gain control, and audio effects
- **Auto-Tune**: Real-time pitch correction with customizable settings
- **Device Selection**: Choose your preferred microphone and speakers
- **Live Streaming**: WebSocket-based audio streaming for remote listening
- **Smart Processing**: Instant AI results with optimized workflow

### 🎯 **Smart Coaching System**
- **AI Vocal Coach**: Personalized feedback powered by Google Gemini
- **Key Detection**: Automatic song key analysis for better guidance
- **Performance Analytics**: Detailed scoring breakdown and improvement tips
- **Practice Mode**: Loop specific sections for targeted practice

### 🎨 **Modern Interface**
- **Draggable Windows**: Resizable, movable UI panels for custom layouts
- **Lion-themed Design**: Golden gradient aesthetics with smooth animations
- **Dark Mode**: Eye-friendly dark interface for studio environments
- **Responsive Design**: Works on desktop and large tablets

## 🚀 Quick Start

### Prerequisites

**Frontend:**
- [Node.js 18+](https://nodejs.org/)
- npm or yarn package manager

**AI Backend (Optional but Recommended):**
- [Python 3.8+](https://python.org/)
- [ffmpeg](https://ffmpeg.org/) (for audio processing)
- NVIDIA GPU with CUDA (optional, for faster AI processing)

### 🎯 Frontend Setup

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd Lion-s-Roar-Studio
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   ```bash
   # Copy the example file
   cp .env.local.example .env.local
   
   # Edit .env.local and add your API key
   GEMINI_API_KEY=your_gemini_api_key_here
   ```

4. **Start the development server**
   ```bash
   npm run dev
   ```

5. **Open your browser**
   - Navigate to `http://localhost:3000`
   - Enjoy the karaoke experience!

### 🤖 AI Backend Setup (For Advanced Features)

1. **Navigate to the server directory**
   ```bash
   cd server
   ```

2. **Create a Python virtual environment**
   ```bash
   # Windows
   python -m venv venv
   .\venv\Scripts\activate
   
   # macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Install AI dependencies**
   ```bash
   pip install -r requirements.txt
   ```
   
   > **Note**: This will install PyTorch, Demucs, Whisper, and other AI models. The download may take several minutes and require ~2-4GB of disk space.

4. **Start the AI server**
   ```bash
   python main.py
   ```

5. **Verify the setup**
   - AI Server: `http://localhost:5000/health`
   - Should show all dependencies as available

## 📋 Available Scripts

### Frontend Commands
```bash
npm run dev          # Start development server
npm run build        # Build for production
npm run preview      # Preview production build
npm run build-css    # Build Tailwind CSS (watch mode)
```

### Backend Commands
```bash
# In the server directory
python main.py                    # Start AI server
python -m pytest                 # Run tests (if available)
pip install -r requirements.txt  # Install/update dependencies
```

## 🏗️ Project Structure

```
Lion-s-Roar-Studio/
├── 📁 components/               # React components
│   ├── 📁 ui/                  # Reusable UI components
│   ├── 📁 windows/             # Draggable window components
│   ├── ControlHub.tsx          # Main audio control center
│   ├── LibraryUI.tsx           # Song library management
│   ├── MainStudio.tsx          # Primary karaoke interface
│   ├── SongEditor.tsx          # Lyrics editing with timestamp display
│   ├── LoadingScreen.tsx       # Application loading interface
│   └── VideoSplashScreen.tsx   # Intro video component
├── 📁 context/                 # React context providers
│   └── AppContext.tsx          # Global app state management
├── 📁 server/                  # Python AI backend
│   ├── main.py                 # Flask server with AI models
│   ├── requirements.txt        # Python dependencies
│   └── README.md               # Backend documentation
├── 📁 utils/                   # Utility functions
│   └── music.ts                # Audio processing and timestamp utilities
├── 📁 types.ts                 # TypeScript type definitions (TimedLyric, Song, etc.)
├── 📁 public/                  # Static assets
│   ├── 📁 assets/              # Images and videos
│   ├── favicon.svg             # Custom lion favicon
│   └── favicon.ico             # Fallback favicon
├── 🎨 index.css               # Tailwind CSS with custom styles
├── ⚛️ App.tsx                 # Main React application
├── 🔧 tailwind.config.js      # Tailwind CSS configuration
└── 📦 package.json            # Project dependencies
```

## 🎵 How to Use

### Basic Karaoke
1. **Upload Songs**: Click "Upload File(s)" or drag & drop audio files
2. **Select a Song**: Choose from your library or use the demo songs
3. **Start Singing**: Click play and sing along with the lyrics
4. **View Your Score**: Real-time scoring appears as you sing

### Enhanced Lyrics Experience
1. **Transcribe with Timestamps**: Use Advanced Tools → "Transcribe Lyrics" to generate timestamped lyrics
2. **Song Editor**: View both plain lyrics and timed segments with precise timing display
3. **Karaoke Display**: Enjoy word-by-word highlighting synchronized with audio
4. **Auto-scrolling**: Lyrics automatically scroll to keep current line centered
5. **Multi-language Support**: Automatic language detection for international songs

### Smart Audio Processing
1. **Intelligent Vocal Removal**: Advanced AI creates clean instrumental versions
2. **Library Integration**: Seamlessly replaces songs with processed versions
3. **Instant Results**: Optimized processing pipeline for immediate feedback
4. **Quality Preservation**: Maintains original audio quality and metadata

### Advanced AI Features
1. **Smart Vocal Separation**: 
   - Select a song → Advanced Tools → "Create Instrumental"
   - Replaces original song with clean instrumental version
   - Perfect for karaoke with confirmation dialog for safety
2. **Advanced Stem Separation**:
   - Advanced Tools → "Separate All Stems" 
   - Creates 4 separate tracks: vocals, drums, bass, and other instruments
   - Adds new songs to library for individual track practice
3. **Timestamped Lyric Transcription**:
   - Advanced Tools → "Transcribe Lyrics"
   - AI generates accurate lyrics with precise timestamps
   - View results in Song Editor with timed segments
   - Enjoy synchronized karaoke-style display during playback
   - Supports multiple languages with automatic detection

### Audio Mixing
1. **Open Mixer**: Click the mixer icon in the control hub
2. **Adjust EQ**: Use the 10-band equalizer for perfect sound
3. **Apply Effects**: Add reverb, echo, or other audio effects
4. **Auto-Tune**: Enable pitch correction for enhanced vocals

## 🔧 Configuration

### Environment Variables
```bash
# .env.local
GEMINI_API_KEY=your_gemini_api_key_here  # For AI vocal coaching
AI_SERVER_URL=http://localhost:5000      # Local AI server
```

### Processing Behavior
- **Vocal Separation**: Replaces original song with instrumental version
- **Stem Separation**: Creates 4 new songs (vocals, drums, bass, other)
- **Transcription**: Adds timestamped lyrics to existing song
- **Confirmation Dialogs**: Vocal separation shows warning before replacing original

### Tailwind CSS Customization
The app uses custom Tailwind classes for theming:
```css
.lion-button   /* Golden gradient buttons */
.lion-input    /* Dark themed inputs */
.lion-card     /* Consistent card styling */
```

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for details.

### Development Workflow
1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Commit your changes: `git commit -m 'Add amazing feature'`
4. Push to the branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Demucs**: AI-powered source separation by Meta Research
- **OpenAI Whisper**: Robust speech recognition system
- **Google Gemini**: Advanced AI for vocal coaching features
- **React & Vite**: Modern web development framework
- **Tailwind CSS**: Utility-first CSS framework

## 🆘 Support

### Troubleshooting

**Frontend Issues:**
- Ensure Node.js 18+ is installed
- Clear browser cache and restart dev server
- Check browser console for error messages

**AI Backend Issues:**
- Verify Python 3.8+ and ffmpeg are installed
- Check server health at `http://localhost:5000/health`
- Review server console for dependency errors

**Performance Tips:**
- Use NVIDIA GPU with CUDA for faster AI processing
- Close unused applications during AI processing
- Ensure sufficient disk space (4GB+ recommended)
- Transcription with timestamps works best with clear audio
- Use high-quality audio files for better lyric accuracy
- Vocal separation works best with stereo recordings
- Confirm processing choices as vocal separation replaces original songs

### Getting Help
- 📧 **Email**: [support@lionsroar.studio](mailto:support@lionsroar.studio)
- 🐛 **Bug Reports**: [Create an Issue](https://github.com/your-repo/issues)
- 💬 **Discussions**: [GitHub Discussions](https://github.com/your-repo/discussions)

---

<div align="center">
<p><strong>🦁 Made with ❤️ for karaoke enthusiasts worldwide</strong></p>
<p><em>Unleash your inner lion and roar with confidence!</em></p>
</div>
