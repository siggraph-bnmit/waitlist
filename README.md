# 🚀 Siggraph BNMIT Waitlist Website

A simple, elegant one-page waitlist for Siggraph BNMIT to collect early interest and notify students when registrations open.

🔗 **Live here**: [https://siggraph-bnmit-waitlist.vercel.app](https://siggraph-bnmit-waitlist.vercel.app)

---

## 💡 What It Does

- Collects **Name**, **Email**, **Phone** via a clean form
- Validates inputs (name: 2–50 letters, email format, phone: 10–15 digits)
- Prevents abuse with **rate limiting** (max 5 submissions per minute)
- Checks Firebase for duplicates (email or phone)
- On successful sign-up:
  - Displays **loading screen** with rotating motivational messages
  - Shows confetti 🎉 and a success popup
- Saves data to **Firebase Realtime DB**
- Works seamlessly with **Zapier** → Google Sheets for logging
- Fully static—deployed on **Vercel**

---

## 🛠 Tech Stack

- **HTML + Tailwind CSS** – frontend UI
- **JavaScript** – form logic & animations
- **Firebase** – Realtime DB & duplicate check
- **Zapier** – webhook → Google Sheets
- **Vercel** – fast static deployment

---

## 🚦 Core Features

- **Debounced input validation** – instant form feedback
- **Rate limiter** – prevents spam and abuse
- **Duplicate check** – no repeated entries in Firebase
- **Loading animation** – custom messages with progress bar
- **Confetti celebration** – visual user feedback

---

## 🚀 Setup Guide

### 1. Clone the repo
```bash
git clone https://github.com/siggraph-bnmit/waitlist.git
cd waitlist
```

### 2. Firebase config
In `main.js`, replace with your project details:
```js
const firebaseConfig = {
  apiKey: "...",
  authDomain: "...",
  databaseURL: "...",
  projectId: "...",
  ...
};
```

### 3. Firebase security rules (basic)
```json
{
  "rules": {
    "waitlist": {
      ".read": false,
      ".write": true
    }
  }
}
```

### 4. Deploy to Vercel
```bash
npm install -g vercel
vercel --prod
```

---

## 🎨 Customize It

- Change loader messages in `js/main.js` (`loadingMessages`)
- Swap out the logo/animation files in `loader/`
- Modify form placeholders and text
- Tweak Tailwind classes in HTML/CSS for fresh look

---

## 👥 Built by

Built with ❤️ by **Siggraph BNMIT Team** 

---

## 📄 License

**MIT** — free to use, remix, and adapt

---

## 📂 Project Structure

- `index.html` – main form UI & loader
- `css/` – Tailwind stylesheet
- `js/main.js` – form logic, validation, Firebase, animations
- `loader/` – logo & animation assets

---

## 🏁 Quick Start

1. Clone ✅  
2. Add Zapier webhook & Firebase config 🔧  
3. Deploy on Vercel 🚀  
4. Share your link and grow the waitlist!

---

## 🙋‍♂️ Need Help?

Want a Zap template to send update via mail, Firebase rules file, or Vercel help? Just ask! 😊
