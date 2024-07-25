### Live Greeting Web App

A web application that displays and updates the current time. This project is easily containerized using the included Dockerfile.

## Containerizing the Application

To containerize this application, follow these steps:

1. **Build the Docker image**: Run the following command in the directory that contains the Dockerfile. Replace `my-node-app` with the name you want to give to your Docker image.

    ```bash
    docker build -t my-node-app .
    ```

2. **Run the Docker image**: After building the image, you can run it with the following command. Replace `your-image-name` with the name you gave to your Docker image.

    ```bash
    docker run -p 3000:3000 my-node-app
    ```

    This command runs the Docker image and maps port 3000 inside the Docker container to port 3000 on your local machine. Adjust the port numbers as necessary based on your application's configuration.

3. **Access the application**: You can now access the application in your web browser at `http://localhost:3000`.

Remember to replace `my-node-app` with the name you gave to your Docker image.



## Docker Image

The Docker image for this application is available on Docker Hub. You can access it [here](https://hub.docker.com/r/seanbryson/my-node-app).



## [Optional] Installing Node Modules

It's not necassry to install node modules prior to containerizing the application. With that in mind, here are the steps to run the project locally without Docker:

1. **Navigate to your project directory**: Open a terminal and navigate to the directory of your project where your `package.json` file is located.

2. **Install the modules**: Run the following command to install the modules:

    ```bash
    npm install
    ```

    This command reads the `package.json` file in your project directory and installs all the modules listed under `dependencies` and `devDependencies`. The installed modules will be placed in a folder named `node_modules` in your project directory.

Remember, you need to have Node.js and npm installed on your machine to run this command. If they're not installed, you can download Node.js (which includes npm) from the [official website](https://nodejs.org/).

3. **Start the application**: Run the following command in your terminal:

    ```bash
    npm start
    ```

    This command starts the application. You should see output in your terminal indicating that the application is running.

4. **Access the application**: Open your web browser and navigate to the URL where your application is running (`http://localhost:3000`).
