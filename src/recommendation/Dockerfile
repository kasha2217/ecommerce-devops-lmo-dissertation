FROM python:3.11-slim-bookworm AS base
WORKDIR /usr/src/app

# Copy requirements
COPY requirements.txt ./

# Install dependencies
RUN pip install --no-cache-dir --upgrade pip && \
    pip install --no-cache-dir -r requirements.txt

# Copy application code
COPY . .

# Set environment variable
ENV RECOMMENDATION_PORT=1010

# Run the application
ENTRYPOINT ["python", "recommendation_server.py"]
