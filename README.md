# Study Buddy AI

> 🎓 An open-source AI personal tutor that runs locally on your computer

## About

Study Buddy is a desktop application that provides personalized AI tutoring without requiring internet access, accounts, or risking API abuse. It's a fork of the excellent Llama Tutor project, enhanced with:

- 🔌 **Provider-agnostic architecture** - Use Ollama (local), OpenAI, Together AI, or others
- 🖥️ **Desktop application** - Runs securely on your computer via Electron
- 🔒 **Privacy-first** - Default local mode means your data never leaves your device
- 💰 **Free to use** - No API costs with local Ollama mode
- 🎯 **Student-focused** - Simple interface designed for learners

## Features

- 📚 Generate comprehensive tutorials on any topic
- 🔍 Smart search integration for enriched content
- 💬 Interactive chat for follow-up questions
- 🎨 Clean, intuitive interface
- 📱 Works offline after initial setup
- ⚡ Fast local inference with Ollama

## Installation

### Prerequisites

- Node.js 18+ installed
-  [Ollama](https://ollama.com/) for local AI 

### Quick Start

1. **Download the latest release**
   - Windows: `StudyBuddy-Setup-x.x.x.exe`
   - macOS: `StudyBuddy-x.x.x.dmg`

2. **Install and run** - that's it! Study Buddy will use Ollama if installed, or prompt for API configuration.

### Development Setup

```bash
# Clone the repository from zip file
cd study-buddy #path for file

# Install dependencies
npm install

# Run in development mode
npm run electron-dev

# Build for production
npm run electron-pack


#After running the project , open settings page and change ollama settings of your system ollama configuration after downloading it then save and apply the changes.
```

## Configuration

### AI Providers

Study Buddy supports multiple AI providers. Configure in Settings or via environment variables:

#### Local (Recommended for Students)
```env
AI_PROVIDER=ollama
# No API key needed! Just install Ollama
```

#### OpenAI
```env
AI_PROVIDER=openai
OPENAI_API_KEY=your_api_key_here
```

#### Together AI
```env
AI_PROVIDER=together
TOGETHER_API_KEY=your_api_key_here
```



## Technical Stack

- **Frontend**: Next.js 14, React, TypeScript, Tailwind CSS
- **Desktop**: Electron
- **AI Integration**: Configurable providers (Ollama, OpenAI, Together AI)
- **Search**: Tavily API for enriched content
- **Analytics**: Helicone (optional)
- **Database**: Supabase (optional, for web deployment)



