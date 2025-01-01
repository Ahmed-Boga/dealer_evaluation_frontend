# Dealer Evaluation Frontend

This repository contains the Dealer Evaluation Frontend project, which is a web application designed for comparing product prices across different dealers. The application uses Flask for the backend, HTML for the frontend, and Docker for containerization.

---

## Project Structure

```
.
├── app.py                # Main Flask application
├── Dockerfile            # Docker configuration file
├── requirements.txt      # Python dependencies
├── html/
│   └── index.html        # Frontend HTML file
```

---

## Features

- Displays a dropdown of available products.
- Fetches dealer information for the selected product.
- Displays price details for a dealer or all dealers in a table format.
- Responsive and interactive UI.
- Integrated backend for serving the frontend and handling API requests.

---

## Setup Instructions

### Prerequisites

Ensure the following are installed:

- [Python 3.8](https://www.python.org/downloads/)
- [Docker](https://www.docker.com/)

### Steps to Run Locally

1. **Clone the Repository**
    
    ```
    git clone https://github.com/yourusername/dealer-evaluation-frontend.git
    cd dealer-evaluation-frontend
    ```
    
2. **Install Dependencies**
    
    ```
    pip install -r requirements.txt
    ```
    
3. **Run the Application**
    
    ```
    python app.py
    ```
    
    Access the application at `http://127.0.0.1:5001`.
    

---

## Docker Instructions

### Build the Docker Image

```
docker build -t dealer-evaluation-frontend .
```

### Run the Docker Container

```
docker run -p 5001:5001 dealer-evaluation-frontend
```

Access the application at `http://localhost:5001`.

---

## API Endpoints

### Products and Dealers Integration

This application interacts with two external APIs for product and dealer data:

1. **Products API**
    - URL: `https://prodlist.1mtynpbnwpgm.us-south.codeengine.appdomain.cloud/`
    - Endpoints:
        - `GET /products`: Fetches the list of products.
        - `GET /getdealers/<product>`: Fetches dealers for a specific product.
2. **Dealer API**
    - URL: `https://dealerdetails.1mtynpbnwpgm.us-south.codeengine.appdomain.cloud/`
    - Endpoints:
        - `GET /price/<dealer>/<product>`: Fetches price of a product from a dealer.
        - `GET /allprice/<product>`: Fetches prices from all dealers for a product.

---

## Frontend Details

### File: `html/index.html`

- **Product Dropdown**: Fetches available products and displays them in a dropdown.
- **Dealer Dropdown**: Fetches dealers for the selected product.
- **Price Display**: Fetches and displays prices for the selected dealer or all dealers.

### Style and Script Integration

- **Axios**: Used for making API calls.
- **Inline CSS**: Provides basic styling for table rows and dropdowns.

---

## Development Notes

- Flask runs the backend server on port 5001.
- Docker image is based on `python:3.8-slim-buster` for lightweight containerization.
- Ensure external APIs are accessible before running the application.

---

## Contribution

Feel free to submit issues or pull requests to improve the functionality or add new features.

---

## License

This project is licensed under the MIT License.

---

### Contact
