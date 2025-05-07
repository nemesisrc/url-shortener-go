# 🔗 URL Shortener - A Go Project 🚀  

A fast and efficient URL shortener built with **Go** (Golang) that converts long URLs into short, manageable links. Perfect for sharing and tracking!  

---

## ✨ Features  

- **⚡ Blazing Fast** – Built with Go for high performance  
- **🔒 Persistent Storage** – Uses **Redis** for storing shortened URLs  
- **🌍 REST API** – Easy integration with frontends or other services  
- **📊 Analytics** – Track click counts (optional)  
- **🐳 Docker Support** – Easy deployment with containers  

---

## 🛠️ Installation  

### Prerequisites  
- Go (≥1.20)  
- Redis (for storage)  

### Steps  
1. Clone the repo:  
   ```sh
   git clone https://github.com/yourusername/url-shortener-go.git
   cd url-shortener-go
   ```  
2. Install dependencies:  
   ```sh
   go mod download
   ```  
3. Configure `.env`:  
   ```sh
   cp .env.example .env
   # Edit .env with your Redis and server settings
   ```  
4. Run the server:  
   ```sh
   go run main.go
   ```  

---

## 🚀 Usage  

### Shorten a URL  
**Request:**  
```sh
curl -X POST http://localhost:8080/shorten \
  -H "Content-Type: application/json" \
  -d '{"url": "https://your-long-url.com/very-long-path"}'
```  

**Response:**  
```json
{
  "short_url": "http://localhost:8080/abc123",
  "original_url": "https://your-long-url.com/very-long-path"
}
```  

### Redirect to Original URL  
Visit `http://localhost:8080/abc123` to be redirected.  

---

## 🐳 Docker Deployment  

```sh
docker-compose up --build
```  
The service will be available at `http://localhost:8080`.  

---

## 📂 Project Structure  

```
.
├── main.go          # Entry point
├── handlers/        # HTTP request handlers
├── storage/         # Redis storage logic
├── models/          # Data structures
├── go.mod           # Go dependencies
├── Dockerfile       # Container setup
└── docker-compose.yml # Redis + App setup
```

---

## 🤝 Contributing  

PRs and issues are welcome!  
1. Fork the repo  
2. Create a feature branch (`git checkout -b feature/awesome-feature`)  
3. Commit changes (`git commit -m 'Add awesome feature'`)  
4. Push to branch (`git push origin feature/awesome-feature`)  
5. Open a PR  

---

## 📜 License  

MIT © [Your Name](https://github.com/yourusername)  

---

⭐ **Star this repo if you like it!** ⭐  

---

Made with ❤️ and **Go** 🐹