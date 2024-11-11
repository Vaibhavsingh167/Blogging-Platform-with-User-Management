
# Blogging Platform with User Management

A Flask-based blogging platform that enables users to create accounts, publish posts, add comments, and manage their content. This platform includes user authentication, file uploads, commenting, and contact form capabilities.

## Features

- **User Authentication**: Secure registration, login, and logout functionality.
- **Multiple Authors**: Each user can create and manage their own blog posts.
- **Comments**: Users can comment on posts, fostering interaction.
- **File Uploads**: Support for image uploads for posts.
- **Contact Form**: Users can reach out via a contact form that sends an email notification.
- **Dashboard**: Logged-in users can view and manage their posts.
- **Image Support**: Allows image attachments for posts and displays them on the home page and individual post pages.

## Output-


## Setup Instructions

1. **Clone the Repository**

   ```bash
   git clone https://github.com/Vaibhavsingh167/Blogging-Platform-with-User-Management.git
   cd Blogging-Platform-with-User-Management
   ```

2. **Install Requirements**

   Ensure you have Python and pip installed. Then, install the required packages:

   ```bash
   pip install -r requirements.txt
   ```

3. **Set Up Environment Variables**

   Edit the `app.config` section in the code or set these environment variables in your environment:

   - `SECRET_KEY`: A secret key for Flask sessions.
   - `MAIL_SERVER`: Set to `smtp.gmail.com`.
   - `MAIL_PORT`: Set to `587`.
   - `MAIL_USE_TLS`: Set to `True`.
   - `MAIL_USERNAME`: Your Gmail address.
   - `MAIL_PASSWORD`: Your Gmail password or app-specific password.
   - `MAIL_DEFAULT_SENDER`: Same as `MAIL_USERNAME`.

4. **Initialize the Database**

   Create the SQLite database by running:

   ```bash
   python
   from app import db
   db.create_all()
   ```

5. **Run the Application**

   Start the application:

   ```bash
   python app.py
   ```

   Access it at `http://127.0.0.1:5000` in your browser.

## Usage

- **Homepage**: View all published posts.
- **Register/Login**: Create a new user account or log in.
- **Dashboard**: View and manage your posts.
- **Create Post**: Add a new post with optional image upload.
- **View Post**: See the full post and add comments if logged in.
- **Edit Post**: Update the title, content, or image of your posts.
- **Contact Form**: Send messages to the admin’s email via the contact form.

## Code Overview

### Key Files and Directories

- `app.py`: Main application code with routes, models, and logic.
- `templates/`: HTML templates for rendering pages.
- `static/uploads/`: Folder to store uploaded images.

### Models

- **User**: Handles user data and authentication.
- **Post**: Stores blog posts, including titles, content, author reference, and optional image path.
- **Comment**: Stores comments linked to posts and users.

### Key Routes

- **/register**: User registration page.
- **/login**: User login page.
- **/logout**: Logs out the current user.
- **/dashboard**: Displays user-specific posts.
- **/create**: Create a new post.
- **/post/<post_id>**: View and comment on a specific post.
- **/edit/<post_id>**: Edit an existing post.
- **/contact**: Handles contact form submissions.

### Helper Functions

- `allowed_file(filename)`: Checks if the uploaded file has an allowed extension.
- `save_image(file)`: Saves the uploaded image and returns the path.

## License

This project is open-source.
