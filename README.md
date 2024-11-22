# Todo App

This is a simple Todo application built with Golang for the API, Vite React for the frontend, and Kubernetes for deployment.

## Table of Contents

- Installation
- Usage
- Deployment
- Contributing

## Installation

### Backend (Golang API)

1. Navigate to the `backend` directory:
    ```sh
    cd backend
    ```
2. Run the Go server:
    ```sh
    go run main.go
    ```

### Frontend (Vite React)

1. Navigate to the `frontend` directory:
    ```sh
    cd frontend
    ```
2. Install dependencies:
    ```sh
    npm install
    ```
3. Start the development server:
    ```sh
    npm run dev
    ```

## Usage

Once both the backend and frontend servers are running, you can access the application at `http://localhost:3000`.

## Deployment

### Docker Build and Push

1. Build the Docker image for the Go server:
    ```sh
    docker build -t hanyi00i/back:v1 ./backend
    ```
2. Push the Docker image to your repository:
    ```sh
    docker push hanyi00i/back:v1
    ```
3. Build the Docker image for the React frontend:
    ```sh
    docker build -t hanyi00i/front:v1 ./frontend
    ```
4. Push the Docker image to your repository:
    ```sh
    docker push hanyi00i/front:v1
    ```

### Kubernetes

1. Ensure you have Kubernetes and Docker installed and configured.
2. Apply the Kubernetes configuration:
    ```sh
    kubectl apply -f kubernetes
    ```

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.
