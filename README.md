# Chatbot Project

A full-stack chatbot application with a FastAPI backend (Python) and a modern React frontend. The backend connects to OpenAI (via OpenRouter) to provide conversational AI responses, while the frontend offers a beautiful, responsive chat UI.

---

## Features

- **FastAPI backend**: Handles chat requests, connects to OpenAI API, and manages CORS for local development.
- **React frontend**: Clean, modern chat interface with markdown/code rendering, auto-scroll, and error handling.
- **Styling**: Uses Bootstrap and Bootstrap Icons for a polished look.
- **Markdown & Syntax Highlighting**: Supports markdown and code blocks in bot replies.

---

## Project Structure

```
chatbot/
├── backend/
│   ├── app.py              # FastAPI app (main backend logic)
│   ├── requirements.txt    # Python dependencies
│   ├── .gitignore          # Python/venv ignores
│   └── ...
├── frontend/
│   ├── src/
│   │   ├── App.js          # Main React app (chat UI)
│   │   ├── App.css         # Custom styles
│   │   └── index.js        # Entry point
│   ├── public/
│   │   └── index.html      # HTML template
│   ├── package.json        # Frontend dependencies/scripts
│   └── ...
└── README.md               # (This file)
```

---

## Getting Started

### 1. Backend (FastAPI)

#### Setup
1. Navigate to the backend folder:
   ```bash
   cd backend
   ```
2. (Recommended) Create a virtual environment:
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Set your OpenAI API key in a `.env` file:
   ```env
   OPENAI_KEY=your_openai_key_here
   ```
5. Run the backend server:
   ```bash
   uvicorn app:app --reload
   ```
   The backend will be available at `http://localhost:8000`.

### 2. Frontend (React)

#### Setup
1. Navigate to the frontend folder:
   ```bash
   cd frontend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the development server:
   ```bash
   npm start
   ```
   The frontend will be available at `http://localhost:3000`.

---

## How It Works
- The React frontend sends user messages to the FastAPI backend at `/chat`.
- The backend forwards the message to OpenAI (via OpenRouter) and returns the AI's reply.
- The frontend displays the conversation, supporting markdown and code formatting.

---

## Customization
- **Model**: The backend uses `openai/gpt-4o` by default. You can change the model in `backend/app.py`.
- **Styling**: Edit `frontend/src/App.css` or use Bootstrap classes for custom styles.
- **API Keys**: Never commit your `.env` file or API keys to version control.

---

## Dependencies

### Backend
- fastapi
- uvicorn
- openai
- python-dotenv

### Frontend
- react, react-dom, react-bootstrap, bootstrap, bootstrap-icons
- axios, react-markdown, react-syntax-highlighter, remark-gfm

---

## License

This project is for educational/demo purposes. See individual package licenses for details.

---

## Credits
- [OpenAI](https://openai.com/) for the language model API
- [FastAPI](https://fastapi.tiangolo.com/) for the backend framework
- [Create React App](https://create-react-app.dev/) for frontend bootstrapping
- [Bootstrap](https://getbootstrap.com/) for UI components

---

## Screenshots

_Add screenshots of your app here!_

---

## Troubleshooting
- If the frontend can't connect to the backend, check CORS settings in `backend/app.py` and make sure both servers are running.
- For API errors, verify your OpenAI key and network connection.

---

## Contributing
Pull requests and suggestions are welcome!
