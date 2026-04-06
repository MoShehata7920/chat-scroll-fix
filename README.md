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
- `@record`

## Setup

1. Get a free Gemini API key from [ai.google.dev](https://ai.google.dev)
2. Run `flutter pub get`
3. Run `flutter run` (web, macOS, or any platform)
4. Enter your API key and start chatting

## Your Task

This app has scroll UX issues. Compare it against the reference implementation and fix them.

**Reference:** https://iman-admin.github.io/chat-scroll-demo/

Test these scenarios in the reference demo before you start coding. Start by sending a message that produces a long response to fill the screen (e.g. _"Write a detailed essay about the history of the internet"_). If the response is too short, send another one.

1. Send a message and let the response stream in.
2. While a response is streaming, scroll up manually.
3. While scrolled up, send a new message.
4. While a response is streaming, scroll back down to the bottom.

Your solution will be scored primarily on how closely it matches the reference. You are free to use any AI tools you'd like.

## How to Submit

1. Clone this repo into a **private** repository on your own GitHub account.
2. Implement your solution.
3. Deploy your solution to the web.
4. Update this README with:
   - The UX issues you identified and fixed.
   - Your deployed URL.
   - Include screen recordings for all five scenarios and the deployed URL below.
5. Add **IMan-admin** as a collaborator to your private repo.
6. Send us the link to your repo.


### Deployed URL

[Live Demo](https://your-deployed-url.com)

### Screen Recordings

- **Scenario 1 (Basic Auto-Scroll):** [Watch Recording](https://your-recording/scenario1)
- **Scenario 2 (Pause on Manual Scroll):** [Watch Recording](https://your-hrecording/scenario2)
- **Scenario 3 (Send While Scrolled Up):** [Watch Recording](https://your-recording/scenario3)
- **Scenario 4 (Resume Auto-Scroll After Scroll Down):** [Watch Recording](https://your-recording/scenario4)
 

## Evaluation Criteria

- Does each scenario work correctly in isolation?
- Do all four scenarios work together without regressions?
- Does the behavior match the reference demo?
- Is the code clean, testable, and well-separated?
