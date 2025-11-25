# SPA Direct API — WhatsApp & Viber

![HTML5](https://img.shields.io/badge/HTML5-orange?logo=html5)
![WhatsApp API](https://img.shields.io/badge/WhatsApp%20API-green?logo=whatsapp)
![Viber API](https://img.shields.io/badge/Viber%20API-purple?logo=viber)
![License: MIT](https://img.shields.io/badge/License-MIT-blue)

Single Page Application (SPA) for sending messages directly to **WhatsApp Cloud API** and **Viber PA API**, without backend relay. Configuration is stored in `localStorage` and managed via a modal form.

## ✨ Features
- Direct communication with official APIs (WhatsApp Cloud API, Viber PA API)
- Inline Web Workers for message sending logic
- First message acts as validation (if fails, stops sending)
- Configuration stored in browser `localStorage`
- Modal dialog for entering API tokens and IDs
- README instructions embedded in the modal with official links

## 📂 Project Structure
```
spa-direct-api/
├── README.md
├── index.html
└── assets/
    └── screenshots/
```

## 🚀 Setup
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/spa-direct-api.git
   cd spa-direct-api
   ```
2. Open `index.html` in your browser.

## ⚙️ Configuration
On first load, a modal will appear asking for:
- **WhatsApp Token** (Permanent Access Token)
- **WhatsApp Phone Number ID**
- **Viber Token** (X-Viber-Auth-Token)

### How to get these keys?
- **WhatsApp Cloud API**:
  - [Meta Developers — WhatsApp Cloud API](https://developers.facebook.com/docs/whatsapp/cloud-api)
  - Create an app and link WhatsApp Business account
  - Get token and Phone Number ID from [Meta App Dashboard](https://developers.facebook.com/apps/)

- **Viber PA API**:
  - [Viber Admin Panel](https://partners.viber.com/)
  - Create Public Account or Bot
  - Get X-Viber-Auth-Token from bot settings

## 🖼 Screenshots
*(Add screenshots in `assets/screenshots` folder)*

## 🔐 Security Notes
- **Do NOT use this approach in production** with tokens stored in `localStorage`.
- Recommended: Use a secure backend relay to hide tokens and handle API calls.

## ✅ How It Works
- Enter phone number, select API (WhatsApp/Viber), and type messages (each on a new line).
- First message is sent as validation.
- If validation succeeds, remaining messages are sent sequentially.
- Log panel shows status updates.

## 📜 License
MIT
