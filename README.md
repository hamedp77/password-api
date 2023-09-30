# Password Generator API

This is a simple REST API project using the Python framework Flask. The password generator is using my other project, which you can find it [here](https://github.com/hamedp77/password-generator.git).

## Running the project

You have 2 options to run this project in your own environment:

1. Docker (Recommended)
2. Python

### Docker

1. Make sure you have docker installed on your machine. Use [this guide](https://docs.docker.com/engine/install/) to get started.

2. Clone the repository:

   ```shell
   git clone https://github.com/hamedp77/password-api.git
   ```

3. Make sure you're in the root directory of the project:

   ```shell
   cd password-api
   ```

4. Build the docker image and tag it:

   ```shell
   docker build . -t password-api
   ```

5. Run the container and publish port `80` of the container to an open port on your local machine, e.g., port `5000`:

   ```shell
   docker run -p 5000:80 password-api
   ```

6. Open `http://localhost:5000` to make sure everything is running.

### Python

1. Make sure you have Python installed on your machine. You can download and install the latest version of Python from [here](https://www.python.org/downloads/).

2. Clone the repository:

   ```shell
   git clone https://github.com/hamedp77/password-api.git
   ```

3. Make sure you're in the root directory of the project:

   ```shell
   cd password-api
   ```

4. Install dependencies:

   ```shell
   pip install -r requirements.txt
   ```

5. To run in a "development" environment you can use:

   ```shell
   flask --app api run
   ```

   or

   ```shell
   python api.py
   ```

   These commands will run the application on `http://localhost:5000` with debug mode disabled by default. The easiest way to enable debug mode is to set the `FLASK_DEBUG` environment variable to `true`.

    **Note:** Using a WSGI server like [gunicorn](https://gunicorn.org/) is the preferred way of running this in a "production" environment. If you have been following along with these steps, you have gunicorn already installed. All you have to do is run this command:

   ```shell
   gunicorn -b 0.0.0.0:80 api:app
   ```

   This will expose the API on all the available network interfaces of your machine on port `80`.

## Using the API

If you visit the URL of your deployed application, you'll be automatically redirected to the documentation page of the API, which is a Swagger UI. Here you can see all the details of each endpoint, how you can send requests to them, and the expected responses. You can also try each endpoint using the "try it out" button in your browser.
