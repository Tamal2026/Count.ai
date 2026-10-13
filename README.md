# Count AI

SpatialTag AI is a web tool built for warehouses and retail stores to instantly count and track physical boxes and inventory using photos. 

Instead of walking around with clipboards or manually typing data into Excel, a manager can just take a photo of a room or shelf, upload it, and get a clean, searchable digital list of all their assets in seconds.

## 💡 Why I Built This (The Problem)
Standard AI vision models are okay at reading images, but they miss things. If an item is hidden in a dark corner, buried under shadows, or stacked tightly, generic AI often miscounts it. In a multi-million dollar warehouse, missing even one box of parts can cause massive delays and financial loss.

To solve this, I designed this tool to do two things:
1. **Grid Analysis:** It splits the uploaded image into a virtual 3x3 grid (like Top-Left, Bottom-Right) and forces the AI to check every single square inch separately so nothing gets missed.
2. **Double-Check System:** The backend doesn't just trust the first answer. It uses a 3-step pipeline where a second AI agent double-checks the first agent's work. If their box counts don't match, it self-corrects the error before showing it to the user.

## 🛠️ The Tech Stack
- **Backend:** Python (Flask/FastAPI) to handle image processing and logic.
- **Frontend:** HTML, JavaScript, and Tailwind CSS for a fast, clean, dark-mode dashboard.
- **Database:** SQLite to securely store lists and history without high costs.
- **AI Core:** Integrated with Google Gemini & OpenAI Vision APIs.

## 🚀 Key Features
- **Deep Tracking:** Counts boxes and extracts their exact colors, conditions, and markings.
- **Error Protection:** Includes regex filters that clean up messy AI data so the app never crashes.
- **One-Click Export:** A button to instantly download your entire inventory list as a standard Excel/CSV file.
- **File Safety:** Automatic rules that block oversized files or bad uploads before they hit the server.

*Note: This project was architected and deployed using AI-assisted development tools (Replit Agent) to maximize build speed, focusing heavily on robust system design, prompts, and error handling.*
