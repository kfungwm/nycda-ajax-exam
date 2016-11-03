Instructions:

- Add your answers inline to the markdown file.
- Use your own words.
- Come up with an answer from memory. Write it down, even if the answer is "I don't know."
- Then, we will go over the answers in class. Write down your revised answer below your original answer.
- There are two intermissions. We will go over the answers to the previous parts during those times.
- Finally, submit all of your answers in a file to canvas. This is so Lloyd and I can get a sense of your understanding.

---
### Part 1: Servers - 20 minutes

1. What is a server? What does a server do?

2. What is Node.js?

3. What is express?

4. What is a client? What does a client do?

5. How do the server and the client communicate?

6. Debugging:
- 6a. How do you view server logs?
- 6b. How do you view client logs?

---
### Part 2: HTTP Requests - 15 minutes

1. What is an HTTP Request?

2. GET Requests
- 2a. What is a GET request?
- 2b. When do you use GET requests?
- 2c. How do you send data in a GET request?

3. POST Requests
- 3a. What is a POST request?
- 3b. When do you use POST requests?
- 3c. How do you send data in a POST request?

---

### Intermission

---
### Part 3: Ajax - 15 minutes

1. Ajax
- 1a. What is Ajax?
- 1b. When should you use Ajax?

2. Given the following code snippet:

```js
console.log("A");
$('#map').click(function(event) {
	console.log("B");
	var coordinates = convertMouseCoordinatesToGeoCoordinates(event);

	console.log("C");
	$.get('/map', { lat: coordinates.x, lon: coordinates.y }, function(response, status) {
		console.log("D");
		mapDisplay.update(response);
	});

	console.log("E");
});
console.log("F");
```

- 2a. Describe what seems to be happening.
- 2b. In what order is `A` through `F` printed?
- 2c. Describe the events that happen between each letter. When does the server get hit?

---

### Intermission

---
### Part 4: Jade - 20 minutes

1. Jade
- 1a. What is Jade?
- 1b. Why should we use Jade?

2. Explain the difference between 'server side' JavaScript and 'client side' JavaScript.

3. Given this example `index.jade` file:

```js
doctype html
html
	head
		script(src='boop.js')
		script.
			var x = 1;
	body
		- var y = 2;
		h2= z + y
```

- 3a. Is `x` executed server side or client side? Does the client ever see `x`?
- 3b. Is `y` executed server side or client side? Does the client ever see `y`?
- 3c. Is `z` executed server side or client side? Does the client ever see `z`?
- 3d. When is `boop.js` executed? Does the client ever see `boop.js`?

---
### Part 5: Request Lifecycle - 15 minutes

5. Given the following code snippet in an express application:

```js
app.get('/home', function (request, response) {
	response.render('index', { z: 3 } );
});
```

- 5a. List the complete order of events, starting from the browser making a `GET` request to `/home`. Assume that `index` refers to the Jade file in Part 4. Be sure to describe when each JavaScript statement (`x`, `y`, `z`, and `boop.js`) gets executed.
- 5b. What is displayed on the page?
- 5c. What is visible from 'view page source'?
