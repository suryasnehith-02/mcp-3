This is a simple MCP (Model Context Protocol) GitHub Server built using Node.js and Express.js. It interacts with the GitHub API to retrieve user information, list repositories, and create new repositories.

Features:
Fetch authenticated GitHub user details
List all repositories of the authenticated user
Create a new repository

Prerequisites:
Before running the server, ensure you have:
Node.js installed (>= v14 recommended)
A GitHub personal access token with repo permissions

Install dependencies:
npm install
This project requires the following dependencies:
express: For handling HTTP requests
axios: For making API requests to GitHub
dotenv: For managing environment variables

Create a .env file in the project root and add your GitHub token: GITHUB_TOKEN=your_github_personal_access_token PORT=3000

Start Server: npm start

API Endpoints
1. Get GitHub User Details
GET /github/user
2. Get User Repositories
GET /github/repos
3. Create a New Repository
POST /github/create-repo

Testing with curl:

curl -X GET http://localhost:3000/github/user
curl -X GET http://localhost:3000/github/repos
curl -X POST http://localhost:3000/github/create-repo \
-H "Content-Type: application/json" \
-d '{"name": "new-repo", "description": "A test repo", "privateRepo": true}'

License
This project is open-source and available under the MIT License.


