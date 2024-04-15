# The docker system will use the Python 3.12-slim instance of Python
FROM python:3.12-slim

ENV APP_DIR /application

# We outline the core directory of our application to be the ENV variable set above
WORKDIR ${APP_DIR}

# Copy the other files into the working directory of the container
COPY requirements.txt .

# Outline the dependencies within the container
RUN pip install -r requirements.txt

COPY . .

# Label the port where the app executes within the container
EXPOSE 5000

# Execute the app within the container
ENTRYPOINT [ "python", "main.py" ]