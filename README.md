<h1 align="center">
  💧 NeerSetu — Smart Water Tracker
</h1>

<p align="center">
  <b>Your intelligent daily hydration companion powered by AI</b><br/>
  Track, analyze, and improve your water intake with smart reminders, adaptive goals, and gamified challenges.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/React-18.2-61DAFB?logo=react&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/badge/TypeScript-5.8-3178C6?logo=typescript&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/badge/Vite-6.2-646CFF?logo=vite&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/badge/Supabase-Cloud-3ECF8E?logo=supabase&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/badge/Gemini_AI-Powered-4285F4?logo=google&logoColor=white&style=for-the-badge" />
  <img src="https://img.shields.io/badge/PWA-Ready-5A0FC8?logo=pwa&logoColor=white&style=for-the-badge" />
</p>

---

## 📖 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Environment Variables](#environment-variables)
  - [Supabase Setup](#supabase-setup)
  - [Running the App](#running-the-app)
- [Project Structure](#-project-structure)
- [Screenshots](#-screenshots)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🌊 Overview

**NeerSetu** (meaning *Water Bridge* in Hindi) is a full-featured, AI-enhanced Progressive Web App (PWA) that helps users build and maintain healthy hydration habits. It combines smart tracking, personalized coaching, gamification, and cloud sync into one beautifully designed mobile-first experience.

Whether you're a fitness enthusiast, someone managing a health condition, or simply trying to drink more water daily — NeerSetu adapts to your lifestyle and keeps you motivated.

---

## ✨ Features

### 💧 Core Hydration Tracking
- **Log drinks instantly** — Water, Coffee, Tea, Juice, Soda with custom amounts
- **Quick-add buttons** for common portion sizes (150ml, 250ml, 350ml, 500ml)
- **Add custom notes** to any drink entry
- **Delete individual records** at any time
- **Calendar strip** — Browse and review past days with ease
- **ml / oz unit toggle** — Supports both metric and imperial systems

### 🎯 Adaptive Goal Engine
- **AI-driven daily goal** automatically adjusts based on:
  - Body weight (35 ml/kg formula)
  - Activity level (Low / Medium / High)
  - Climate (Cool / Temperate / Hot)
  - Recent 7-day hydration compliance
- **Goal Calculator Modal** — Manual goal estimation wizard
- Goal range clamped between **1,500 ml – 4,500 ml**

### 📊 Statistics & Analytics
- **7-day history** with bar charts (powered by Recharts)
- **Weekly completion rates** and trend visualization
- **Drink quality score** — Weighted by drink type (Water = 100%, Coffee = 45%, Soda = 20%)
- **Health pattern detection**:
  - Weekend hydration drops
  - Low morning intake patterns
  - Consistency streaks
- **Health risk alerts** (None / Low / Medium / High) based on intake pace and time since last drink
- **Personalized tips** generated from your real usage patterns

### 🤖 AI-Powered Insights (Google Gemini)
- **Real-time hydration advice** — Encouraging, science-backed tips based on current intake vs. goal
- **Weekly AI report** — Highlights your best day, detects patterns, and gives one actionable tip for next week
- Weather-aware and context-aware coaching messages

### 🔔 Smart Reminders
- **Interval-based reminders** — Fixed intervals (e.g., every 2 hours)
- **Specific time reminders** — Set exact times like 9:00 AM, 12:00 PM, 6:00 PM
- **Smart reminder mode** — Dynamically adjusts intervals based on your actual drink history
- **Push notifications** via browser Notifications API
- **Wake-up & bedtime window** — Reminders only fire during your active hours
- **Morning hydration nudge** — Reminds you if you haven't logged anything after waking up

### 🏆 Gamification & Achievements
- **XP & Level system** — Earn XP for every drink logged, goals hit, and achievements unlocked
- **Level-up celebrations** with sound effects
- **5 achievements to unlock**:
  | Badge | Description |
  |-------|-------------|
  | 🥤 First Sip | Log your first drink |
  | 🎯 Goal Smasher | Reach your daily goal |
  | 🔥 On Fire | Maintain a 3-day streak |
  | 🔥 Hydration Hero | Maintain a 7-day streak |
  | 🌅 Early Bird | Drink water before 8 AM |
- **Weekly missions / challenges**:
  - Goal Hunter — Hit your daily goal 3 times this week
  - Morning Sprint — Log before 9 AM for 5 days
  - Hydration Cadence — Log 4+ drinks/day for 4 days
- **Streak tracker** with grace-save (one missed day per week forgiven)
- **Milestone celebrations** at 7, 30, and 90-day streaks

### 🏅 Leaderboard (Social Mode)
- Compete against simulated community members
- Your position updates dynamically based on your XP
- Toggle social mode on/off from settings

### 📅 Weekly Coaching Plan
- AI-generated personalized weekly goals based on your history
- Focus areas: Wellness / Performance / Consistency
- Tracks completion rate and adjusts difficulty automatically

### 👤 Authentication & Profiles
- **Email/Password sign-up & login** via Supabase Auth
- **Guest Mode** — Full offline experience, no account required
- **Seamless guest-to-cloud migration** — Offline data automatically syncs when you sign in
- **Edit profile** — Update display name and avatar
- **DiceBear avatars** auto-generated per user

### ☁️ Cloud Sync (Supabase)
- All water records and settings synced to the cloud in real-time
- Works fully **offline** with localStorage fallback
- Automatic conflict-free data migration on first login

### 🌙 UI/UX & Accessibility
- **Dark mode / Light mode** toggle with persistence
- **Animated wave gauge** — Beautiful visual water fill progress indicator
- **Onboarding flow** — First-time setup collects activity level, climate, wake/bed times, and goals
- **Notification toast system** — Non-intrusive in-app alerts
- **Sound effects** — Click, water pour, success chimes (via Web Audio API)
- **Mobile-first, PWA-ready** — Installable on Android & iOS
- **Splash screen** on app load

### ⚙️ Settings & Personalization
- Daily goal (manual + adaptive)
- Wake-up time and bedtime
- Activity level and climate preferences
- Reminder type and interval
- Specific reminder times (add/remove individually)
- Smart reminders toggle
- Adaptive goal toggle
- Social mode toggle
- Unit system (ml / oz)
- Language preference (English / Hindi)
- Wearable sync toggle (extensible)
- Dark mode
- Account management (edit profile / logout)

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **Frontend Framework** | React 18 + TypeScript |
| **Build Tool** | Vite 6 |
| **Styling** | Inline / utility CSS with dark/light theming |
| **Charts** | Recharts 2.12 |
| **Icons** | Lucide React |
| **AI / LLM** | Google Gemini API (`@google/genai`) |
| **Backend / Auth** | Supabase (PostgreSQL + Auth) |
| **PWA** | Custom Service Worker (`sw.js`) + Web App Manifest |
| **Audio** | Web Audio API (sound service) |
| **State Management** | React Hooks + localStorage + Supabase cloud |

---

## 🚀 Getting Started

### Prerequisites

Make sure you have the following installed:

- **Node.js** `v18+` — [Download](https://nodejs.org/)
- **npm** `v9+` (comes with Node.js)
- A **Supabase** account — [supabase.com](https://supabase.com)
- A **Google Gemini API key** — [Get one here](https://aistudio.google.com/app/apikey)

---

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/Srush6007/NeerSetu.git

# 2. Navigate into the project directory
cd NeerSetu

# 3. Install dependencies
npm install
```

---

### Environment Variables

Create a `.env` file in the root of the project:

```env
# Google Gemini AI API Key
VITE_API_KEY=your_gemini_api_key_here
```

> **Note:** The Gemini API key is accessed via `process.env.API_KEY` in the services. Vite exposes variables prefixed with `VITE_` — ensure your `vite.config.ts` maps this correctly if needed.

---

### Supabase Setup

1. Go to [supabase.com](https://supabase.com) and create a new project.
2. In the **SQL Editor**, run the following to create the required tables:

```sql
-- Water intake records table
CREATE TABLE water_records (
  id TEXT PRIMARY KEY,
  user_id UUID REFERENCES auth.users(id) ON DELETE CASCADE,
  amount INTEGER NOT NULL,
  type TEXT NOT NULL,
  note TEXT,
  timestamp TIMESTAMPTZ NOT NULL,
  created_at TIMESTAMPTZ DEFAULT NOW()
);

-- User settings table
CREATE TABLE user_settings (
  user_id UUID PRIMARY KEY REFERENCES auth.users(id) ON DELETE CASCADE,
  settings JSONB NOT NULL,
  updated_at TIMESTAMPTZ DEFAULT NOW()
);

-- Enable Row Level Security
ALTER TABLE water_records ENABLE ROW LEVEL SECURITY;
ALTER TABLE user_settings ENABLE ROW LEVEL SECURITY;

-- Policies: users can only access their own data
CREATE POLICY "Users can manage their own records"
  ON water_records FOR ALL
  USING (auth.uid() = user_id);

CREATE POLICY "Users can manage their own settings"
  ON user_settings FOR ALL
  USING (auth.uid() = user_id);
```

3. Copy your **Project URL** and **anon/public API key** from `Settings → API` in your Supabase dashboard.
4. Update `services/supabaseClient.ts` with your credentials:

```ts
const supabaseUrl = 'https://your-project-id.supabase.co';
const supabaseKey = 'your-anon-key';
```

---

### Running the App

```bash
# Start the development server
npm run dev
```

Open your browser and navigate to `http://localhost:5173`

```bash
# Build for production
npm run build

# Preview the production build
npm run preview
```

---

## 📁 Project Structure

```
NeerSetu/
├── components/
│   ├── AchievementsScreen.tsx   # Achievements gallery
│   ├── AddDrinkModal.tsx        # Log a new drink
│   ├── Auth.tsx                 # Login / Sign-up screen
│   ├── CalendarStrip.tsx        # Horizontal date picker
│   ├── Dashboard.tsx            # Main home screen
│   ├── EditProfileModal.tsx     # Update name & avatar
│   ├── GoalCalculatorModal.tsx  # Hydration goal wizard
│   ├── NotificationToast.tsx    # In-app toast alerts
│   ├── Onboarding.tsx           # First-time setup flow
│   ├── Reminders.tsx            # Drink history & reminder log
│   ├── Settings.tsx             # App settings panel
│   ├── SplashScreen.tsx         # Loading splash
│   ├── Statistics.tsx           # Analytics & charts
│   └── WaveGauge.tsx            # Animated water fill gauge
│
├── services/
│   ├── dbService.ts             # Supabase CRUD operations
│   ├── geminiService.ts         # Google Gemini AI integration
│   ├── hydrationPlanner.ts      # Adaptive goal & coaching engine
│   ├── notificationService.ts   # Push notification handler
│   ├── soundService.ts          # Web Audio API sound effects
│   ├── supabaseClient.ts        # Supabase client initialization
│   └── utilityService.ts        # Shared utility helpers
│
├── App.tsx                      # Root component & app state
├── index.tsx                    # React entry point
├── types.ts                     # TypeScript type definitions
├── index.html                   # HTML shell
├── manifest.json                # PWA manifest
├── sw.js                        # Service Worker (PWA caching)
├── vite.config.ts               # Vite configuration
├── tsconfig.json                # TypeScript configuration
└── package.json                 # Dependencies & scripts
```

---

## 📸 Screenshots

> _Coming soon — run the app locally to see the full experience!_

---

## 🤝 Contributing

Contributions are welcome! Here's how to get started:

1. Fork the repository
2. Create your feature branch:
   ```bash
   git checkout -b feature/amazing-feature
   ```
3. Commit your changes:
   ```bash
   git commit -m "feat: add amazing feature"
   ```
4. Push to the branch:
   ```bash
   git push origin feature/amazing-feature
   ```
5. Open a Pull Request

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

---

<p align="center">
  Made with ❤️ by Srushti
</p>
