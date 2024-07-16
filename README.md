## Flask Application Design

### HTML Files
- **base.html:** This file will serve as the base template for all other HTML files in the application. It should define the overall structure of the pages, including the header, footer, and navigation bar.

- **index.html:** This file will be the homepage of the application. It should display a form for users to enter a list of serial numbers and attachment names.

- **result.html:** This file will display the results of the query and the AI's response.

### Routes
- **@app.route('/', methods=['GET', 'POST'])**: This route will handle requests to the homepage. If the request is a GET request, it will render the index.html file. If it's a POST request, it will collect the serial numbers and attachment names from the form, query the data and send the data to AI, and pass the AI's prompt.

- **@app.route('/result', methods=['GET', 'POST'])**: This route will handle requests to the result page. If the request is a GET request, it will render the result.html file. If it's a POST request, it will collect the results from the query and display them on the page.

- **@app.route('/ai', methods=['POST'])**: This route will handle requests to the AI. It will collect the AI's prompt from the POST request and send it to the AI. The AI's response will then be returned to the client.