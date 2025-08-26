FROM python:3.10

WORKDIR /backend
# Copy the requirements file into the container
COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

# Copy the FastAPI application code into the container
COPY ./ ./

# Expose the port that FastAPI will run on
EXPOSE 8000

# Command that will execute the FastAPI application when container starts
CMD ["fastapi", "run", "--workers", "4", "main.py"]