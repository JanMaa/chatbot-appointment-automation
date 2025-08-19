# Chatbot Automation with Botpress, Calendly API, and Google Apps Script API

## 📌 Overview
This project is a **chatbot automation** built using **Botpress**, integrated with **Calendly API** for appointment scheduling and **Google Apps Script API** for lead management.  

The bot collects user information (name, email, phone, type of service), confirms details, and allows users to book appointments via Calendly. All user interaction data is then sent to a Google Apps Script API for storage and marketing purposes.

---

## ⚙️ Features
- **Greeting & Options**
  - Welcomes users.
  - Offers options to ask questions or book an appointment.

- **User Data Collection**
  - First Name  
  - Last Name  
  - Email  
  - Phone Number  
  - Type of Service (Tax Consultation, Financial Planning, Accounting Services)

- **Data Confirmation**
  - Asks the user to confirm collected details.
  - Allows modifications (first name, last name, email, or service type).

- **Calendly Integration**
  - Redirects user to Calendly booking link.  
  - Tracks booking status.  
  - Confirms appointment once completed.

- **Google Apps Script Integration**
  - Sends qualified leads data to Google Apps Script endpoint.  
  - Stores booking details for reporting and marketing.

- **Knowledge QA**
  - Handles FAQs with fallback messages if no answer is available.
  - Option for users to ask more questions.

- **Post-Interaction Flow**
  - Confirms booking.  
  - Ends the conversation if no further action is required.  

---

## 🛠️ Tech Stack
- **Botpress** – Chatbot automation framework  
- **Calendly API** – Appointment scheduling & booking tracking  
- **Google Apps Script API** – Lead data storage & marketing automation  
- **Webhook/API Calls** – For data exchange between systems  

---

## 🔄 Workflow Summary
1. **Start Conversation** → Greet user → Provide options  
2. **Collect Details** → Name, Email, Phone, Service Type  
3. **Confirm Details** → Modify if needed  
4. **Calendly Booking** → Redirect user to booking page → Confirm booking  
5. **Data Handling**  
   - Send user details to Google Apps Script  
   - Store booking information  
   - Track leads for marketing  
6. **Conversation End**  

---

## 🖼️ Bot Workflow Diagram
![Botpress Flow](./bot-flow.pg)  
*(This diagram shows the chatbot conversation flow, including Calendly and Google Apps Script API integrations.)*  

---

## 🚀 Setup Instructions

### 1. Botpress Installation
- Install [Botpress](https://botpress.com/).
- Import the chatbot flow into your Botpress workspace.

### 2. Calendly API Setup
- Generate a **Personal Access Token (PAT)** from Calendly.
- Add API calls in Botpress for:
  - Creating booking links.  
  - Retrieving scheduled events.  

### 3. Google Apps Script API
- Create a new Apps Script project.
- Deploy as a **Web App** with accessible endpoint.
- Connect Botpress via API call to store leads data.

### 4. Environment Variables
Configure Botpress environment with:
```env
CALENDLY_API_KEY=your_calendly_api_key
GOOGLE_APPS_SCRIPT_URL=your_google_script_webapp_url
```

### 5. Run the Bot
- Start Botpress server.
- Test the chatbot in your preferred channel (Webchat, Messenger, etc.).

---

## 📂 Project Structure
```
📦 chatbot-automation
 ┣ 📜 README.md
 ┣ 📜 bot-flow.png   # Bot workflow screenshot
 ┣ 📜 environment.env
 ┗ 📂 botpress-bot-files
```

---

## ✅ Future Enhancements
- Add support for multiple calendar integrations.  
- Enable automated email/SMS reminders.  
- Expand FAQ knowledge base with AI-driven responses.  

---

## 👨‍💻 Author
Developed by **Janric Malate**  
For inquiries, reach out at **janricmalate@gmail.com**
