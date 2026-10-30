<p align="center">
  <a href="https://github.com/Brajesh31/Url-shortening-">
    <img src="https://raw.githubusercontent.com/Brajesh31/asset/main/url-shortener-banner.png" alt="URL Shortener Banner">
  </a>
</p>

<div align="center">

# 🔗 URL Shortener Service ⚡

**A fast and simple API service to create short, manageable links from long URLs, complete with click tracking.**

</div>

<p align="center">
  <a href="[LINK_TO_YOUR_LIVE_DEMO]">
    <img src="https://img.shields.io/badge/Live-View_Demo-brightgreen?style=for-the-badge&logo=vercel" alt="Live Demo">
  </a>
  &nbsp;
  <img src="https://img.shields.io/github/stars/Brajesh31/Url-shortening-?style=for-the-badge&color=gold" alt="Stars">
  &nbsp;
  <img src="https://img.shields.io/github/license/Brajesh31/Url-shortening-?style=for-the-badge&color=blue" alt="License">
</p>

---

## ## ✨ Project Overview

This project is a robust URL shortening microservice, similar to services like Bitly or TinyURL. It takes a long, unwieldy URL and generates a short, unique alias. When a user visits the short link, they are instantly redirected to the original destination.

The application is built with a high-performance backend using Node.js and Express, coupled with a fast database like Redis or MongoDB for quick lookups. It provides a clean REST API for creating and managing links, making it easy to integrate with other applications.



---
## ## ⭐ Core Features

* **Shorten URLs**: Generate a unique, random short code for any valid long URL.
* **Fast Redirection**: Near-instant lookups and HTTP 301 redirects for a seamless user experience.
* **Click Tracking**: Automatically counts and stores the number of visits for each shortened link.
* **Custom Aliases**: (Optional) Users can propose their own custom short links for branding.
* **Simple REST API**: A clean and well-documented API for programmatic use.

---
## ## 🛠️ Technology Stack

| Category | Technology |
| :--- | :--- |
| **Backend** | [![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)](https://nodejs.org/) [![Express.js](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)](https://expressjs.com/) |
| **Database** | [![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)](https://redis.io/) or [![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)](https://www.mongodb.com/) |
| **Short ID Generation** | **nanoid** - A tiny, secure, URL-friendly unique string ID generator. |
| **Frontend** | HTML5, CSS3, Vanilla JavaScript |

---
## ## 🔌 API Endpoints

The service exposes the following RESTful endpoints:

### ### 1. Shorten a URL

Creates a new short link.

* **Endpoint**: `POST /api/shorten`
* **Body** (JSON):
    ```json
    {
      "longUrl": "[https://www.very-long-and-complex-url.com/with/many/path/segments](https://www.very-long-and-complex-url.com/with/many/path/segments)"
    }
    ```
* **Success Response** (201 Created):
    ```json
    {
      "shortUrl": "[http://your-domain.com/aBc12D](http://your-domain.com/aBc12D)",
      "longUrl": "[https://www.very-long-and-complex-url.com/with/many/path/segments](https://www.very-long-and-complex-url.com/with/many/path/segments)"
    }
    ```

### ### 2. Redirect to Original URL

Redirects the user to the original long URL.

* **Endpoint**: `GET /:shortCode`
* **Example**: Visiting `http://your-domain.com/aBc12D`
* **Response**: `HTTP 301 Moved Permanently` with `Location` header set to the original long URL.

### ### 3. Get Link Statistics

Retrieves the click count for a specific short link.

* **Endpoint**: `GET /api/stats/:shortCode`
* **Example**: `GET /api/stats/aBc12D`
* **Success Response** (200 OK):
    ```json
    {
      "shortCode": "aBc12D",
      "longUrl": "[https://www.very-long-and-complex-url.com/](https://www.very-long-and-complex-url.com/)...",
      "clicks": 42
    }
    ```

---
## ## 🚀 Getting Started

To get a local copy up and running, follow these steps.

### ### ✅ Prerequisites

* **Node.js** (v18.x or later)
* **npm** & **Git**
* **Redis** or **MongoDB**: A running instance of your chosen database.

### ### ⚙️ Installation & Setup

1.  **Clone the repository**:
    ```sh
    git clone [https://github.com/Brajesh31/Url-shortening-.git](https://github.com/Brajesh31/Url-shortening-.git)
    ```
2.  **Navigate to the project directory**:
    ```sh
    cd Url-shortening-
    ```
3.  **Install dependencies**:
    ```sh
    npm install
    ```
4.  **Set up environment variables**:
    * Create a `.env` file in the root directory.
    * Add the necessary configuration variables listed below.
5.  **Start the server**:
    ```sh
    npm start
    ```

### ### 🔑 Environment Variables

Create a `.env` file in the root directory and add the following:
The base URL for your short links (e.g., http://localhost:5000)
BASE_URL="Your_Base_URL"

Your MongoDB connection string OR Redis connection details
MONGO_URI="Your_MongoDB_Connection_String"

REDIS_HOST="localhost"
REDIS_PORT=6379
The port for the server to run on
PORT=5000


---
## ## 📜 License

Distributed under the MIT License. See `LICENSE` file for more information.

---
## ## 📬 Contact

Brajesh - [@Brajesh31 on GitHub](https://github.com/Brajesh31)

Last updated: 2026-10-30 21:12 UTC
