# ✈️WhatsApp Flight Booking Bot



A simple and smart WhatsApp chatbot that helps users check real-time flight details and search for cheap flights using natural language messages.
Built with Python (Flask), Twilio WhatsApp API, and AviationStack API, the bot can understand user queries, detect flight routes, and return the best available flights instantly.

🚀 Features

Chat-based flight search
Users can simply text “Find flights from Delhi to Dubai” on WhatsApp.

AI understanding
Extracts cities, date, and details from natural language messages.

Real-Time Flight Information
Fetches flight prices and schedules using AviationStack API.

Fallback mode
If API fails, the bot uses sample/mock data to respond.

Easy booking links
Direct links to Skyscanner, Kayak, etc.

Status endpoints
Includes / and /health for deployment checks.

🧰 Tech Used

Python + Flask – Backend

Twilio WhatsApp API – Messaging

AviationStack API – Live flight data

HuggingFace API – Query understanding

Requests / Regex – Data extraction

dotenv – Secure environment variables

📁 Project Structure
project/
├── app.py
├── requirements.txt
├── Procfile
├── demo/
│   └── demo.gif
└── README.md


## How to Run

### 1\. Clone the Repository

```bash
git clone https://github.com/username/repo-name
cd repo-name
```

### 2\. Set Up Environment Variables

Create a `.env` file in the root directory and populate it with your API keys and credentials.

```
TWILIO_ACCOUNT_SID=your_twilio_account_sid
TWILIO_AUTH_TOKEN=your_twilio_auth_token
TWILIO_PHONE_NUMBER=whatsapp:+14155238886
AVIATION_STACK_API_KEY=your_aviation_stack_api_key
HUGGINGFACE_API_KEY=your_hugging_face_api_key  # Optional
```

### 3\. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4\. Run the Application

```bash
python main.py
```

### 5\. Configure Twilio Webhook

  - The application will run on `http://localhost:5000`. To expose this to the internet, you'll need a tunneling service like **ngrok** or **Cloudflare Tunnel**.

<!-- end list -->

```bash
ngrok http 5000
```

  - Copy the `https://` URL provided by ngrok.
  - In your **Twilio Console**, navigate to **Develop \> Messaging \> Senders \> WhatsApp Senders**.
  - Find your Twilio WhatsApp number and paste the ngrok URL followed by `/webhook` into the `A MESSAGE COMES IN` field. For example: `https://your-ngrok-url.ngrok.io/webhook`.

You can now send a WhatsApp message to your Twilio number to start interacting with the bot\!

-----

## Demo

![Demo GIF](demo/demo.gif)

-----

## Author

**Manu JP**

  - GitHub: [@https://github.com/mj110805)
  - LinkedIn: [https://www.linkedin.com/in/manu-jayaprakash-2a6a6527b)
