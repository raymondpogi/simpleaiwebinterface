# simpleaiwebinterface
A Simple Self Hosted AI Web Interface that Interacts with your hosted LLM like Ollama. 

<img width="927" height="630" alt="image" src="https://github.com/user-attachments/assets/45359d5b-0d48-45b5-8126-b72ca59f2d9e" /> 
<img width="1785" height="905" alt="image" src="https://github.com/user-attachments/assets/66822693-42cd-4301-a1f5-976e8b3642a8" />

Ollama Chat Interface
A modern, client-side web application for interacting with Ollama models, built with React, Tailwind CSS, and JavaScript. Features a sleek, ChatGPT-inspired UI with user authentication, unique user profiles, dark/light mode, and support for file uploads and conversation management.
Features

User Authentication: Create accounts or log in with username/password (stored in localStorage with SHA-256 hashed passwords).
Unique User Profiles: Each user has isolated conversations and system prompts stored in localStorage.
Dark/Light Mode: Toggle between themes with persistent settings.
File Uploads: Upload and process .txt, .pdf, .docx, and .xlsx files (up to 10MB) for contextual chat.
Conversation Management: Save, load, delete, export, and import conversations (note: export/import includes conversations only, excluding documents).
System Prompts: Create, save, and manage custom system prompts per user.
Markdown Support: Render AI responses with markdown formatting.
Modern UI: Responsive design with teal gradients, Inter font, message avatars, and smooth animations.
Error Handling: Retry failed messages, 5-second input disable after stopping requests, and detailed error messages.
Ollama Integration: Connects to a local Ollama server (http://localhost:11434) for model selection and chat.

Installation

Prerequisites:

Install Ollama and pull a model (e.g., ollama pull mistral).
Ensure Ollama is running: ollama serve.
Python 3.x for the installer script.


Setup:

Clone the repository:git clone https://github.com/yourusername/ollama-chat-interface.git
cd ollama-chat-interface


Run the installer script to set up the project directory (~/OllamaChat or C:\Users\<Username>\OllamaChat) and create a Desktop shortcut:python installer.py




Launch the App:

Windows: Double-click Ollama Chat Interface.lnk or run start_ollama_chat.bat.
Linux: Double-click OllamaChat.desktop or run bash start_ollama_chat.sh.
Access at http://localhost:8080.



Usage

Login or Create Account:

On first load, create an account or log in with a username and password.
Each user has a unique profile with isolated conversations and prompts.


Chat Interface:

Select an Ollama model from the dropdown.
Upload documents (.txt, .pdf, .docx, .xlsx) for context.
Type messages and press Enter to send (Shift+Enter for new lines).
Use “New Chat” to save and start a new session.
Toggle dark/light mode via the sun/moon icon.


Conversation Management:

Save, load, or delete conversations from the sidebar.
Export conversations to a .json file or import from a previous export (excludes documents).


System Prompts:

Create and save custom system prompts for consistent AI behavior.
Load or delete saved prompts from the sidebar.



Notes

Security: Uses localStorage for client-side storage with SHA-256 password hashing. Not suitable for production without a secure backend.
Dependencies: Loads external libraries (React, Tailwind CSS, CryptoJS, etc.) via CDNs.
Limitations: Export/import functionality excludes uploaded documents.

Debugging

Check Ollama: Ensure ollama serve is running and models are available (curl http://localhost:11434/api/tags).
Console Errors: Open browser DevTools (F12 → Console) for logs.
Storage: Verify localStorage (F12 → Application → Storage) for user-specific data (savedConversations_<username>).

Contributing
Contributions are welcome! Please open an issue or submit a pull request with improvements or bug fixes.
License
MIT License
