# Registration Info RAG

## Overview

This project is a Flask-based server designed to handle a registration information retrieval system using Retrieval-Augmented Generation (RAG). The primary functionality of this server is to answer queries related to registration information by leveraging a combination of retrieval and generative AI techniques.

## Features

- Handles user queries related to registration information.
- Utilizes a retrieval-augmented generation approach to provide accurate and relevant answers.
- Provides a Flask-based API for easy integration with other applications.
- Includes an ngrok setup for exposing the local server to the internet.

## Setup

### Prerequisites

Before you begin, ensure you have the following installed:

- Python 3.7 or higher
- Flask
- Flask-CORS
- ngrok

### Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/registration-info-rag.git
   cd registration-info-rag
   ```

2. **Install dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

3. **Start the Flask server:**

   ```bash
   python app.py
   ```

4. **Start ngrok:**

   ```bash
   ngrok http 5000
   ```

   This will provide a public URL to access the Flask server.

## Usage

### API Endpoints

- **Home Endpoint**

  ```http
  GET /
  ```

  Returns a welcome message indicating the server is running.

- **Query Endpoint**

  ```http
  POST /query
  ```

  Expects a JSON payload with the following structure:

  ```json
  {
      "question": "Your question here"
  }
  ```

  **Example:**

  ```bash
  curl -X POST http://localhost:5000/query -H "Content-Type: application/json" -d '{"question":"What is the registration deadline?"}'
  ```

  **Response:**

  ```json
  {
      "response": "The registration deadline is July 31st."
  }
  ```

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Create a new Pull Request.

## Acknowledgements

This project was created using the Flask framework and leverages ngrok for local development. Special thanks to the open-source community for their contributions and support.
