# AI Design Benchmark

An AI-powered UI component generator that creates high-fidelity design variations in real-time using multiple AI models. Compare design outputs from different LLMs including Google Gemini and any OpenRouter-supported model.

![AI Design Benchmark](https://img.shields.io/badge/AI-Design%20Tool-blue) ![React](https://img.shields.io/badge/React-19.0-61dafb) ![TypeScript](https://img.shields.io/badge/TypeScript-5.8-3178c6)

## 🎨 Features

- **Multi-Model Support**: Switch between Google Gemini and any OpenRouter model
- **Real-time Streaming**: Watch designs generate live as the AI creates them
- **3 Design Variations**: Get three unique design directions for every prompt
- **Full Homepage Generation**: Expand any component into a complete 8-section homepage
- **Variation Explorer**: Generate radical conceptual alternatives for any design
- **Export Ready**: Copy HTML/CSS source code for production use
- **Model Benchmarking**: Compare design quality across different AI models

## 🚀 Quick Start

### Prerequisites

- Node.js 16+ installed
- API keys for:
  - Google Gemini API (get from [Google AI Studio](https://makersuite.google.com/app/apikey))
  - OpenRouter API (get from [OpenRouter](https://openrouter.ai/keys))

### Installation

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/AI-DESIGN-BENCHMARK.git
cd AI-DESIGN-BENCHMARK

# Install dependencies
npm install

# Set up environment variables
# Create .env.local file with:
GEMINI_API_KEY=your_gemini_api_key_here
OPENROUTER_API_KEY=your_openrouter_api_key_here
```

### Run Development Server

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

## 🎯 How to Use

### 1. Select Your Model

Choose between:
- **Gemini**: Google's Gemini 3 Flash model
- **OpenRouter**: Any model from [OpenRouter's catalog](https://openrouter.ai/models)
  - Paste model ID (e.g., `z-ai/glm-4.7`, `anthropic/claude-3.5-sonnet`, `openai/gpt-4`)

### 2. Generate Components

Enter a design prompt like:
- "A minimalist weather card"
- "Dark mode dashboard with charts"
- "Futuristic product card with holographic effects"

Press Enter or click "Surprise Me" for random prompts.

### 3. Explore Features

- **Variations**: Click to generate 3 radical design alternatives
- **Full Homepage**: Expand any component into an 8-section landing page
- **Source Code**: View and copy the HTML/CSS
- **Grid View**: Compare all variations side-by-side

## 🏗️ Architecture

```
flash-ui/
├── index.tsx              # Main React app
├── index.html             # HTML entry point
├── index.css              # Global styles
├── vite.config.ts         # Vite configuration
├── types.ts               # TypeScript interfaces
├── constants.ts           # Placeholder prompts
├── utils.ts               # Utility functions
└── components/
    ├── ArtifactCard.tsx           # Design preview cards
    ├── SideDrawer.tsx             # Code viewer drawer
    ├── DottedGlowBackground.tsx   # Animated background
    └── Icons.tsx                  # SVG icon components
```

## 🤖 Supported Models

### Google Gemini
- **gemini-3.1-flash-lite**: Fast, creative UI generation

### OpenRouter (Examples)
- `z-ai/glm-4.7` - GLM-4.7 with reasoning
- `anthropic/claude-3.5-sonnet` - Claude 3.5 Sonnet
- `openai/gpt-4` - GPT-4
- `meta-llama/llama-3-70b-instruct` - Llama 3 70B
- See full list at [openrouter.ai/models](https://openrouter.ai/models)

## 🎨 Design System

The app uses a dark-themed design system with:
- **Colors**: Deep blacks, subtle grays, accent highlights
- **Typography**: Inter (sans-serif), Roboto Mono (code)
- **Effects**: Glassmorphism, backdrop blur, subtle shadows
- **Animations**: Smooth transitions, loading indicators

## 🔧 Tech Stack

- **React 19** - UI framework
- **TypeScript 5.8** - Type safety
- **Vite 6** - Fast build tool
- **Google GenAI SDK** - Gemini API integration
- **OpenRouter API** - Multi-model access
- **CSS3** - Custom styling (no frameworks)

## 📝 Scripts

```bash
npm run dev       # Start development server
npm run build     # Build for production
npm run preview   # Preview production build
```

## 🌟 Key Features Explained

### Real-time Streaming
Uses Server-Sent Events (SSE) to stream AI responses in real-time, showing progressive HTML generation as it happens.

### IP-Safe Prompts
All design prompts use physical/material metaphors instead of artist names to avoid copyright issues:
- ❌ "Bauhaus style"
- ✅ "Rectilinear grid with primary pigments"

### Smart Caching
Saves model selection and generated placeholders to localStorage for faster subsequent sessions.

### Responsive Design
Fully responsive with mobile-optimized layouts (≤1024px breakpoint).

## 🚧 Development

### Adding New Models

Simply select "OpenRouter" and paste any model ID from [openrouter.ai/models](https://openrouter.ai/models). No code changes needed!

### Customizing Prompts

Edit `constants.ts` to modify placeholder prompts or `index.tsx` to adjust AI generation prompts.

## 📄 License

Apache 2.0

## 🙏 Credits

Original concept by ammaar@google.com

Enhanced with:
- Multi-model support
- Full homepage generation
- OpenRouter integration
- Model benchmarking capabilities

## 🐛 Issues & Contributions

Found a bug or want to contribute? Open an issue or PR!

---

**Built with ❤️ using AI-powered design generation**
