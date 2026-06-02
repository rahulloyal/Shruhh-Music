<div align="center">

# 🎵 Shruhh Music

<img src="app-icon.png" width="120" height="120" style="border-radius: 24px;" alt="Shruhh Music Logo" />

### *Free Unlimited Music. No Ads. Just Vibes.*

[![Platform](https://img.shields.io/badge/Platform-Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)](/)
[![PWA](https://img.shields.io/badge/PWA-Supported-5A0FC8?style=for-the-badge&logo=pwa&logoColor=white)](/)
[![Version](https://img.shields.io/badge/Version-1.0.5-FF2D55?style=for-the-badge)](/)
[![License](https://img.shields.io/badge/License-Proprietary-1a1a2e?style=for-the-badge)](/)
[![Powered By](https://img.shields.io/badge/Powered%20By-Shruhh.Inc-8b5cf6?style=for-the-badge)](/)

---

**Shruhh Music** is a sleek, modern music streaming application built for Indian music lovers. Stream trending Bollywood, Punjabi, Tamil, Telugu, and English tracks — completely free, with no audio ads, ever.

[📱 Download APK](#-download) · [✨ Features](#-features) · [📸 Screenshots](#-screenshots) · [🛠 Tech Stack](#-tech-stack) · [👨‍💻 Developer](#-developer)

</div>

---

## 📸 Screenshots

<div align="center">

| Home & Trending | Discover New Music | Album View |
|:---:|:---:|:---:|
| <img src="screenshots/Artboard 1.jpg" width="250" /> | <img src="screenshots/Artboard 1-1.jpg" width="250" /> | <img src="screenshots/Artboard 1-2.jpg" width="250" /> |
| **Artist Profile** | **Curated Playlists** | |
| <img src="screenshots/Artboard 1-3.jpg" width="250" /> | <img src="screenshots/Artboard 1-4.jpg" width="250" /> | |

</div>

---

## ✨ Features

### 🎶 Core Music Experience
- **Free Unlimited Streaming** — Listen to millions of songs with zero audio ads
- **High Quality Audio** — Toggle between standard and high-quality streaming
- **Full-Length Tracks** — No 30-second previews, get the complete songs
- **Background Playback** — Music keeps playing when you switch apps

### 🔍 Smart Discovery
- **Trending Now** — Real-time trending albums, playlists, and songs updated daily
- **Find New** — Discover fresh releases filtered by language (Hindi, Punjabi, English, Tamil, Telugu & more)
- **EchoFind** — AI-powered song recognition to identify what's playing around you
- **Top Charts & Editorial Picks** — Handpicked playlists curated for every mood
- **Radio Stations** — Curated mood-based radio stations (Lofi, Romantic, Party, Chill, and more)

### 🤖 AI-Powered Intelligence
- **Gemini AI Integration** — AI-powered playlist generation based on your mood or prompt
- **Smart Recommendations** — Machine learning-based song suggestions that learn your taste
- **Auto-Play Engine** — Intelligent queue management that never lets the music stop
- **Mood-Based Recommendation Engine** — Analyzes energy, tempo, genre, and language to suggest the perfect next track

### 📚 Library & Organization
- **Custom Playlists** — Create, edit, and manage unlimited playlists
- **Favorites** — One-tap favorite any song for quick access
- **Listening History** — Full playback history with recently played tracks
- **Smart Auto-Playlists** — Automatically generated playlists based on your listening patterns (by genre, artist, or mood)
- **Offline Downloads** — Save songs for offline listening via IndexedDB storage
- **Drag & Drop Queue** — Reorder your up-next queue with intuitive drag-and-drop

### 🎨 Premium User Experience
- **Dark Theme UI** — Beautiful dark interface with vibrant accent colors
- **Animated Player** — Full-screen player with smooth transitions and gestures
- **Swipe Controls** — Swipe to expand/collapse the player
- **Sleep Timer** — Set a timer to automatically stop music
- **Shuffle & Repeat** — Shuffle mode, repeat all, and repeat one
- **Media Session API** — Native media controls in notification bar and lock screen
- **Push Notifications** — Stay updated with new releases and recommendations

### 📊 Personalization & Stats
- **User Profile** — Customizable profile with name, avatar, and bio
- **Listening Statistics** — Track your top songs, top artist, total plays, and genre breakdown
- **Recharts-Powered Insights** — Beautiful data visualizations of your listening habits

### 🔒 Privacy & Security
- **Content Security Policy** — Strict CSP headers to prevent XSS attacks
- **No Tracking** — Your music data stays on your device
- **Local-First Storage** — Playlists, history, and preferences stored locally

---

## 🛠 Tech Stack

<div align="center">

| Layer | Technology |
|:---|:---|
| **Framework** | React 19 with TypeScript |
| **Build Tool** | Vite 6 |
| **UI Library** | Lucide React Icons |
| **Animations** | Framer Motion |
| **Styling** | Tailwind CSS 3 |
| **Typography** | Google Fonts — Outfit |
| **Charts** | Recharts |
| **Drag & Drop** | @hello-pangea/dnd |
| **AI / ML** | Google Gemini API (`@google/genai`) |
| **Native Bridge** | Capacitor 8 (Android) |
| **Push Notifications** | @capacitor/push-notifications |
| **Analytics** | Firebase Analytics (via Capacitor) |
| **Media Controls** | Capacitor Media Session Plugin |
| **Offline Storage** | IndexedDB (custom service) |
| **Music API** | JioSaavn API (via saavn.dev) |
| **Deployment** | Cloudflare Pages (PWA) |
| **PWA Support** | vite-plugin-pwa |

</div>

---

## 🏗 Architecture

```
┌─────────────────────────────────────────────┐
│                 React 19 App                │
│  ┌──────────┐ ┌──────────┐ ┌─────────────┐ │
│  │   Home   │ │  Search  │ │   Library   │ │
│  │  Screen  │ │  Screen  │ │   Screen    │ │
│  └────┬─────┘ └────┬─────┘ └──────┬──────┘ │
│       │             │              │        │
│  ┌────▼─────────────▼──────────────▼──────┐ │
│  │           Component Layer              │ │
│  │  Player · SongCard · ArtistProfile     │ │
│  │  AlbumProfile · PlaylistModal · Queue  │ │
│  │  EchoFind · ProfileView · Library      │ │
│  └────────────────┬───────────────────────┘ │
│                   │                         │
│  ┌────────────────▼───────────────────────┐ │
│  │            Service Layer               │ │
│  │  Music API · Recommendation Engine     │ │
│  │  Auto-Play · Offline Storage           │ │
│  │  Smart Playlists · Gemini AI           │ │
│  │  User Behavior · Pre-fetch · Color     │ │
│  └────────────────┬───────────────────────┘ │
│                   │                         │
│  ┌────────────────▼───────────────────────┐ │
│  │          Capacitor Bridge              │ │
│  │  Push Notifications · Media Session    │ │
│  │  Firebase Analytics · App Lifecycle    │ │
│  └────────────────────────────────────────┘ │
└─────────────────────────────────────────────┘
```

---

## 📱 Supported Platforms

| Platform | Status | Notes |
|:---|:---:|:---|
| **Android** (APK) | ✅ Available | Native Android via Capacitor |
| **Web** (PWA) | ✅ Live | Installable Progressive Web App |
| **iOS** | 🔜 Coming Soon | Planned for future release |
| **Desktop** | 🔜 Coming Soon | Via Electron or Tauri |

---

## 📥 Download

<div align="center">

### 📲 Get Shruhh Music Now

[![Download APK](https://img.shields.io/badge/Download_APK-Shruhh_Music_v1.0.5-FF2D55?style=for-the-badge&logo=android&logoColor=white)](Shruhh%20Music.apk)

**Size:** ~18 MB · **Min Android:** 7.0+ · **Architecture:** Universal

> 💡 **How to install:** Download the APK → Open it → Allow "Install from unknown sources" if prompted → Done!

</div>

| Method | Link | Notes |
|:---|:---|:---|
| **📦 Direct APK** | [**Download Shruhh Music.apk**](Shruhh%20Music.apk) | Click to download directly from this repo |
| **🌐 Web App (PWA)** | [**shruhhmusic.pages.dev**](https://shruhhmusic.pages.dev/) | Use instantly in your browser, installable as PWA |

---

## 👨‍💻 Developer

<div align="center">

### **Rahul Loyal Dalmas**

*Full-Stack Developer & Creator*

[![Instagram](https://img.shields.io/badge/Instagram-%23E4405F.svg?style=for-the-badge&logo=Instagram&logoColor=white)](https://www.instagram.com/rahul_.loyal/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/rahul-loyal-dalmas-5baa4532b/)

</div>

---

## 🏢 Powered By

<div align="center">

### **Shruhh.Inc**

*Building the future of entertainment, one app at a time.*

Shruhh.Inc is a product studio focused on creating premium, user-first digital experiences. Our apps are built with cutting-edge technology, beautiful design, and a relentless focus on performance.

**Other products by Shruhh.Inc:**
- 🌊 **Wave** — Desktop Music Player
- 🤖 **Sarahh AI** — AI-powered Personal Assistant  
- 📝 **Sticky Notes** — Minimal Note-taking App
- 📱 **Shruhh.Inc** — Product Catalog & Portfolio

</div>

---

## ⚖️ License

This project is **proprietary software** owned by Shruhh.Inc.  
The source code is not open source. This repository serves as a public showcase of the application.

All rights reserved © 2024-2026 Shruhh.Inc

---

<div align="center">

**Made with ❤️ by [Rahul Loyal Dalmas](https://www.linkedin.com/in/rahul-loyal-dalmas-5baa4532b/) — Powered by [Shruhh.Inc](https://www.instagram.com/rahul_.loyal/)**

*If you enjoy Shruhh Music, give this repo a ⭐*

</div>
