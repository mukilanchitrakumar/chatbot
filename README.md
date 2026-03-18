# Claude Chatbot 🤖

A ChatGPT-style chatbot UI built with plain HTML, CSS, and JavaScript — powered by the Anthropic Claude API.

![Claude Chatbot Preview](https://img.shields.io/badge/Claude-Sonnet%204-black?style=flat-square&logo=anthropic)
![HTML](https://img.shields.io/badge/HTML-Single%20File-orange?style=flat-square)
![No Framework](https://img.shields.io/badge/Framework-None-green?style=flat-square)

---

## Features

- 💬 Real-time streaming responses
- 🔑 API key input modal (no hardcoding needed)
- 🗂️ Chat history sidebar
- 📋 Copy message button
- ⏹️ Stop generation mid-stream
- ✨ Markdown rendering (bold, code blocks, lists, headers)
- 📱 Responsive layout

---

## Getting Started

### 1. Clone the repo

```bash
git clone https://github.com/your-username/claude-chatbot.git
cd claude-chatbot
```

### 2. Open the file

No install. No build step. Just open the file in your browser:

```bash
open claude-chatbot.html
```

Or double-click `claude-chatbot.html` in your file explorer.

### 3. Enter your API Key

When the app opens, a modal will ask for your **Anthropic API key**.

Paste your key (starts with `sk-ant-...`) and click **Start Chatting**.

> Get your API key at → [console.anthropic.com](https://console.anthropic.com)

---

## File Structure

```
claude-chatbot/
└── claude-chatbot.html   # Everything in one file
└── README.md
```

---

## How It Works

1. User types a message and hits Enter
2. The app calls `POST https://api.anthropic.com/v1/messages` with streaming enabled
3. Tokens stream back in real time and render as markdown
4. Full conversation history is sent each turn so Claude has context

---

## Requirements

- A modern browser (Chrome, Firefox, Edge, Safari)
- An [Anthropic API key](https://console.anthropic.com)
- No Node.js, no npm, no framework

---

## Security Note

Your API key is stored **only in browser memory** for the current session. It is never saved to `localStorage`, cookies, or any server. Closing the tab clears it.

> ⚠️ Do not commit your API key into the source code or share it publicly.

---

## Model

Uses `claude-sonnet-4-20250514` by default. You can change the model inside the `sendMessage()` function in the script:

```js
model: 'claude-sonnet-4-20250514',
```

Available models: `claude-opus-4-20250514`, `claude-sonnet-4-20250514`, `claude-haiku-4-5-20251001`

---

## License

MIT — free to use, modify, and distribute.
