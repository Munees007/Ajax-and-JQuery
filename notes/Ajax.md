
---

# AJAX Notes (Complete)

---

## 1. Introduction

**AJAX**

**Full Form:**
**A**synchronous **J**avaScript **A**nd **X**ML

---

## 2. What is AJAX?

AJAX is a technique used to send and receive data from a server **without reloading the web page**.

### Key Idea

* Communicates with server in the background
* Updates only required parts of the page
* Improves performance and user experience

---

## 3. Traditional vs AJAX Approach

### Without AJAX (Form Submission)

* Request sent to server
* Entire page reloads
* New page is loaded with response

### With AJAX

* Request sent in background
* No page reload
* Only specific part of page updates

---

## 4. What is an API?

**API (Application Programming Interface)** is a system that allows communication between **frontend and backend**.

### Simple Definition

> API is a bridge between client (browser) and server (database/backend)

---

## 5. How AJAX Works with API

1. User performs action (click, input)
2. JavaScript sends request (AJAX)
3. API receives request
4. Server processes data
5. API sends response (usually JSON)
6. UI updates dynamically

---

## 6. HTTP Methods (API Methods)

These define the type of operation performed on the server.

| Method | Purpose          | Example          |
| ------ | ---------------- | ---------------- |
| GET    | Read data        | Get user details |
| POST   | Send/Create data | Submit form      |
| PUT    | Update data      | Update profile   |
| DELETE | Remove data      | Delete record    |

---

## 7. AJAX using jQuery

```js id="cxtsbn"
$.ajax({
    url: "API_URL",
    method: "POST",
    contentType: "application/json",
    data: JSON.stringify({ key: value }),

    success: function(response) {
        console.log(response);
    },

    error: function() {
        console.log("Error");
    }
});
```

---

## 8. AJAX using Modern JavaScript (fetch)

```js id="7yxh2r"
async function loadData() {

    const res = await fetch("API_URL", {
        method: "POST",
        headers: {
            "Content-Type": "application/json"
        },
        body: JSON.stringify({ key: value })
    });

    const data = await res.json();
    console.log(data);
}
```

---

## 9. Data Format

* Most modern APIs use **JSON (JavaScript Object Notation)**

Example:

```json
{
    "name": "John",
    "age": 21
}
```

---

## 10. Advantages of AJAX

* No page reload
* Faster interaction
* Better user experience
* Partial page updates

---

## 11. Limitations

* Requires JavaScript enabled
* Debugging can be complex
* Depends on API availability

---

# API Creation (Roadmap – Beginner Friendly)

---

## Step 1: Choose Backend Technology

Common options:

* Node.js (Express)
* .NET
* Java (Spring Boot)
* Python (FastAPI)

---

## Step 2: Create Server

Example (Node.js):

```js id="py57nq"
const express = require("express");
const app = express();

app.use(express.json());
```

---

## Step 3: Define Route (Endpoint)

```js id="lplh1o"
app.post("/kural", (req, res) => {
    const num = req.body.num;

    res.json({
        message: "Received",
        number: num
    });
});
```

---

## Step 4: Run Server

```js id="7rte5k"
app.listen(3000, () => {
    console.log("Server running on port 3000");
});
```

---

## Step 5: Connect Frontend (AJAX / fetch)

Frontend sends request → API responds → UI updates

---

## Step 6: Add Database (Advanced)

* Store and retrieve real data
* Examples:

  * MySQL
  * PostgreSQL
  * MongoDB

---

## Step 7: Deploy API

* Host backend online
* Examples:

  * Vercel
  * Render
  * AWS

---
