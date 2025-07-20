# simpleaiwebinterface
A Simple Self Hosted AI Web Interface that Interacts with your hosted LLM like Ollama. 

<img width="757" height="731" alt="image" src="https://github.com/user-attachments/assets/21b6f573-6800-44f2-821a-19478af1bcf0" />

<img width="1848" height="916" alt="image" src="https://github.com/user-attachments/assets/6fd6811a-0008-494a-a3cc-8f4cae9fce08" />

**Installer.py**
The single file that you need to run and will create folder and download files for offline use at the "Users" Folder. 

**Ollama Chat Interface**
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

**Prerequisites:**
-Install Ollama Desktop (from official website) and pull a model via CMD (e.g., cmd> ollama pull phi3:mini).
-Ensure Ollama is running: cmd > ollama serve.
-Python 3.x to host the index.html

**Setup:**

1. Download the index.html and save to your preferred location
2. Open CMD/Terminal and locate the index.html
3. Type: python -m http.server 8080
4. Launch the Web App:

Access at **http://localhost:8080**.

**Usage**

Login or Create Account:

On first load, create an account or log in with a username and password.
Each user has a unique profile with isolated conversations and prompts.

**Chat Interface:**

Select an Ollama model from the dropdown.
Upload documents (.txt, .pdf, .docx, .xlsx) for context.
Type messages and press Enter to send (Shift+Enter for new lines).
Use “New Chat” to save and start a new session.
Toggle dark/light mode via the sun/moon icon.


**Conversation Management:**

Save, load, or delete conversations from the sidebar.
Clear Chat to clear current Chat Box. This will refresh the Conversation and Bot
Export conversations to a .json file or import from a previous export (excludes documents).

**System Prompts:**

Create and save custom system prompts for consistent AI behavior.
Load or delete saved prompts from the sidebar.

**Notes**

Security: Uses localStorage for client-side storage with SHA-256 password hashing. Not suitable for production without a secure backend.
Dependencies: Loads external libraries (React, Tailwind CSS, CryptoJS, etc.) via CDNs.
Limitations: Export/import functionality excludes uploaded documents.

**Debugging**

Check Ollama: Ensure ollama serve is running and models are available (curl http://localhost:11434/api/tags).
Console Errors: Open browser DevTools (F12 → Console) for logs.
Storage: Verify localStorage (F12 → Application → Storage) for user-specific data (savedConversations_<username>).

**Contributing**
Contributions are welcome! Please open an issue or submit a pull request with improvements or bug fixes.
License
MIT License
