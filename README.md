# Credit Card Fraud Detection

A web-based application for detecting fraudulent credit card transactions using machine learning. This project provides a simple and intuitive interface for real-time fraud detection.

## 🚀 Features

- **Real-time Fraud Detection**: Instant analysis of credit card transactions
- **Web-based Interface**: User-friendly HTML interface for input and results
- **Machine Learning Model**: Uses a pre-trained decision tree model for predictions
- **RESTful API**: JSON-based API endpoints for integration
- **Probability Scoring**: Provides fraud probability scores for each transaction

## 📋 Prerequisites

Before running this application, make sure you have the following installed:

- Python 3.7 or higher
- pip (Python package installer)

## 🛠️ Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd Credit-Card-Fraud-Detection
   ```

2. **Create a virtual environment (recommended)**
   ```bash
   python -m venv myenv
   ```

3. **Activate the virtual environment**
   - On Windows:
     ```bash
     myenv\Scripts\activate
     ```
   - On macOS/Linux:
     ```bash
     source myenv/bin/activate
     ```

4. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

## 🚀 Usage

### Running the Application

1. **Start the Flask server**
   ```bash
   python app.py
   ```

2. **Access the application**
   - Open your web browser and navigate to `http://localhost:5000`
   - The application will be available on port 5000 by default

### Using the Web Interface

1. **Enter Transaction Details**:
   - Transaction Amount: Enter the monetary value of the transaction
   - Transaction Type: Specify the type of transaction (e.g., "online", "in-store", "atm")

2. **Submit for Analysis**:
   - Click the "Check for Fraud" button
   - The system will analyze the transaction and provide results

3. **Review Results**:
   - **Green Alert**: No fraud detected (safe transaction)
   - **Red Alert**: Fraud detected (suspicious transaction)
   - Probability score indicates the confidence level of the prediction

### API Usage

The application also provides a REST API endpoint for programmatic access:

**Endpoint**: `POST /predict-fraud`

**Request Body**:
```json
{
    "amount": 150.00,
    "transactionType": "online"
}
```

**Response**:
```json
{
    "isFraud": false,
    "probability": 0.2345
}
```

## 📁 Project Structure

```
Credit-Card-Fraud-Detection/
├── app.py                      # Main Flask application
├── requirements.txt            # Python dependencies
├── decision_tree_model.h5      # Pre-trained machine learning model
├── templates/
│   └── index.html             # Web interface template
├── myenv/                     # Virtual environment (created during setup)
└── README.md                  # This file
```

## 🔧 Configuration

### Environment Variables

- `PORT`: Set the port number for the Flask application (default: 5000)

### Model Configuration

The application uses a pre-trained decision tree model stored in `decision_tree_model.h5`. The model is loaded automatically when the application starts.

## 🛡️ Security Considerations

⚠️ **Important**: This is a demonstration application. For production use:

- Implement proper authentication and authorization
- Use HTTPS for secure communication
- Add input validation and sanitization
- Implement rate limiting
- Use environment variables for sensitive configuration
- Consider using a production-grade WSGI server

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## ⚠️ Disclaimer

This application is for educational and demonstration purposes only. The fraud detection model provided is simplified and should not be used for actual financial transactions without proper validation and testing.

## 🆘 Support

If you encounter any issues or have questions:

1. Check the existing issues in the repository
2. Create a new issue with detailed information about your problem
3. Include error messages, system information, and steps to reproduce

## 🔮 Future Enhancements

- [ ] Add more transaction features (location, time, merchant category)
- [ ] Implement user authentication
- [ ] Add transaction history and analytics
- [ ] Support for multiple machine learning models
- [ ] Real-time model retraining capabilities
- [ ] Integration with external fraud detection services
