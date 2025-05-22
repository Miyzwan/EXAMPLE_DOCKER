# c-project

This project contains a simple C program that prints "Hello world" and the numbers from 1 to 3. It is packaged using Docker for easy deployment.

## Project Structure

```
c-project
├── src
│   └── app.c
├── Dockerfile
└── README.md
```

## Building the Docker Image

To build the Docker image for this project, navigate to the project directory and run the following command:

```
docker build -t c-project .
```

## Running the Docker Container

After building the image, you can run the Docker container using the following command:

```
docker run --rm c-project
```

This will execute the compiled C program, which will output "Hello world" followed by the numbers 1 to 3.

## Requirements

- Docker must be installed on your machine.
- Basic knowledge of Docker commands is helpful.

## License

This project is licensed under the MIT License.