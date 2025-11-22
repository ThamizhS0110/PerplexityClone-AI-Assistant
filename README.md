# 🤖 PerplexityClone AI Assistant

> A comprehensive AI assistant system with PC control, real-time search, multi-agent orchestration, and workflow automation capabilities.

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
[![Node.js](https://img.shields.io/badge/Node.js-18+-green.svg)](https://nodejs.org/)
[![React](https://img.shields.io/badge/React-18+-blue.svg)](https://reactjs.org/)

## 🌟 Features

### Core Capabilities
- 🔍 **Real-time Web Search** - Integrated search with source citations
- 💬 **AI Conversations** - Multi-turn conversations with context awareness
- 🖥️ **System Control** - OS-level command execution and automation
- 📁 **File Processing** - Handle PDF, CSV, images, and more
- 🤝 **Multi-Agent Orchestration** - Coordinate multiple AI agents
- 🔒 **Security Framework** - Built-in authentication and sandboxing
- ⚡ **Workflow Automation** - Automate repetitive tasks

### Frontend Features
- Modern chat interface with message history
- Real-time search suggestions
- Citation display system
- File upload capability
- Dark/Light theme toggle
- Code syntax highlighting
- Markdown rendering
- Responsive design

### Backend Features
- RESTful API endpoints
- WebSocket for real-time communication
- AI integration (OpenAI compatible)
- Search API integration
- Session management
- Rate limiting
- Error handling & logging

## 🏗️ Architecture

```
├── client/              # React frontend
│   ├── src/
│   │   ├── components/  # UI components
│   │   ├── pages/       # Page components
│   │   ├── services/    # API services
│   │   └── utils/       # Utility functions
│   └── public/
├── server/              # Express backend
│   ├── routes/          # API routes
│   ├── controllers/     # Request handlers
│   ├── middleware/      # Custom middleware
│   └── services/        # Business logic
├── ai-core/             # AI reasoning engine
│   ├── models/          # AI model integrations
│   ├── search/          # Search functionality
│   └── citations/       # Citation system
├── automation/          # Automation agents
│   ├── agents/          # Individual agents
│   ├── workflows/       # Workflow definitions
│   └── scheduler/       # Task scheduler
└── docs/                # Documentation
```

## 🚀 Quick Start

### Prerequisites
- Node.js 18 or higher
- npm or yarn
- OpenAI API key (or compatible AI service)
- Search API key (optional, for web search)

### Installation

```bash
# Clone the repository
git clone https://github.com/ThamizhS0110/PerplexityClone-AI-Assistant.git
cd PerplexityClone-AI-Assistant

# Install dependencies for client
cd client
npm install

# Install dependencies for server
cd ../server
npm install

# Set up environment variables
cp .env.example .env
# Edit .env with your API keys
```

### Environment Variables

Create a `.env` file in the server directory:

```env
# Server Configuration
PORT=5000
NODE_ENV=development

# AI Configuration
OPENAI_API_KEY=your_openai_api_key
AI_MODEL=gpt-4

# Search Configuration
SEARCH_API_KEY=your_search_api_key

# Security
JWT_SECRET=your_jwt_secret
SESSION_SECRET=your_session_secret

# CORS
CLIENT_URL=http://localhost:3000
```

### Running the Application

```bash
# Terminal 1 - Run the backend
cd server
npm run dev

# Terminal 2 - Run the frontend
cd client
npm start
```

Access the application at `http://localhost:3000`

## 📖 Usage

### Basic Chat
```javascript
// Send a message to the AI
POST /api/chat
{
  "message": "What is artificial intelligence?",
  "sessionId": "unique-session-id"
}
```

### Web Search
```javascript
// Perform a web search with AI analysis
POST /api/search
{
  "query": "latest developments in AI",
  "includeAnalysis": true
}
```

### File Analysis
```javascript
// Upload and analyze a file
POST /api/files/analyze
FormData: { file: <file-object> }
```

## 🔧 Development

### Tech Stack
- **Frontend**: React 18, Tailwind CSS, Axios, Socket.io-client
- **Backend**: Node.js, Express, Socket.io, JWT
- **AI**: OpenAI API, LangChain
- **Search**: SerpAPI or similar
- **Database**: MongoDB (optional)

### Project Structure
```
client/
  src/
    components/
      Chat/
        ChatInterface.jsx
        MessageList.jsx
        InputBox.jsx
      Search/
        SearchBar.jsx
        SearchResults.jsx
      FileUpload/
        FileUploader.jsx
    pages/
      Home.jsx
      Dashboard.jsx
    services/
      api.js
      socket.js
    App.jsx
    index.js

server/
  routes/
    chat.js
    search.js
    files.js
  controllers/
    chatController.js
    searchController.js
  middleware/
    auth.js
    rateLimit.js
  services/
    aiService.js
    searchService.js
  server.js
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

**Thamizh S**
- GitHub: [@ThamizhS0110](https://github.com/ThamizhS0110)
- Project: [PerplexityClone AI Assistant](https://github.com/ThamizhS0110/PerplexityClone-AI-Assistant)

## 🙏 Acknowledgments

- Inspired by Perplexity AI
- Built with modern web technologies
- Community-driven development

## 📞 Support

If you have any questions or need help, please open an issue on GitHub.

---

**Note**: This is an educational project demonstrating AI integration, web search, and automation capabilities. Always ensure proper security measures and API key protection in production environments.      
