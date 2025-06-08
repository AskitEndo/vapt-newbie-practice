# ✅ Lab 02: Command-line Web Requests & Data Extraction using cURL

## 🎯 Objective

Understand how to perform HTTP GET and POST requests using `cURL` and explore basic API interactions from the terminal.

## 🛠 Tools Used

- cURL

## 🔄 Task Summary

- Perform HTTP GET and POST requests.
- Extract and interact with data from web servers or mock APIs.

## 🧪 Steps

### 🔹 Step 1: Perform a GET request

```bash
curl https://jsonplaceholder.typicode.com/posts/1
```

### 🔹 Step 2: Perform a POST request

```bash
curl -X POST https://jsonplaceholder.typicode.com/posts -d "title=lab&body=manual&userId=1"
```

### 🔹 Optional: Add headers to customize the request

```bash
curl -H "Content-Type: application/json" https://jsonplaceholder.typicode.com/posts
```

## 👀 Observations

- GET is used to fetch data; POST is used to send data.
- You can add headers, query parameters, and body data.
- Useful for API testing, scraping, and scripting.

## ✅ Expected Output

- For GET: JSON data of the requested resource (e.g., a blog post).
- For POST: JSON confirmation of the posted data.
