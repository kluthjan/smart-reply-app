# SmartSupply 
> **Delivering inspiring customer service support**

![SmartSupply](logo.png)

**SmartSupply** is a next-generation, privacy-focused customer support dashboard designed to empower support teams with AI-driven email drafting capabilities. Uniquely, SmartSupply runs its AI models **entirely in the browser** (Client-Side), ensuring that sensitive customer data never leaves your device unless you strictly choose to use a cloud fallback.

## 🚀 Key Features

### 🔒 Uncompromising Privacy
- **Local AI Engine:** Leverages [WebLLM](https://webllm.mlc.ai/) to run powerful Large Language Models (like Llama-3) directly inside your Chrome/Edge browser.
- **Client-Side Encryption:** All user data, including API keys and custom policies, is encrypted with **AES-GCM** using the Web Crypto API before being saved to `localStorage`.
- **Guest Mode:** Need a quick session? Use Guest Mode to run the app in-memory only. No data is written to the disk.

### ⚡ Intelligent Workflow
- **One-Click Drafting:** Paste a customer email, set a simple instruction (e.g., "Refund approved"), and generate a polite, policy-compliant response in seconds.
- **Smart Policies:** Define dynamic "Company Profiles" with specific return policies, tone of voice guidelines, and legal disclaimers. The AI strictly adheres to these rules.
- **Multi-Language Support:** Fully localized interface and response generation for **English, German, French, Dutch, Italian, and Spanish**.

### 🖥️ Adaptive Workspace
- **Fixed-Viewport Dashboard:** A productivity-first layout that fits everything on one screen. No endless scolling—panels scroll internally.
- **Custom Layouts:** Switch between a structured **Grid Mode** and a flexible **Custom Mode** where you can drag, resize, and stack windows to fit your personal workflow.
- **Dark Slate Aesthetic:** A professional, high-contrast design optimized for long working hours.

## 🛠️ Technology Stack
- **Core:** HTML5, React 18, Tailwind CSS (via CDN for rapid deployment).
- **AI/ML:** WebLLM (WASM-based local inference).
- **Security:** Native Web Crypto API.
- **Architecture:** Zero-Backend (Serverless). The entire app is a static frontend.

## 📦 Getting Started

### Prerequisites
- A modern browser with WebGPU support (Chrome 113+, Edge).
- A local web server (required for ES Modules & CORS).

### Installation
1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/smart-supply.git
   cd smart-supply
   ```

2. **Run locally**
   Since the app uses ES Modules, you cannot open `index.html` directly from the file system. Use a simple HTTP server:
   
   ```bash
   # Using Python
   python -m http.server 8000
   
   # OR using Node.js
   npx http-server .
   ```

3. **Launch**
   Open `http://localhost:8000` in your browser.

## 🎮 Usage Guide

1. **Login / Register:** Create a local account. Your password encrypts your data vault.
2. **Dashboard:**
   - **Incoming:** Paste the customer's query here.
   - **Policy:** Select a shop profile (e.g., "Fashion Boutique") to load specific rules.
   - **Response:** Click "Generate" (Zap icon) to auto-draft a reply.
3. **Local AI Setup:** Click "Enable Offline AI" in the settings. The browser will download the model weights (~2GB) once and cache them.

## 🤝 Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## 📄 License
[MIT](https://choosealicense.com/licenses/mit/)
