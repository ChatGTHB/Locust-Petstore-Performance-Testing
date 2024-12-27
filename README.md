# Locust Performance Testing Project

![Locust](https://img.shields.io/badge/Locust-Performance_Testing-2D6DB5?style=for-the-badge)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)

A Locust-based project for performance testing RESTful APIs. This project simulates multiple users interacting with API endpoints to evaluate the system's behavior under load.

**Target API**: [Swagger Petstore](https://petstore.swagger.io)  
**Report**: [View Full Test Report](./reports/report_1735264922.9668682.html)

---

## 🚀 Features

- Simulates API requests for user management.
- Performs the following tasks:
  - Create user (`POST /v2/user`)
  - Update user (`PUT /v2/user/<username>`)
  - Retrieve user information (`GET /v2/user/<username>`)
  - Delete user (`DELETE /v2/user/<username>`)
- Provides performance metrics like request per second (RPS), response time, and error rates.
- Configurable user count and spawn rate.

---

## 📂 Project Structure

```
LocustPerformanceTest/
├── UserTest.py              # Locust task definitions
├── requirements.txt         # Python dependencies
├── README.md                # Project documentation
└── reports/                 # Test reports and CSV files
    ├── report_1735264922.9668682.html
    ├── failures_1735265107.5026798.csv
    ├── exceptions_1735265110.4368029.csv
    └── requests_1735265102.7598166.csv
```

---

## 🛠️ Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/ChatGTHB/LocustPerformansTest.git
   cd LocustPerformanceTest
   ```

2. **Install Dependencies**
   - Ensure you have Python 3.8+ installed.
   - Use the `requirements.txt` file to install dependencies:
     ```bash
     pip install -r requirements.txt
     ```

3. **Verify Locust Installation**
   ```bash
   locust --version
   ```

---

## ⚙️ Usage

### Running the Locust Test
1. **Start Locust**
   ```bash
   locust -f UserTest.py
   ```

2. **Open the Locust Web Interface**
   - Navigate to [http://localhost:8089](http://localhost:8089) in your browser.

3. **Configure the Test**
   - Set the number of users and spawn rate.
   - Click **Start Swarming**.

---

## 🔍 Tasks

### 1. **Create User**
   - Endpoint: `POST /v2/user`
   - Payload:
     ```json
     {
       "id": 249897,
       "username": "denemekullanici",
       "firstName": "deneme",
       "lastName": "kullanici",
       "email": "denemekullanici@gmail.com",
       "password": "123456789",
       "phone": "5362264319",
       "userStatus": 0
     }
     ```

### 2. **Update User**
   - Endpoint: `PUT /v2/user/<username>`
   - Payload:
     ```json
     {
       "id": 24985,
       "username": "guncelkullanici",
       "firstName": "guncel",
       "lastName": "kullanici",
       "email": "guncelkullanici@gmail.com",
       "password": "123456",
       "phone": "5452126585",
       "userStatus": 0
     }
     ```

### 3. **Get User Info**
   - Endpoint: `GET /v2/user/<username>`

### 4. **Delete User**
   - Endpoint: `DELETE /v2/user/<username>`

---

## 📊 Results and Metrics

- After running the test, the Locust web interface provides:
  - Requests per second (RPS)
  - Response time distribution
  - Failure rates and errors

### 📂 Test Reports

- [View Full Test Report (HTML)](./reports/report_1735264922.9668682.html)  
- [Failures Report (CSV)](./reports/failures_1735265107.5026798.csv)  
- [Exceptions Report (CSV)](./reports/exceptions_1735265110.4368029.csv)  
- [Requests Statistics (CSV)](./reports/requests_1735265102.7598166.csv)  

---

## 📝 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## ❓ Contact

For any questions or issues, please open an issue in this repository.

