
---

# AJAX vs XML vs JSON – Quick Revision Sheet

---

## 1. Basic Overview

| Concept  | Description                                              |
| -------- | -------------------------------------------------------- |
| **AJAX** | Technique to communicate with server without page reload |
| **XML**  | Data format used to store and transport structured data  |
| JSON     | Lightweight data format used in modern APIs              |

---

## 2. Purpose

| Concept | Purpose                             |
| ------- | ----------------------------------- |
| AJAX    | Send/receive data asynchronously    |
| XML     | Store and transport structured data |
| JSON    | Store and exchange data efficiently |

---

## 3. Role in Web Development

| Concept | Role                                               |
| ------- | -------------------------------------------------- |
| AJAX    | Handles communication between frontend and backend |
| XML     | Early data format used in AJAX                     |
| JSON    | Modern data format used with AJAX                  |

---

## 4. Syntax Comparison

### XML Example

```xml id="cmp1"
<user>
    <name>John</name>
    <age>21</age>
</user>
```

---

### JSON Example

```json id="cmp2"
{
    "name": "John",
    "age": 21
}
```

---

## 5. Key Differences (XML vs JSON)

| Feature     | XML             | JSON            |
| ----------- | --------------- | --------------- |
| Format Type | Markup language | Data format     |
| Syntax      | Tag-based       | Key-value pairs |
| Readability | Less readable   | More readable   |
| Size        | Larger          | Smaller         |
| Parsing     | Complex         | Easy            |
| Speed       | Slower          | Faster          |

---

## 6. AJAX Data Flow

### With XML (Old)

```text id="cmp3"
User Action → AJAX Request → Server → XML Response → Parse XML → Update UI
```

---

### With JSON (Modern)

```text id="cmp4"
User Action → AJAX Request → Server → JSON Response → Direct Use → Update UI
```

---

## 7. Code Comparison

### AJAX with XML (Old)

```js id="cmp5"
var xhr = new XMLHttpRequest();

xhr.open("GET", "data.xml", true);

xhr.onload = function() {
    var xml = xhr.responseXML;
    var name = xml.getElementsByTagName("name")[0].childNodes[0].nodeValue;
    console.log(name);
};

xhr.send();
```

---

### AJAX with JSON (Modern)

```js id="cmp6"
fetch("data.json")
    .then(res => res.json())
    .then(data => {
        console.log(data.name);
    });
```

---

## 8. Advantages Summary

| Concept | Advantages                         |
| ------- | ---------------------------------- |
| AJAX    | No page reload, faster interaction |
| XML     | Structured, extensible             |
| JSON    | Lightweight, easy to use, fast     |

---

## 9. Current Usage

| Concept | Usage Today                    |
| ------- | ------------------------------ |
| AJAX    | Widely used (core concept)     |
| XML     | Limited (legacy systems, SOAP) |
| JSON    | Standard for modern APIs       |

---

## 10. Final Understanding

* AJAX is a **technique**
* XML and JSON are **data formats**
* Modern web apps use:

  * AJAX + JSON
* XML is mostly replaced due to complexity

---

## 11. One-Line Summary

> AJAX handles communication, while XML and JSON define how data is structured and transferred.

---

