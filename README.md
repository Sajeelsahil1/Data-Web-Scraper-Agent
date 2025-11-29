🤖 AI Data Web Scraper Agent

An intelligent, autonomous web agent powered by Google Gemini 2.5 Flash and Playwright. This agent can browse any website, plan its own actions, handle dynamic content, and scrape structured data based on simple natural language goals.

Note: This agent uses "Stealth Mode" to bypass basic bot detection on sites like Amazon, eBay, and Etsy.

🚀 Features

🧠 AI Brain: Uses Gemini 2.5 Flash to analyze page layouts and decide next steps (Click, Type, Scrape).

👀 Computer Vision (Text-Based): Simplifies complex HTML DOM into an AI-readable format to save tokens and improve accuracy.

🕵️ Stealth Mode: Includes anti-bot detection measures (User-Agent rotation, navigator.webdriver masking).

🔄 Auto-Correction: If a selector fails or content isn't loaded, the agent waits and retries or adapts its strategy.

🔗 Smart Scraping: Automatically associates text (like prices) with their relevant links.

🛠️ Prerequisites

Python 3.8+

A Google Gemini API Key (Get it here)

📦 Installation

Clone the repository

git clone [https://github.com/Sajeelsahil1/Data-Web-Scraper-Agent.git](https://github.com/Sajeelsahil1/Data-Web-Scraper-Agent.git)
cd Data-Web-Scraper-Agent


Install Python dependencies

pip install playwright beautifulsoup4 google-generativeai


Install Browser Binaries

playwright install


⚙️ Configuration

Open webautomationagent.py (or your main script file) and look for the configuration section at the top.

Replace the placeholder with your actual API key:

# ==========================================
# CONFIGURATION
# ==========================================
GEMINI_API_KEY = "YOUR_REAL_API_KEY_HERE" 


🏃 Usage

Run the agent from your terminal:

python webautomationagent.py


The agent will interactively ask you for the target and goal:

🤖 AI Web Agent Initialized.
-----------------------------------
🌐 Enter the URL to start at: [https://www.ebay.com](https://www.ebay.com)
🎯 What should I do?: Search for 'latest winter boys jacket' and save prices and links


📂 Output

The scraped data is automatically saved to a JSON file in the project directory:

gemini_agent_results.json

Example Output:

[
  {
    "step": 9,
    "data": [
      {
        "text": "Boys Winter Jacket Puffer...",
        "link": "[https://www.ebay.com/itm/12345](https://www.ebay.com/itm/12345)..."
      }
    ]
  }
]


🤝 Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements.

📄 License

This project is open-source and available under the MIT License.
