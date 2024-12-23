# Image to Video Converter App
### Click here
[Image to Video Converter App](https://project-amigos.onrender.com/)

## Overview

This Image to Video Converter app is a web application built using Flask. It allows users to upload images, convert them into a video, and add audio to the video. The app also supports user authentication, storing images in a database, and retrieving audio files from the database.

## Features

### User Authentication

- **Signup**
  - Route: `/signup`
  - Allows users to create an account by providing a username, email, fullname, and password. The password is hashed using bcrypt before storing it in the database.

- **Login**
  - Route: `/login`
  - Allows users to log in by providing their username and password. A JWT token is generated upon successful login and stored in the session.

### Image Upload and Storage

- **Upload Images**
  - Route: `/upload_files`
  - Allows users to upload multiple images. The images are saved to the server and stored in the database.

- **Upload Selected Images**
  - Route: `/upload_seleted_files`
  - Allows users to upload selected images. The images are saved to the server and stored in the database.

### Image Retrieval

- **Retrieve Images**
  - Route: `/user_profile/<username>`
  - Retrieves all images uploaded by the user and displays them on the user's profile page.

- **Retrieve Selected Images**
  - Route: `/selectedImages`
  - Retrieves all selected images uploaded by the user and returns them as a JSON response.

### Video Creation

- **Create Video**
  - Function: `create_video`
  - Converts the uploaded images into a video. The video is saved to the server.

- **Add Audio to Video**
  - Route: `/get_audio_path`
  - Adds audio to the created video and saves the merged video to the server.

### Audio Retrieval

- **Retrieve Audio Files**
  - Function: `retrieve_audio_files`
  - Retrieves audio files from the database and saves them to the server.

### User Profile

- **User Profile**
  - Route: `/user_profile/<username>`
  - Displays the user's profile with all uploaded images.

### Logout and Cleanup

- **Logout and Delete**
  - Route: `/logout_and_delete`
  - Logs out the user and deletes the selected images and merged video from the server.

## Implementation Details

### Database Configuration

- **Database Connection**
  - Function: `db_config`
  - Sets up the database connection using the provided credentials and certificate.

- **Close Connection**
  - Function: `close_connection`
  - Closes the database connection.

### JWT Token Management

- **Generate Token**
  - Function: `generate_token`
  - Generates a JWT token for the user.

- **Verify Token**
  - Function: `verify_token`
  - Verifies the JWT token.

### Flask Routes

- **Index**
  - Route: `/`
  - Renders the index page.

- **Signup**
  - Route: `/signup`
  - Handles user signup.

- **Login**
  - Route: `/login`
  - Handles user login.

- **User Profile**
  - Route: `/user_profile/<username>`
  - Displays the user's profile.

- **Upload Files**
  - Route: `/upload_files`
  - Handles image uploads.

- **Upload Selected Files**
  - Route: `/upload_seleted_files`
  - Handles selected image uploads.

- **Retrieve Selected Images**
  - Route: `/selectedImages`
  - Retrieves selected images.

- **Create Video**
  - Route: `/video`
  - Creates a video from the uploaded images.

- **Add Audio to Video**
  - Route: `/get_audio_path`
  - Adds audio to the created video.

- **Logout and Delete**
  - Route: `/logout_and_delete`
  - Logs out the user and deletes selected images and merged video.

## Deployment

This app has been deployed on Render. You can access it using the following link:
[Image to Video Converter App](https://project-amigos.onrender.com/)

## Academic Project

This application is part of an academic group project. It was developed by a team of students to demonstrate the integration of various technologies such as Flask, MySQL, JWT, and video processing libraries.

## Usage

To use this app, follow these steps:

1. **Install Dependencies**: Install the required dependencies using `pip install -r requirements.txt`.
2. **Set Up Database**: Configure the database connection in the `db_config` function.
3. **Run the App**: Start the Flask app using `python app.py`.
4. **Access the App**: Open a web browser and navigate to `http://localhost:5007` to access the app.

## Conclusion

This Image to Video Converter app provides a comprehensive set of features for uploading images, converting them into a video, adding audio, and managing user authentication. It is designed to be a functional and user-friendly web application.
