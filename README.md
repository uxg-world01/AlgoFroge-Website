# AlgoForge

AlgoForge is a browser-based trading strategy generator that turns user inputs into AI-assisted algorithm ideas and script-ready output for multiple markets and programming languages.

The project includes a frontend UI for selecting strategy parameters and a Node.js backend that calls AI providers (DeepSeek and Gemini) to generate trading logic. The app is designed for quick experimentation with market conditions, candlestick setups, risk rules, and executable strategy scripts.

## Features

- AI-powered strategy generation
- Multi-market support for forex, crypto, stocks, commodities, and indices
- Multiple output languages: Python, MQL5, Java, C, and C++
- Candlestick pattern selection
- Support and resistance logic
- Risk management controls
- Stop-loss and take-profit configuration
- Copy and download generated code
- Responsive modern interface
- Automatic fallback between DeepSeek and Gemini APIs

## Tech stack

- HTML, CSS, and JavaScript frontend
- Express.js backend
- Node.js server runtime
- OpenAI-compatible DeepSeek integration
- Google Gemini integration
- dotenv environment configuration

## Project structure

```bash
HTML_FILES/
├── index.html
├── generateScript.mjs
├── script.js
├── gemini.js
├── .env
├── .env_example
├── Dockerfile
├── package.json
├── README.md
├── SECURITY.md
├── image(13).png
└── node_modules/
```

## Prerequisites

- Node.js 18+
- npm
- At least one AI API key from either DeepSeek or Gemini

## Installation

1. Clone the repository:

```bash
git clone <your-repo-url>
cd HTML_FILES
```

2. Install dependencies:

```bash
npm install
```

3. Create your environment file:

```bash
cp .env_example .env
```

4. Add your API keys in `.env`:

```env
# DeepSeek
DEEPSEEK_API_KEY_1=your_key_here
DEEPSEEK_API_KEY_2=
DEEPSEEK_API_KEY_3=

# Gemini
GEMINI_API_KEY_1=your_key_here
GEMINI_API_KEY_2=
GEMINI_API_KEY_3=

PORT=3000
```

## Running the app

Start the server:

```bash
npm start
```

The app will run on the configured port, defaulting to `3000` unless you override it in `.env`.

Then open:

```text
http://localhost:3000
```

## How it works

- The frontend collects strategy inputs such as market, language, risk profile, and pattern preferences.
- The browser sends a prompt to the backend API.
- The backend tries DeepSeek first.
- If DeepSeek fails, it falls back to Gemini.
- The returned response is displayed in the app and can be copied or downloaded.

## API endpoint

The backend exposes:

```http
POST /api/generate
```

Example request body:

```json
{
  "prompt": "Generate a Python breakout strategy for BTCUSD with risk management and entry rules."
}
```

Example response:

```json
{
  "provider": "DeepSeek",
  "response": "...generated trading strategy..."
}
```

## Notes

- The app is intended for strategy generation and educational use.
- AI-generated trading ideas should be reviewed carefully before live use.
- API keys are loaded from `.env` and should not be committed to source control.

## License

This project is licensed under the ISC license unless otherwise specified.

---

# 📄 Output

After generation, three tabs become available.

## 📄 Script

View the complete source code.

You can

- Copy
- Download

---

## 📖 Explanation

Understand how the strategy works.

Includes

- Entry Logic
- Exit Logic
- Risk Management
- Support & Resistance
- Pattern Detection

---

## 📊 Backtest Notes

View

- Estimated Win Rate
- Profit Factor
- Drawdown
- Expected Signals
- Deployment Checklist

---

# 🔗 Connect Broker (Optional)

Scroll to the **Broker** section.

Choose your broker.

Examples

- MetaTrader 5
- Binance
- Bybit
- OANDA
- Interactive Brokers
- Kraken
- Alpaca

Enter your API credentials.

Click

```
Connect
```

The broker will appear as **Connected**.

---

# 📥 Download the Generated Code

Click

```
⬇ Download
```

The script will automatically be saved with the correct extension.

Example

```
strategy.py
```

or

```
strategy.mq5
```

or

```
strategy.java
```

---

# 🎉 You're Done!

Your AI-generated trading strategy is now ready for:

- Backtesting
- Paper Trading
- Demo Account Testing
- Live Deployment (after proper testing)

# 🤝 Contributing

Pull requests are welcome.

For major changes, please open an issue first to discuss your ideas.

# 👨‍💻 Author

**Shibanshu Das**

---

# ⭐ Support

If you found this project useful, please consider giving it a ⭐ on GitHub.

---

<div align="center">

## ⚡ AlgoForge

### AI Trading Script Generator

Built with ❤️ for Algorithmic Traders

</div>#
