# ChatWithYourData_Bot

A chatbot interface designed to interact with PDF documents. Through this bot, users can upload PDF documents and have intelligent conversations about their content.

## Dependencies

- **OpenAI**: Used for embeddings and conversational interfaces.
- **Panel & Param**: For creating interactive GUI components.
- **OS**: Accessing environment variables and system-specific settings.
- **Datetime**: Handling and formatting date-time information.
- **langchain**: A hypothetical library that seems to provide various utilities for language embeddings, text splitting, and more.

It's recommended to create a virtual environment to manage these dependencies.

## Dockerization

To containerize this application, you can use Docker. Here's a simple guide:

1. Create a `Dockerfile` in the root directory of the application:

```Dockerfile
FROM python:3.8

WORKDIR /app

COPY requirements.txt ./

RUN pip install --no-cache-dir -r requirements.txt

COPY . .

CMD ["python", "./your_script_name.py"]
```

2. Create a `requirements.txt` file in the root directory listing all your Python dependencies.

3. Build the Docker image:

```bash
docker build -t chatwithyourdata_bot:latest .
```

4. Run the Docker container:

```bash
docker run -e API_KEY=your_actual_api_key_here -p 1365:1365 
chatwithyourdata_bot
```

This will start the application inside a Docker container, accessible via `localhost:1365`.

## Usage

1. Set up the necessary environment, either manually or using Docker.
2. Ensure you have your OpenAI API key set as an environment variable named `API_KEY`.
3. Run the code to initialize a dashboard server.
4. Use the dashboard to upload a PDF document and start chatting with the bot about its content.
5. The bot will intelligently pull information from the uploaded PDF to answer queries.

