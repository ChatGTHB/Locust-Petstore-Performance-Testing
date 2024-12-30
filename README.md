# Locust Petstore Performance Testing

![Locust](https://img.shields.io/badge/Locust-Performance_Testing-2D6DB5?style=for-the-badge)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)

A Locust-based project designed to perform load and stress testing on the [Swagger Petstore API](https://petstore.swagger.io). This project simulates concurrent users interacting with API endpoints, measuring the system's performance and responsiveness.

---

## 🌐 Target API

- **API Endpoint**: [Swagger Petstore](https://petstore.swagger.io)
- **Version**: v2  
- **Focus**: User management endpoints, including creating, updating, retrieving, and deleting users.

---

## 🚀 Features

- Performance testing for CRUD operations on user data.
- Simulates API requests to:
  - **Create User** – `POST /v2/user`
  - **Update User** – `PUT /v2/user/<username>`
  - **Get User Info** – `GET /v2/user/<username>`
  - **Delete User** – `DELETE /v2/user/<username>`
- Tracks response time, failure rates, and throughput metrics.

---

## 💂️ Project Structure

```
locust-petstore-performance-testing/
├── UserTest.py              # Locust task definitions
├── requirements.txt         # Python dependencies
├── README.md                # Project documentation
└── reports/                 # Test reports and CSV files
    ├── report_1735264922.html
    ├── failures_1735265107.csv
    ├── exceptions_1735265110.csv
    └── requests_1735265102.csv
```

---

## 🛠️ Installation

1. **Clone the Repository**  
   ```bash
   git clone https://github.com/cihat-kose/locust-petstore-performance-testing.git
   cd locust-petstore-performance-testing
   ```

2. **Install Dependencies**  
   Ensure Python 3.8+ is installed.  
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

2. **Access Locust Web Interface**  
   Open [http://localhost:8089](http://localhost:8089) in your browser.

3. **Configure Test Parameters**  
   - Set the number of users and spawn rate.  
   - Click **Start Swarming** to begin the test.

---

## 🔍 Example API Tasks

### 1. **Create User**

- Endpoint: `POST /v2/user`  
- Example Payload:  
   ```json
   {
     "id": 249897,
     "username": "testuser",
     "firstName": "Test",
     "lastName": "User",
     "email": "testuser@gmail.com",
     "password": "12345678",
     "phone": "1234567890",
     "userStatus": 0
   }
   ```

---

### 2. **Update User**

- Endpoint: `PUT /v2/user/testuser`  
- Example Payload:  
   ```json
   {
     "firstName": "Updated",
     "lastName": "User"
   }
   ```

---

### 3. **Retrieve User Info**

- Endpoint: `GET /v2/user/testuser`

---

### 4. **Delete User**

- Endpoint: `DELETE /v2/user/testuser`

---

## 📊 Results and Reports

After executing tests, results can be found in the `reports/` directory. The Locust web interface also provides real-time data:  
- **Requests per second (RPS)**  
- **Response time distribution**  
- **Failures and exceptions**  

### 📂 Example Reports

- [Full Test Report (HTML)](./reports/report_1735264922.html)  
- [Failures (CSV)](./reports/failures_1735265107.csv)  
- [Exceptions (CSV)](./reports/exceptions_1735265110.csv)  
- [Request Stats (CSV)](./reports/requests_1735265102.csv)  

---

## 📉 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## ❓ Contact

If you encounter any issues, please open an issue in this repository.

