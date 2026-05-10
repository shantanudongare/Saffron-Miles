# Saffron Miles - Travel & Tourism Intelligence Platform

**A comprehensive AI-powered travel companion application built with React, Python Flask, and MongoDB.**

## 🎯 Features

- **AI-Powered Recommendations**: Smart destination and itinerary suggestions
- **Safety Analytics**: Real-time safety measures and alerts
- **Budget Optimization**: AI-driven budget planning for trips
- **Weather Integration**: Live weather updates and alerts
- **AI Storyteller**: Generate travel stories with AI
- **Chatbot Assistant**: Interactive travel guidance
- **Trip Planning**: Comprehensive itinerary management
- **Transport & Food**: Local recommendations

## 🛠️ Tech Stack

**Frontend:**
- React + TypeScript
- Vite (build tool)
- Tailwind CSS
- Lucide React (icons)

**Backend:**
- Python Flask
- MongoDB (Atlas)
- Groq AI API
- OpenWeather API
- ElevenLabs (Text-to-Speech)
- FastSMS & SMTP (notifications)

## 📋 Prerequisites

- Node.js 16+
- Python 3.8+
- MongoDB Atlas account
- API keys (see `.env.example`)

## 🚀 Quick Start

### 1. Clone and Setup

```bash
git clone https://github.com/shantanudongare/Saffron-Miles.git
cd Saffron-Miles
```

### 2. Backend Setup

```bash
cd backend
python -m venv venv

# Activate virtual environment
# Windows
venv\Scripts\activate
# macOS/Linux
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

### 3. Frontend Setup

```bash
npm install
```

### 4. Environment Configuration

```bash
# Copy example environment file
cp .env.example .env

# Edit .env with your actual credentials
# See 'Environment Variables' section below
```

### 5. Run Application

**Backend (Terminal 1):**
```bash
cd backend
python app.py
# Server runs on http://localhost:5000
```

**Frontend (Terminal 2):**
```bash
npm run dev
# App runs on http://localhost:5173
```

## 🔐 Environment Variables

Create a `.env` file in the project root using `.env.example` as template:

### Database
- `MONGO_URI`: MongoDB Atlas connection string

### AI/ML APIs
- `GROQ_API_KEY`: Main Groq API key
- `GROQ_API_KEY_BUDGET`: Budget Optimizer key
- `GROQ_API_KEY_ITINERARY`: Itinerary Planner key
- `NLP_CHATBOT`: Chatbot API key

### Text-to-Speech
- `ELEVENLABS_API_KEY`: ElevenLabs API key

### Notifications
- `SMTP_EMAIL`: Gmail address
- `SMTP_PASSWORD`: Gmail app password
- `FAST2SMS_API_KEY`: SMS API key

### Weather
- `OPENWEATHER_API_KEY`: OpenWeather API key
- `VITE_OPENWEATHER_API_KEY`: Frontend weather API key

### Firebase
- `FIREBASE_API_KEY`: Firebase credentials
- (See `.env.example` for all Firebase keys)

### App Config
- `DEBUG`: Development mode (False for production)
- `SECRET_KEY`: Flask session key
- `ENVIRONMENT`: development/production

## 📁 Project Structure

```
Saffron-Miles/
├── backend/               # Python Flask API
│   ├── routes/           # API endpoints
│   ├── services/         # Business logic
│   ├── models/           # ML models
│   ├── db/              # Database connections
│   ├── utils/           # Utilities
│   └── app.py           # Flask entry point
├── src/                  # React frontend
│   ├── components/       # React components
│   ├── pages/           # Page components
│   ├── services/        # API clients
│   ├── contexts/        # React contexts
│   ├── hooks/           # Custom hooks
│   └── App.tsx          # Root component
├── public/              # Static assets
├── docs/                # Documentation
├── tests/               # Test files
├── .env.example         # Environment template
├── .gitignore           # Git ignore rules
└── README.md            # This file
```

## 🔧 Configuration

### Flask Configuration
Edit `backend/config.py` to customize:
- Debug mode
- Database settings
- API timeouts
- Logging levels

### Vite Configuration
Edit `vite.config.ts` to customize:
- Port and proxy settings
- Build optimization
- Environment variables

## 🧪 Testing

```bash
# Backend tests
cd backend
python -m pytest

# Frontend tests
npm run test
```

## 📊 API Documentation

All API endpoints are prefixed with `/api/v1/`

### Main Endpoints
- `/attractions` - City attractions
- `/recommendations` - AI recommendations
- `/itinerary` - Trip planning
- `/budget` - Budget optimization
- `/safety` - Safety information
- `/weather` - Weather alerts
- `/chatbot` - AI chatbot
- `/stories` - AI storyteller

## 🐛 Troubleshooting

### "Module not found" errors
```bash
# Reinstall dependencies
pip install -r requirements.txt  # Python
npm install                      # Node
```

### Database connection errors
- Verify `MONGO_URI` in `.env`
- Check MongoDB Atlas IP whitelist
- Ensure network access is enabled

### API key errors
- Verify all required keys in `.env`
- Check key validity on respective platforms
- Ensure keys have appropriate permissions

### Video files not loading
Large media files are stored in `/local_assets_not_for_github/`
See `LARGE_FILES_GUIDE.md` for details.

## 🔐 Security

- ✅ All secrets in `.env` (never committed)
- ✅ API keys rotated regularly
- ✅ HTTPS enforced in production
- ✅ CORS properly configured
- ✅ Input validation on all endpoints
- ✅ SQL injection prevention
- ✅ Large files excluded from Git

## 📝 Large Files

**Note**: Media files over 50MB are not included in Git. 

To work with large files:
1. Download from `/local_assets_not_for_github/` locally
2. Or use Git LFS (Large File Storage)
3. See `LARGE_FILES_GUIDE.md` for details

## 🤝 Contributing

1. Create a feature branch
2. Commit with clear messages
3. Push and create a Pull Request
4. Ensure tests pass before merging

## 📄 License

Private repository - All rights reserved

## 👥 Contributors

- Shantanu Dongre - Lead Developer

## 📞 Support

For issues and questions:
- Open an issue on GitHub
- Contact: saffronmiless@gmail.com

## 🔄 Version

Current Version: 1.0.0

## 📚 Additional Resources

- [Backend Setup Guide](./docs/BACKEND_SETUP.md)
- [Frontend Setup Guide](./docs/FRONTEND_SETUP.md)
- [Environment Variables](./docs/ENVIRONMENT_SETUP.md)
- [Large Files Management](./docs/LARGE_FILES_GUIDE.md)
- [Deployment Guide](./docs/DEPLOYMENT.md)

---

**Last Updated**: May 2026
