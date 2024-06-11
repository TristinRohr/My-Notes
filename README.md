# My-Note-Taker

## Description

Note Taker is a web application that allows users to write, save, and delete notes. This application uses an Express.js back end and saves and retrieves note data from a JSON file. It is designed to help users organize their thoughts and keep track of tasks.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Screenshots](#screenshots)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)

## Installation

To install and run this application locally, follow these steps:

1. **Clone the repository:**
   ```sh
   git clone https://github.com/TristinRohr/My-Notes
   cd note-taker
   ```
2. **Install dependencies:**
   ```sh
   npm install
   ```
3. **Run the application:**
   ```sh
   npm start
   ```
   The application will be available at `http://localhost:3000`.

## Usage

1. **Open the application:** Navigate to `http://localhost:3000` in your web browser.
2. **Create a new note:** Click the "New Note" button, enter a title and the note content, then click the "Save" button.
3. **View existing notes:** Click on any note in the left-hand column to view its content.
4. **Delete a note:** Click the trash icon next to a note in the left-hand column to delete it.

## API Endpoints

### GET /api/notes

- **Description:** Retrieves all saved notes.
- **Response:** JSON array of note objects.

### POST /api/notes

- **Description:** Adds a new note.
- **Request Body:**
  ```json
  {
    "title": "Note Title",
    "text": "Note text"
  }
  ```
- **Response:** The saved note object with a unique ID.

### DELETE /api/notes/:id

- **Description:** Deletes the note with the specified ID.
- **Response:** JSON object indicating success.

## Screenshots

![Home Page](screenshots/home.png)
*Home page of the Note Taker application.*

![Notes Page](screenshots/notes.png)
*Notes page where users can add, view, and delete notes.*

## Deployment

This application is deployed on [Render](https://render.com). You can access the live application at [https://my-notes-04aq.onrender.com](https://my-notes-04aq.onrender.com).

### Deploying to Render

1. **Create a `render.yaml` file** in the root directory:
   ```yaml
   services:
     - type: web
       name: note-taker
       env: node
       buildCommand: 'npm install'
       startCommand: 'node server.js'
   ```

2. **Push your project to a Git repository**.

3. **Deploy the project**:
   - Go to Render’s dashboard.
   - Create a new web service.
   - Connect it to your GitHub repository.
   - Render will use the `render.yaml` to set up the deployment.

## Contributing

Contributions are welcome! Please follow these steps to contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add new feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
```