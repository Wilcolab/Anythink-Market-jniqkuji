# My Express App

This project is a simple Express server scaffolded to listen on port 8001. It uses Nodemon for automatic code updates during development.

## Project Structure

```
my-express-app
├── src
│   └── app.js          # Entry point of the application
├── package.json        # Configuration file for npm
├── nodemon.json        # Configuration for Nodemon
├── Dockerfile          # Instructions to build the Docker image
└── README.md           # Project documentation
```

## Getting Started

To set up and run the server, follow these steps:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Wilcolab/Anythink-Market-jniqkuji.git
   cd my-express-app
   ```

2. **Install dependencies:**
   ```bash
   yarn install
   ```

3. **Run the server:**
   ```bash
   yarn start
   ```

The server will start and listen on port 8001.

## Docker

To build and run the application using Docker, use the following commands:

1. **Build the Docker image:**
   ```bash
   docker build -t my-express-app .
   ```

2. **Run the Docker container:**
   ```bash
   docker run -p 8001:8001 my-express-app
   ```

The application will be accessible at `http://localhost:8001`.

## License

This project is licensed under the MIT License.