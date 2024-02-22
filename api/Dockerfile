# Parent Image: Pull the node image from Docker hub
FROM node:17-alpine

# The Working Directory represents the main folder of the image
WORKDIR /app

# Copy all the files from source folder to destination folder
  # COPY <SOURCE_FOLDER_PATH> <DESTINATION_FOLDER_PATH>
  # First Dot (.) represents the root folder -- since all our files are in root folder
  # Second Dot (.) represents the root folder of the image
    # If WORKDIR specified --> it represents WORKDIR path
COPY . .

# Commands that run at the build time -- as the image gets built
# In general these commands will run inside the root directory of the image
  # If we don't specify the WORKDIR, then commands will run in the root directory of the image
  # If we specify the WORKDIR, then commands will run in the WORKDIR path
  # In our case 'yarn install' will run in '/app' directory
RUN yarn install

# Define the network ports that this container will listen on at runtime
EXPOSE 4000

# Commands that run inside the container. It's an array of strings.
CMD ["node", 'app.js']
