
# Flask RGB Calculator

This project is a simple Flask web application that allows users to interactively adjust RGB sliders to see color changes in real-time. The application also provides HEX and RGB color codes for the selected color. It uses Docker to containerize the application for easy deployment.

## Project Structure

- `main.py`: The main Flask application file.
- `templates/`: Directory containing the HTML templates.
  - `index.html`: The main HTML file for the application.
- `Dockerfile`: Dockerfile to build the Docker image.
- `requirements.txt`: Python dependencies for the Flask application.
- `.dockerignore`: Docker ignore file to exclude unnecessary files from the Docker image.

## Prerequisites

To run this project, you need to have the following installed on your machine:

- Python 3.x
- Docker (for containerization)

## Setup

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/your-repository-name.git
cd your-repository-name
```

### 2. Install Python Dependencies

If you are running the application locally (not in a Docker container), create a virtual environment and install the required Python packages.

```bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
pip install -r requirements.txt
```

### 3. Build and Run the Docker Container

If you prefer to use Docker, follow these steps to build and run the Docker container.

#### Build the Docker Image

```bash
docker build -t flask-app .
```

#### Run the Docker Container

```bash
docker run -p 8080:8080 flask-app
```

This command maps port 8080 of the Docker container to port 8080 on your host machine.

### 4. Access the Application

Open a web browser and navigate to:

```
http://localhost:8080
```

You should see the RGB Calculator application running.

## Application Overview

- **Sliders**: Adjust the Red, Green, and Blue values using the sliders. The color preview box will update in real-time.
- **Color Picker**: Use the color picker to select a color, which will update the RGB sliders and color preview.
- **Color Codes**: The HEX and RGB codes of the selected color are displayed and can be copied using the provided buttons.

## Dockerfile

The Dockerfile is configured to:

1. Use the official Python 3.10 slim image.
2. Set the working directory to `/app`.
3. Install dependencies from `requirements.txt`.
4. Copy the application code into the Docker image.
5. Expose port 8080.
6. Set the `PORT` environment variable.
7. Run `main.py` when the container starts.

## Requirements

The `requirements.txt` file includes:

- Flask==2.3.0

You can add additional dependencies to this file as needed.

## .dockerignore

The `.dockerignore` file ensures that unnecessary files (e.g., Python bytecode files, Git files) are excluded from the Docker image.

## Troubleshooting

- **Port Issues**: Ensure that port 8080 is available on your machine and not used by other applications.
- **Dependency Errors**: Check the `requirements.txt` file for any missing dependencies or version conflicts.

## Contributing

If you want to contribute to this project, please fork the repository and create a pull request with your changes. Ensure that your code adheres to the project's coding standards and includes relevant tests.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Contact

For any questions or feedback, please reach out to:

- [LinkedIn Profile](https://www.linkedin.com/in/yashkavaiya/)
- [GitHub Profile](https://github.com/Yash-Kavaiya)

Thank you for using the Flask RGB Calculator!


### Explanation:
- **Project Structure:** Details the organization of the project files.
- **Prerequisites:** Lists the tools and software needed.
- **Setup:** Provides instructions for both local setup and Docker containerization.
- **Application Overview:** Describes the functionality of the web application.
- **Dockerfile:** Summarizes the purpose of the Dockerfile.
- **Requirements and .dockerignore:** Explains the role of these files.
- **Troubleshooting:** Offers common solutions to potential issues.
- **Contributing:** Guidelines for contributing to the project.
- **License and Contact:** Provides licensing information and contact details.
