# Stella Chatbot
Stellar Chatbot is a lightweight, responsive web application that provides an interactive conversational experience using the gemma3:1b language model via the Ollama API. It features a clean, modern interface with dark/light mode support and real-time response streaming.

## Features
- Real-time chat with message history (10 messages).
- Light/dark mode toggle with persistence.
- Markdown support, code highlighting, and copy buttons.
- Integrates with local Ollama server.
- Includes "Diagram" and "Specs" pages.

## Prerequisites
- Modern browser.
- Ollama with `gemma3:1b`:
  ```bash
  ollama pull gemma3:1b
  ollama run gemma3:1b
  Local server (e.g., python -m http.server 8000).

## Installation
1. Clone: git clone https://github.com/your-username/stellar-chatbot.git
2. Serve: cd stellar-chatbot && python -m http.server 8000
3. Ensure Ollama runs on http://localhost:11434
4. Visit: http://localhost:8000/index.html

## Usage
- Start your Ollama server if not already running: ollama serve
- Open the chat interface in your browser.
- Type and send messages via "Send" or Enter.
- Navigate to "Diagram" or "Specs" in the navbar.
- Toggle mode with the switch.

## System Architecture
The Stellar Chatbot consists of three main components:
1. Frontend Web Interface - HTML/CSS/JavaScript application
2. Ollama Server - Local API endpoint for model interaction
3. gemma3:1b Model - The language model generating responses
User Input → Ollama → gemma3:1b → Ollama → Response

## Configuration
You can modify the model parameters in the 'JavaScript code':


    model: 'gemma3:1b',
    prompt: fullPrompt,
    stream: true,
    options: { 
        temperature: 0.7,  // Controls randomness (0-1)
        top_k: 40,         // Limits next token selection
        top_p: 0.9,        // Nucleus sampling threshold
        num_ctx: 2048      // Context window size
    




## Structure
stellar-chatbot/
├── index.html  # HTML, CSS, JS
├── README.md   # This file


## Technical Details
- Frontend: HTML5, CSS3, JavaScript.
- API: Ollama at http://localhost:11434/api/generate.
- Model: gemma3:1b (Temp: 0.7, Top-k: 40, Top-p: 0.9, Context: 2048 tokens).
- Limits: Local Ollama required, basic error handling.

## Limitations
- Context limited to ~2048 tokens
- Requires local Ollama server running
- Performance depends on local hardware
- Basic error handling only

## Contributing
1. Fork and branch: git checkout -b feature/your-feature
2. Commit: git commit -m "Feature desc"
3. Push: git push origin feature/your-feature
4. Open a PR.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments
- Ollama for the local AI infrastructure
- Google for the gemma3:1b model
- All open-source projects that made this possible
  
##
Built with ❤️ by Farbest AI Engineering (Gary)
