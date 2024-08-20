

# Echo Rift Backend

## Overview

Welcome to the Echo Rift backend repository! Echo Rift is a fast-paced, team-based game inspired by Echo Arena And Lone Echo 1. This repository contains the backend services and infrastructure needed to support Echo Rift’s dynamic gameplay.

## Table of Contents

- [Project Structure](#project-structure)
- [Setup & Installation](#setup--installation)
- [Configuration](#configuration)
- [API Documentation](#api-documentation)
- [Development](#development)
- [Testing](#testing)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)

## Project Structure

Here's a brief overview of the project structure:

```
/echo-rift-backend
│
├── /src
│   ├── /controllers        # Business logic for handling game operations
│   ├── /models             # Database models
│   ├── /routes             # API routes
│   ├── /services           # External service integrations
│   └── /utils              # Utility functions and helpers
│
├── /config                 # Configuration files
├── /scripts                # Helper scripts for setup and maintenance
├── /tests                  # Unit and integration tests
├── /docs                   # Documentation
├── Dockerfile              # Docker configuration
└── README.md               # This file
```

## Setup & Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/WeCan-Games/echo-rift-backend.git
   cd echo-rift-backend
   ```

2. **Install Dependencies**

   Make sure you have [Node.js](https://nodejs.org/) (v14 or higher) and [npm](https://www.npmjs.com/) installed. Then, run:

   ```bash
   npm install
   ```

3. **Environment Configuration**

   Create a `.env` file in the root directory and add your configuration variables. You can refer to the `.env.example` file for required environment variables.

   ```env
   DB_HOST=localhost
   DB_PORT=5432
   DB_USER=youruser
   DB_PASS=yourpassword
   PORT=5000
   ```

4. **Run the Application**

   To start the server in development mode:

   ```bash
   npm run dev
   ```

   For production mode:

   ```bash
   npm start
   ```

## Configuration

Configuration files are located in the `/config` directory. Key configuration settings include:

- **Database Connection:** Configurations for connecting to the database.
- **Server Settings:** Port, environment, and other server-related settings.

## API Documentation

The Echo Rift backend provides a set of RESTful APIs. API documentation is located in the `/docs` directory and can be generated using tools like Swagger or Postman.

### Example Endpoints

- **GET /api/games** - Retrieve a list of ongoing games.
- **POST /api/players** - Register a new player.
- **PUT /api/games/{gameId}** - Update game state.
- **DELETE /api/games/{gameId}** - Delete a game.

## Development

To contribute to the development of Echo Rift:

1. **Branching Strategy**

   - Create a new branch for each feature or bugfix: `git checkout -b feature/your-feature-name`
   - Commit your changes: `git commit -am 'Add new feature'`
   - Push to the branch: `git push origin feature/your-feature-name`

2. **Code Style**

   - Follow the coding conventions specified in the `.eslintrc.json` file.
   - Ensure code is well-commented and maintainable.

3. **Submit a Pull Request**

   - Create a pull request from your feature branch to `main`.
   - Ensure all tests pass and include a description of your changes.

## Testing

To run tests:

```bash
npm test
```

Tests are located in the `/tests` directory and cover both unit and integration testing. You can use [Jest](https://jestjs.io/) or [Mocha](https://mochajs.org/) as your testing framework.

## Deployment

For deployment:

1. **Build the Docker Image**

   ```bash
   docker build -t echo-rift-backend .
   ```

2. **Run the Docker Container**

   ```bash
   docker run -p 5000:5000 --env-file .env echo-rift-backend
   ```

3. **Deployment Scripts**

   Deployment scripts for cloud providers or servers are located in the `/scripts` directory.

## Contributing

We welcome contributions! Please read our [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on how to contribute.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
