# Feedback App

The Feedback App is a basic example of a containerized Node.js application that utilizes volumes with Docker. The purpose of this project is to demonstrate a simple webpage with a feedback form. When a user submits the form, the application creates a file in the "/feedback" path. If you want to view your feedback, you can access it using a specific URL structure.

## Docker Setup

To use the Feedback App with Docker, follow these steps:

1. Clone the repository:
git clone https://github.com/victorisena/feedback-app.git

2. Navigate to the project directory:
cd feedback-app

3. Build the Docker image:
docker build -t feedback-node:volumes .

## Running the Application

To run the Feedback App using Docker, execute the following command:

docker run -d -p 3000:3000 --rm --name feedback-app -v feedback:/app/feedback feedback-node:volumes

This command starts a Docker container based on the `feedback-node:volumes` image. It maps the container's port 3000 to the host's port 3000, allowing you to access the application at `localhost:3000`. The volume `feedback` is created and mounted to the `/app/feedback` directory inside the container, ensuring that the feedback files are persisted.

## Accessing Feedback

To access the feedback you submitted, use the following URL format: `localhost:3000/feedback/<filename>.txt`. Replace `<filename>` with the name you provided in the feedback form.

## Stopping the Application

To stop the Feedback App Docker container, run the following command:

docker stop feedback-app

## Contact

If you have any questions or feedback regarding the Feedback App, feel free to reach out to me:

* Email: victorigorsena@gmail.com
* LinkedIn: [linkedin.com/in/victor-igor-sena](https://www.linkedin.com/in/victor-igor-sena/)
* Twitter: [@victorisena](https://twitter.com/victorisena)