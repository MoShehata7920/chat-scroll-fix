# Chat Auto-Scroll Challenge

## Chat Auto-Scroll Fix

This Flutter project focuses on fixing common chat auto-scroll UX problems, especially with **streaming AI responses**, to deliver a smooth “ChatGPT / WhatsApp-like” experience.

### UX Issues Identified
- Auto-scroll always triggered even when user scrolled up
- No distinction between user position (top vs bottom)
- Sending messages while scrolled up forced unwanted scroll
- Streaming responses caused jumpy scrolling

### Solutions Implemented
- Introduced `isUserAtBottom` flag
- `ScrollController` listener to track user position
- Conditional auto-scroll logic (`maybeScrollToBottom()`)
- Threshold-based bottom detection
- Smooth `animateTo` scrolling
- Streaming-safe scroll handling

### Scenarios Covered
- Basic auto-scroll
- Pause on manual scroll
- Send while scrolled up
- Resume on scroll down
- Streaming behavior

### Tech Details
- Flutter
- `ScrollController`
- `WidgetsBinding.instance.addPostFrameCallback`

### Deployed URL
- `https://moshehata7920.github.io/chat-scroll-fix/`

### Screen Recordings
- `record/2026-04-06 15-10-42.mp4`

## Setup

1. Get a free Gemini API key from [ai.google.dev](https://ai.google.dev)
2. Run `flutter pub get`
3. Run `flutter run` (web, macOS, or any platform)
4. Enter your API key and start chatting
