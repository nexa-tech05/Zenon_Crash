# Zenon Crash Server

A clean, functional Express.js server for the Zenon Crash project.

## 🚀 Quick Start

### Prerequisites
- Node.js (v14 or higher)
- npm or yarn

### Installation

1. Clone the repository
```bash
git clone https://github.com/nexa-tech05/Zenon_Crash.git
cd Zenon_Crash
```

2. Install dependencies
```bash
npm install
```

3. Create environment configuration
```bash
cp .env.example .env
```

4. Start the server
```bash
npm start
```

The server will run on `http://localhost:3000`

## 📋 API Endpoints

### Health Check
```
GET /api/health
```
Returns: `{ status: "OK", message: "Server is running" }`

### Get Data
```
GET /api/data
```
Returns:
```json
{
  "success": true,
  "data": {
    "message": "Welcome to Zenon Crash Server",
    "timestamp": "2026-06-26T..."
  }
}
```

### Submit Message
```
POST /api/submit
Content-Type: application/json

{
  "message": "Your message here"
}
```

Returns:
```json
{
  "success": true,
  "received": "Your message here",
  "processedAt": "2026-06-26T..."
}
```

## 📁 Project Structure

```
.
├── public/
│   └── index.html          # Web interface
├── main.js                 # Express server setup
├── package.json            # Dependencies & scripts
├── .env.example            # Environment template
├── .gitignore             # Git ignore rules
└── README.md              # This file
```

## 🛠️ Development

### Environment Variables
- `PORT` - Server port (default: 3000)
- `NODE_ENV` - Environment (development/production)

### Testing Endpoints

Use the web interface at `http://localhost:3000` to test the API, or use curl:

```bash
# Health check
curl http://localhost:3000/api/health

# Get data
curl http://localhost:3000/api/data

# Submit message
curl -X POST http://localhost:3000/api/submit \
  -H "Content-Type: application/json" \
  -d '{"message":"Hello"}'
```

## 📦 Dependencies

- **express** - Web framework
- **cors** - Cross-Origin Resource Sharing
- **dotenv** - Environment variables

See `package.json` for the full list of dependencies.

## ⚠️ Security Notes

- Never commit `.env` files with sensitive data
- Keep `NODE_ENV=production` in production
- Validate all user inputs
- Use HTTPS in production

## 📄 License

MIT License - See LICENSE file for details

## 👤 Author

Toxxic

---

**Last Updated:** June 26, 2026
