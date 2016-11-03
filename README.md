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
		a server is a computerprogram that comminicate service to other computer programs in the same computer or other computers.
2. What is Node.js?
	node.js is a server platform that you can test all the JS codes in realtime.

3. What is express?
	express is program to make a server in memory

4. What is a client? What does a client do?
	Client is the user that want to request something and want to receive a response from the server

5. How do the server and the client communicate?
	For example via a browser to communicate.

6. Debugging:
- 6a. How do you view server logs?

- 6b. How do you view client logs?

---
### Part 2: HTTP Requests - 15 minutes

1. What is an HTTP Request?
the browser fetch a file from server and the user wants to request some file and the webserver will response back the file

2. GET Requests
- 2a. What is a GET request?
	get request is request to get data from the server

- 2b. When do you use GET requests?
		user wants to get data from the server

- 2c. How do you send data in a GET request?



3. POST Requests
- 3a. What is a POST request?
		Post request is a request for modifying data on the server

- 3b. When do you use POST requests?
		to modified data on the server

- 3c. How do you send data in a POST request?
	with a string?
---

### Intermission

---
### Part 3: Ajax - 15 minutes

1. Ajax
- 1a. What is Ajax?
	exchange data with the server and update part of the website without reloading the whole page

- 1b. When should you use Ajax?
	if you want dynamic content


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
	On the console it will print out "A"
	if someone clicked it will print int he console "B"




- 2b. In what order is `A` through `F` printed?
		A and F will print it out

- 2c. Describe the events that happen between each letter. When does the server get hit?
		If some one clicked the button, the function will print out B, C
		if the mapDislay is true it will print out the D  and the E


---

### Intermission

---
### Part 4: Jade - 20 minutes

1. Jade
- 1a. What is Jade?
		simplefied html

- 1b. Why should we use Jade?
	you don't need to make multipage pages to write it.

2. Explain the difference between 'server side' JavaScript and 'client side' JavaScript.
		frontend en backend javascript

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
		server side and they will not see the X

- 3b. Is `y` executed server side or client side? Does the client ever see `y`?
		client side but it will not show it.

- 3c. Is `z` executed server side or client side? Does the client ever see `z`?
		client side but it will show it.

- 3d. When is `boop.js` executed? Does the client ever see `boop.js`?
		on the head it will executed and the client will see it

---
### Part 5: Request Lifecycle - 15 minutes

5. Given the following code snippet in an express application:

```js
app.get('/home', function (request, response) {
	response.render('index', { z: 3 } );
});
```

- 5a. List the complete order of events, starting from the browser making a `GET` request to `/home`. Assume that `index` refers to the Jade file in Part 4. Be sure to describe when each JavaScript statement (`x`, `y`, `z`, and `boop.js`) gets executed.

	on the head it will executed the JS file

- 5b. What is displayed on the page?
	 it will display 5 (h2= z + y)

- 5c. What is visible from 'view page source'?
	it will display the code on the view page source
