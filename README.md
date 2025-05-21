# X AI Agent

An intelligent agent that can interact with Twitter (X) using natural language commands through a Gemini-powered AI interface.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js and npm**: Download and install from [nodejs.org](https://nodejs.org)
- **Git**: For cloning the repository

### API Keys Required

- **Google Gemini API Key**: Obtain from [Google AI Studio](https://ai.google.dev/)
- **Twitter (X) API v2 Keys**: You'll need an approved Developer Account and an App set up on the Twitter Developer Portal with Read and Write permissions:
  - App Key (Consumer Key / API Key)
  - App Secret (Consumer Secret / API Secret Key)
  - Access Token
  - Access Token Secret

> **Note**: Due to recent Twitter API changes, posting tweets might require a paid API tier.

## Installation & Setup

### Clone the repository:

```bash
git clone https://github.com/Faizan123post/Twitter-AI-agent.git
cd Twitter-AI-agent/mcp-server-main
```

### Set up the Server:

1. Navigate to the server directory:
```bash
cd server
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env` file in the server directory (`mcp-server-main/server/.env`) and add your Twitter API credentials:
```
TWITTER_API_KEY=YOUR_TWITTER_APP_KEY
TWITTER_API_SECRET=YOUR_TWITTER_APP_SECRET
TWITTER_ACCESS_TOKEN=YOUR_TWITTER_ACCESS_TOKEN
TWITTER_ACCESS_TOKEN_SECRET=YOUR_TWITTER_ACCESS_TOKEN_SECRET
```

### Set up the Client:

1. Navigate to the client directory:
```bash
cd ../client  # If you were in the server directory
```
or
```bash
cd client     # If you were in mcp-server-main root
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env` file in the client directory (`mcp-server-main/client/.env`) and add your Google Gemini API Key:
```
GEMINI_API_KEY=YOUR_GEMINI_API_KEY
```

## Running the Application

You will need two separate terminal windows.

### Start the MCP Server:

1. Open a terminal and navigate to the server directory:
```bash
cd server     # Assuming you are in mcp-server-main/
```

2. Run the server:
```bash
node index.js
```

You should see the output: `Server is running on http://localhost:3001`

### Start the AI Client:

1. Open a new terminal window and navigate to the client directory:
```bash
cd client     # Assuming you are in mcp-server-main/
```

2. Run the client:
```bash
node index.js
```

You should see output like:
```
Connected to mcp server
You:
```

## Interacting with the Agent

Type your commands or questions in the client terminal after the "You:" prompt.

Example commands:
- `Can you tweet "Hello from my AI agent!" for me?`
- `What are the latest tweets on my timeline?`
- `Can you search for tweets about #AI?`

## Stopping the Application

To stop the client or server, go to its respective terminal window and press `Ctrl+C`.

## Troubleshooting

- **ECONNREFUSED errors**: Make sure the server is running before starting the client
- **API key errors**: Double-check your API keys in both `.env` files
- **Twitter API limitations**: Some features may require a paid Twitter API tier

## Project Structure

```
mcp-server-main/
├── client/         # AI client powered by Google Gemini
│   ├── index.js
│   └── .env        # Contains Gemini API key
│
└── server/         # MCP server for Twitter integration
    ├── index.js
    └── .env        # Contains Twitter API credentials
```

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

* Google Gemini for AI capabilities
* Twitter API for social media integration
