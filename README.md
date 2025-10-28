# ChainedBrain 🔗🧠

An AI-powered multiplayer quiz platform with Web3 theming where brains connect through the chain.

![ChainedBrain](https://img.shields.io/badge/ChainedBrain-AI%20Quiz%20Platform-blueviolet?style=for-the-badge)
![Next.js](https://img.shields.io/badge/Next.js-15-black?style=for-the-badge&logo=next.js)
![SpacetimeDB](https://img.shields.io/badge/SpacetimeDB-Real--time-blue?style=for-the-badge)
![Groq](https://img.shields.io/badge/Groq-AI%20Powered-orange?style=for-the-badge)

---

## 🌟 Features

### 🎮 Dual Quiz Creation Modes
- **🤖 AI Generation**: Auto-generate quiz questions using Groq's Llama 3.3 70B model
- **✍️ Manual Creation**: Craft custom questions from scratch with full control

### 🏆 Live Multiplayer Sessions
- Real-time Kahoot-style quiz gameplay
- Room code system for easy joining
- Live leaderboards with podium rankings
- Host controls for quiz flow management
- Instant feedback with answer explanations

### 🖼️ Public Quiz Gallery
- Browse community-created quizzes
- Advanced search and filtering
- Sort by popularity, trending, newest
- Play solo anytime at your own pace
- Daily featured challenges

### 📊 Rich Analytics & Tracking
- **Detailed Quiz Summary**: Question-by-question breakdown with performance stats
- **Quiz History**: Track all your attempts with dates and scores
- **Creator Analytics**: Insights into quiz performance and question difficulty
- **Personal Stats**: Accuracy percentages, total attempts, best times

### 🏅 Gamification
- **Achievement System**: 6 unlockable badges
  - 🎯 First Steps - Complete your first quiz
  - ⭐ Perfect Score - Get 100% accuracy
  - ⚡ Speed Demon - Complete quiz in under 60 seconds
  - 🏆 Quiz Creator - Create your first quiz
  - 👥 Social Butterfly - Take 10 different quizzes
  - 🔥 Streak Master - 5 perfect scores in a row

### 👤 Profile Customization
- Custom display names and avatars
- Personal bio section
- Profile statistics display

### 🔗 Social Features
- Share results to Twitter/X and Farcaster
- Copy results to clipboard
- Public leaderboards for each quiz

---

## 🛠️ Tech Stack

- **Frontend**: Next.js 15 + React 19
- **Styling**: Tailwind CSS + shadcn/ui
- **Real-time Database**: SpacetimeDB (multiplayer sync + persistent storage)
- **AI Generation**: Groq API (Llama 3.3 70B)
- **Language**: TypeScript
- **Deployment**: Vercel-ready

---

## 🚀 Getting Started

### Prerequisites

- Node.js 18+ installed
- Groq API key (free tier available at [console.groq.com](https://console.groq.com))

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/mrbrightsides/chainedbrain.git
cd chainedbrain
```

2. **Install dependencies**
```bash
npm install
```

3. **Set up environment variables**

Create a `.env.local` file in the root directory:
```env
NEXT_PUBLIC_GROQ_API_KEY=your_groq_api_key_here
```

4. **Run the development server**
```bash
npm run dev
```

5. **Open in browser**
```
http://localhost:3000
```

---

## 📦 Project Structure

```
chainedbrain/
├── src/
│   ├── app/
│   │   ├── page.tsx                 # Main application page
│   │   ├── layout.tsx               # Root layout
│   │   └── api/
│   │       └── proxy/               # API proxy endpoint
│   ├── components/
│   │   ├── ui/                      # shadcn/ui components
│   │   ├── CreateQuiz.tsx           # Quiz creation interface
│   │   ├── LiveSession.tsx          # Multiplayer session UI
│   │   ├── EnhancedGallery.tsx      # Quiz gallery with search/filters
│   │   ├── QuizHistory.tsx          # User quiz history
│   │   ├── Achievements.tsx         # Achievement tracking
│   │   ├── CreatorAnalytics.tsx     # Analytics dashboard
│   │   ├── ProfileEditor.tsx        # Profile customization
│   │   └── About.tsx                # About page
│   ├── lib/
│   │   └── groq/
│   │       └── groqService.ts       # Groq API integration
│   ├── spacetime/                   # SpacetimeDB client setup
│   └── spacetime_module_bindings/   # Auto-generated DB bindings
├── spacetime-server/
│   └── src/
│       └── lib.rs                   # SpacetimeDB schema & reducers
├── public/                          # Static assets
└── README.md                        # This file
```

---

## 🎮 How to Use

### Creating a Quiz

1. **Click "Create Quiz" tab**
2. **Choose your mode:**
   - **AI Mode**: Enter topic, difficulty, and question count → AI generates instantly
   - **Manual Mode**: Add questions one by one with custom options
3. **Review & Start**: Preview questions, then start a live session or save to gallery

### Hosting a Live Session

1. Create or select a quiz
2. Click "Start Live Session"
3. Share the 6-digit room code with players
4. Control quiz flow: start questions, show answers, view live rankings
5. See final leaderboard with podium

### Joining a Live Session

1. Click "Join Live" tab
2. Enter room code and your nickname
3. Wait in lobby for host to start
4. Answer questions in real-time
5. Compete for top rankings!

### Playing from Gallery

1. Browse quizzes in "Gallery" tab
2. Use search/filters to find topics
3. Click "Play Solo" to start
4. Complete at your own pace
5. Submit score to public leaderboard

---

## 🗄️ Database Schema (SpacetimeDB)

### Core Tables
- **quiz**: Quiz metadata, questions, settings
- **live_session**: Active multiplayer sessions
- **participant**: Session players and scores
- **quiz_attempt**: Historical quiz attempts
- **user_achievement**: Earned badges
- **user_stats**: Aggregate user statistics
- **user_profile**: Profile customization
- **question_analytics**: Question performance data
- **daily_challenge**: Featured daily quizzes

### Key Reducers
- `create_quiz`: Save new quiz
- `start_live_session`: Initialize multiplayer session
- `join_session`: Add player to session
- `submit_answer`: Record player answer
- `record_quiz_attempt`: Save quiz history
- `award_achievement`: Grant badges
- `update_user_stats`: Update statistics
- `set_daily_challenge`: Set featured quiz

---

## 🎨 Design Philosophy

ChainedBrain embraces **Web3 aesthetics** with:
- Purple/blue/teal gradient themes
- Chain link motifs throughout the UI
- Smooth animations and transitions
- Responsive design for mobile and desktop
- Clean, modern component architecture

---

## 🔐 Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `NEXT_PUBLIC_GROQ_API_KEY` | Groq API key for AI generation | Yes |

---

## 📝 Development Phases

### Phase 1 ✅
- Core quiz creation (AI + Manual)
- Live multiplayer sessions
- Public gallery with solo play
- Detailed quiz summaries
- Quiz history tracking
- Achievement system
- Social sharing

### Phase 2 ✅
- Advanced gallery (search, filters, sorting)
- Creator analytics dashboard
- Profile customization
- Daily challenges
- Enhanced social features

### Future Phases 🚧
- Team mode (2v2, 3v3)
- Question types (true/false, fill-in-blank)
- Image-based questions
- Leaderboard seasons
- Mobile app
- NFT badges (Web3 integration)

---

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests
- Improve documentation

---

## 📄 License

MIT License - feel free to use this project for your own purposes.

---

## 👨‍💻 Credits

Created by **[mrbrightsides](https://github.com/mrbrightsides)**

Website: **[rantai.elpeef.com](https://rantai.elpeef.com)**

---

## 🙏 Acknowledgments

- **Groq** for blazing-fast AI inference
- **SpacetimeDB** for real-time multiplayer capabilities
- **shadcn/ui** for beautiful UI components
- **Vercel** for seamless deployment
- The open-source community

---

<div align="center">

**Built with 🧠 and ⛓️**

[GitHub](https://github.com/mrbrightsides) • [Website](https://rantai.elpeef.com)

</div>
