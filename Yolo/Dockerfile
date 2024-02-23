# Use an official Python runtime as a parent image
FROM python:3.12.2

# Set the working directory in the container
WORKDIR /usr/src/app

# Install OpenCV dependencies
RUN apt-get update && apt-get install -y libgl1-mesa-glx libglib2.0-0

# Upgrade pip
RUN pip install --upgrade pip

# Install Python dependencies
# Assuming you don't have a requirements.txt, we install directly
RUN pip install opencv-python-headless ultralytics

# Copy the Python script and any necessary files into the container
COPY test_1.py .
# If you have a YOLO model file you need to include, uncomment and adjust the following line
COPY yolov8x.pt .

# Command to run the script
CMD ["python", "./test_1.py"]
