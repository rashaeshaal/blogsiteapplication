FROM python:3.10

# Set the working directory
WORKDIR /app

# Copy requirements.txt
COPY requirements.txt .

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of your application
COPY . .

# Command to run your application
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
