# Bank Statement Aggregator

A Java-based application built with **Spring Boot** that aggregates and processes bank statements (PDF and CSV) to provide a unified view of transactions. 
This project demonstrates the ability to handle file uploads, parse data, and manage transactions using a RESTful API.

---

## Features

- **Upload Bank Statements**: Supports PDF and CSV file formats.
- **Transaction Extraction**: Extracts transaction details (date, description, amount) from uploaded files.
- **Unified View**: Aggregates transactions from multiple statements into a single database.
- **REST API**: Provides endpoints for uploading statements and retrieving transactions.
- **Easy to Run**: Simple setup with Maven and Docker support.

---

## Technologies Used

- **Backend**: Java (Spring Boot)
- **Database**: MySQL
- **PDF Parsing**: Apache PDFBox
- **CSV Parsing**: OpenCSV
- **Build Tool**: Maven
- **Containerization**: Docker (optional)

---

## How to Run

### Prerequisites

- Java 17 or higher
- Maven 3.x
- (Optional) Docker

---

### Running Locally

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/bank-statement-aggregator.git
   cd bank-statement-aggregator

2. **Build the project**:
   ./mvnw clean install
3. **Run the application**:
   ./mvnw spring-boot:run


**API Documentation**
Upload Bank Statement
Endpoint: POST /api/transactions/upload
Description: Upload a bank statement file (PDF or CSV) for processing.
Request:
Method: POST
Content-Type: multipart/form-data

Parameters:

file: The bank statement file to upload.
Response:
Success: 200 OK with a message: "File processed successfully"
Error: 400 Bad Request with an error message.

**Get All Transactions**
Endpoint: GET /api/transactions
Description: Retrieve all transactions stored in the database.
Response:
Success: 200 OK with a list of transactions in JSON format.
