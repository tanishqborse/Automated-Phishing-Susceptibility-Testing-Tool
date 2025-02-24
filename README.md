# Automated Phishing Susceptibility Testing Tool 

A Python-based project to test the susceptibility of users to phishing attacks by sending push notifications through Duo Security and tracking their responses (authorize, deny, or no response). This tool integrates Active Directory enumeration to pull user data, sends push notifications to selected users, and reports on their responses, while securely handling API credentials through environment variables. This tool helps an organisation to understand how employees react to social engineer and phishing attacks, and give them the required cybersecurity training.

---

## 🚀 Features

- **Automated Duo Push**: Sends push notifications to users for authentication attempts.
- **User Selection**: Retrieves users from Active Directory and allows selection of individuals to send pushes to.
- **Track Responses**: Tracks if users authorize, deny, or do nothing on the push.
- **HMAC Authentication**: Secure communication with Duo API using HMAC signature.
- **Environment Variables**: Credentials are managed securely using environment variables.

---

## 📥 Installation

1. Clone this repository to your local machine:

   ```bash
   git clone https://github.com/yourusername/phishing-susceptibility-testing.git
   cd phishing-susceptibility-testing
   ```
2. Install required dependencies:

  ```bash
  pip install -r requirements.txt
  ```
Create a .env file to store your Duo API credentials and Active Directory details (example below):
  ```plaintext
  DUO_API_HOST=api-xxxxxx.duosecurity.com
  DUO_API_KEY=your_api_key
  DUO_API_SECRET=your_api_secret
  DUO_API_SECRET_KEY=your_hmac_secret_key
  ```
Ensure you have Python 3 and the required libraries installed.

**⚡ Usage**
  Run the script:
      Use the command below to start the phishing susceptibility test. Make sure you have the required environment variables set in your .env file.
  ```python phishing_test.py```
  

**Interactive User Selection:**
The script will list all users retrieved from Active Directory.
You will be prompted to select which users to send Duo push notifications to by entering their index number.

**Response Tracking:**
The script tracks whether users authorize, deny, or ignore the push notification.
The results will be displayed after the test.

---
**📌 Example Output**
```perl
    Fetched the following users from Active Directory:
    1. user1@example.com
    2. user2@example.com
    3. user3@example.com
    
    Enter the number(s) of the users to send push to (comma-separated): 1,2
    
    [+] Sending push notification to user1@example.com
    [+] Sending push notification to user2@example.com
    
    [+] Results:
      - Authorized: 1 users
      - Denied: 1 users
      - No Response: 0 users
```
---
**🛠 Requirements**
Python 3.x
requests library
pyad for Active Directory enumeration
python-dotenv for managing environment variables

**To install dependencies:**

```bash
  pip install -r requirements.txt
```
---

**🔥 How It Works**
  Active Directory Enumeration:
  Fetches a list of users from Active Directory.
  Duo Push Notification:
  Sends a push notification to selected users through the Duo API.
  HMAC Signature:
  Ensures the request is authenticated using HMAC signatures for secure communication.
  Tracking User Response:
  Tracks whether a user authorizes, denies, or ignores the push notification.

**Results Reporting:**
After completion, displays the results (authorized, denied, no response).

---

**📜 License**
This project is licensed under the MIT License.


**🤝 Contributing**
🚀 Contributions are welcome! If you have ideas to improve the script or additional features to add, feel free to contribute!


👨‍💻 Developed by Tanishq 

---
