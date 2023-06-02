Flight API Server
=================

This is a flight API server that fetches flight data from a remote REST API and sends it as JSON data in response to requests to the `/flights` endpoint. The server uses Express to set up an HTTP server, axios to fetch data from the API, and dotenv to load environment variables. CORS middleware is also used to allow cross-origin requests.

Getting Started
---------------

To run the server, follow these steps:

1. Clone this repository using `git clone`.
2. Install the dependencies by running `npm install`.
3. Create a `.env` file in the root directory and set the following environment variables:

    ```
    URL=<flight API URL>
    TOKEN=<API access token>
    ```

    Replace `<flight API URL>` with the URL of the flight API that you want to fetch data from, and `<API access token>` with the access token for the API.

    For example:

    ```
    URL=https://api.example.com/flights
    TOKEN=abc123
    ```

4. Start the server by running `npm start`.
5. Send a GET request to [http://localhost:8000/flights](http://localhost:8000/flights) to fetch the flight data.

API Endpoints
-------------

### /flights

This endpoint returns a JSON array of flight data.

Supported Query Parameters:

- `page-size` (optional): the number of flights to return per page. Default is 10.

License
-------

This code is licensed under the MIT License.
