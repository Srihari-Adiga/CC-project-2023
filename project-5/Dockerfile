# use the `mongo` image
# copy the app directory and any files needed for your implementation from your local to the container
# equip it with all the packages and installs needed to run the flask app (packages are defined in app/requirements.txt. `pip install -r app/requirements.txt`)
# expose the port flask app will run on

# Use the mongo image as a base
FROM mongo

# Set the working directory to /app
WORKDIR /app

# Copy the app directory and any files needed for your implementation
COPY app/ /app/

# Install any packages needed to run the Flask app
RUN apt-get update && \
    apt-get install -y python3-pip && \
    pip3 install --upgrade pip && \
    pip3 install -r /app/requirements.txt

# Expose the port that the Flask app will run on
EXPOSE 5000

# Set the command to start the Flask app
CMD ["python3", "/app/app.py"]