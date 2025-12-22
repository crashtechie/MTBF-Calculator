# Use official Jupyter Lab base image
FROM jupyter/base-notebook:latest

# Set working directory
WORKDIR /home/jovyan/work

# Copy requirements file
COPY requirements.txt /tmp/requirements.txt

# Install Python packages from requirements.txt
RUN pip install --no-cache-dir -r /tmp/requirements.txt

# Expose Jupyter Lab port
EXPOSE ${JUPYTER_PORT:-8888}

# Start Jupyter Lab with environment variables
CMD jupyter lab \
    --ip=0.0.0.0 \
    --port=${JUPYTER_PORT:-8888} \
    --no-browser \
    --allow-root \
    --NotebookApp.token="${JUPYTER_TOKEN}" \
    --NotebookApp.password="${JUPYTER_PASSWORD}"
