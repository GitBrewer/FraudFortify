# FRAUDFORTIFY
## Multi-Domain Fraud Detection System

## Overview
The Multi-Domain Fraud Detection System is an advanced platform for detecting fraudulent activities across three key domains:

1. **GPT-Generated Text Detection**
2. **Credit Card Fraud Detection**
3. **Automobile Fraud Detection**

The application combines machine learning models, an intuitive user interface, and robust authentication mechanisms to deliver accurate and secure fraud detection services.

---

## Features

### User Interface
- Built using **Streamlit** for interactivity and ease of use.
- Includes a visually appealing sidebar with user registration and login options.
- Supports dynamic fraud detection pages for different domains.
- Enhanced styling using **HTML** and **CSS**.

### User Authentication
- **OTP-based Authentication** via Telegram.
- Validates usernames and emails during registration.
- Securely stores user credentials in an **SQLite** database.
- OTP expires after 30 seconds to ensure security.

### Fraud Detection Modules
- **GPT-Generated Text Detection**: Analyzes text perplexity to differentiate between human-written and AI-generated content.
- **Credit Card Fraud Detection**: Utilizes an **Artificial Neural Network (ANN)** to classify transactions as fraudulent or normal.
- **Automobile Fraud Detection**: Employs supervised learning models to predict fraudulent insurance claims based on user inputs.

### Database Management
- SQLite database (`users.db`) to manage user credentials.
- Stores information like username, email, name, and location.

### Telegram Integration
- Sends OTPs securely via the **Telegram Bot API**.
- Includes error handling for OTP delivery issues.

### Session Management
- **Streamlit Session State** manages:
  - OTPs
  - Timer functionality
  - User login state

---

## Installation

### Prerequisites
- Python 3.8+
- Required Python libraries:
  - `streamlit`
  - `pandas`
  - `numpy`
  - `sqlite3`
  - `requests`
  - `random`
  - `time`
  - `torch`
  - `transformers`
  - `joblib`

### Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/multi-domain-fraud-detection.git
   cd multi-domain-fraud-detection
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Set up environment variables for Telegram Bot API:
   ```bash
   export TELEGRAM_BOT_TOKEN=<your-telegram-bot-token>
   ```

4. Initialize the SQLite database:
   ```bash
   python initialize_db.py
   ```

5. Run the application:
   ```bash
   streamlit run app.py
   ```

---

## Usage

### User Registration
1. Open the application.
2. Navigate to the registration form in the sidebar.
3. Enter your name, email, username, and location.
4. Complete the registration process.

### Login with OTP
1. Enter your username.
2. Request an OTP.
3. Check your Telegram account for the OTP.
4. Enter the OTP within 30 seconds to log in.

### Fraud Detection
1. Choose a fraud detection module from the sidebar.
2. Provide the required inputs (e.g., text, CSV file, or form inputs).
3. View results and insights on fraud detection.

---

## Project Structure

```
.
├── app.py                # Main Streamlit application
├── initialize_db.py      # Script to initialize SQLite database
├── models/               # Pre-trained machine learning models
├── utils/                # Utility scripts (e.g., OTP generation, Telegram integration)
├── templates/            # HTML and CSS files for styling
├── Dataset/              # Sample datasets
└── README.md             # Project documentation
```

---

## Security
- **Data Privacy**: User data is securely stored in the SQLite database.
- **Authentication Security**: OTP-based login with expiration to prevent misuse.
- **Telegram Integration**: Ensures secure and reliable OTP delivery.

---

## Future Enhancements
1. **GPT-Generated Text Detection**:
   - Add detection for AI-generated images and videos.
   - Improve NLP techniques for greater accuracy.

2. **Credit Card Fraud Detection**:
   - Real-time transaction monitoring.
   - Support for multi-currency fraud detection.

3. **Automobile Fraud Detection**:
   - Integrate IoT-based telematics data.
   - Provide enhanced insurance policy recommendations.

4. **User Management**:
   - Add role-based access control.
   - Provide admin dashboards for fraud analytics.

---

## Contributing
Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch (`feature/your-feature-name`).
3. Commit your changes.
4. Push the branch and submit a pull request.

---

## License
This project is licensed under the MIT License. See the LICENSE file for details.

---

## Contact
For any questions or feedback, please contact:
- **Email**: arjunpundir.301@gmail.com


