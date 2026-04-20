
---

# jQuery Notes (Updated – Complete)

---

## 1. Introduction

**jQuery** is a JavaScript library that simplifies DOM manipulation, event handling, data access, and AJAX.

**Key Idea:**
Write less code to perform common JavaScript tasks.

---

## 2. Setup

### Method 1: CDN (Recommended)

```html
<script src="https://code.jquery.com/jquery-3.7.1.min.js"></script>
```

---

### Method 2: Local File

1. Download jQuery from official site
2. Include in project:

```html
<script src="jquery.min.js"></script>
```

---

## 3. Basic Syntax

```js
$(selector).action();
```

* `$` → jQuery object
* `selector` → selects HTML element
* `action()` → operation

---

## 4. Document Ready

```js
$(document).ready(function() {
    // code here
});
```

Ensures DOM is fully loaded before execution.

---

## 5. Selectors

```js
$("#id")        // ID selector
$(".class")     // Class selector
$("p")          // Element selector
```

---

# 6. Reading Data (IMPORTANT)

## Read Input Value

```html
<input type="text" id="name">
```

```js
let value = $("#name").val();
console.log(value);
```

---

## Read Text Content

```html
<p id="text">Hello</p>
```

```js
let text = $("#text").text();
console.log(text);
```

---

## Read HTML Content

```js
let html = $("#text").html();
```

---

## Read Attribute

```html
<img id="img" src="image.png">
```

```js
let src = $("#img").attr("src");
```

---

# 7. Writing / Updating Data

## Set Input Value

```js
$("#name").val("John");
```

---

## Set Text

```js
$("#text").text("New Text");
```

---

## Set HTML

```js
$("#text").html("<b>Bold Text</b>");
```

---

## Set Attribute

```js
$("#img").attr("src", "new.png");
```

---

## Set CSS

```js
$("#box").css("color", "red");
```

---

# 8. Events

```js
$("#btn").click(function() {
    alert("Clicked");
});
```

---

# 9. Show / Hide

```js
$("#box").hide();
$("#box").show();
$("#box").toggle();
```

---

# 10. Effects

```js
$("#box").fadeOut();
$("#box").fadeIn();

$("#box").slideUp();
$("#box").slideDown();
```

---

# 11. Method Chaining

```js
$("#box")
    .text("Hello")
    .css("color", "red")
    .slideUp()
    .slideDown();
```

---

# 12. Example: Read + Write (Form Demo)

## HTML

```html
<input type="text" id="name" placeholder="Enter name">
<button id="btn">Submit</button>
<p id="output"></p>
```

---

## jQuery

```js
$("#btn").click(function() {

    // Read value
    let name = $("#name").val();

    // Write value
    $("#output").text("Hello " + name);

});
```

---

# 13. Example: Attribute Read + Update

```html
<img id="img" src="old.png">
<button id="change">Change Image</button>
```

```js
$("#change").click(function() {

    let current = $("#img").attr("src"); // read

    console.log(current);

    $("#img").attr("src", "new.png"); // update

});
```

---

