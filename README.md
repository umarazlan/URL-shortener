# URL Shortener

A simple, efficient URL shortener built with Node.js (native modules) and Vanilla JavaScript. This project demonstrates how to build a functional web application without relying on heavy frameworks or external dependencies for the backend.

## Features

-   **Shorten URLs**: Convert long URLs into compact, shareable links.
-   **Custom Short Codes**: Option to provide a custom alias for your URL.
-   **Random Generation**: Automatically generates a 4-byte hex code if no custom alias is provided.
-   **Persistent Storage**: Links are saved to a local JSON file (`data/links.json`), ensuring data persists across server restarts.
-   **Clipboard Integration**: One-click button to copy the shortened URL to your clipboard.
-   **Responsive Design**: Clean and responsive UI built with Vanilla CSS.

## Technologies Used

-   **Backend**: Node.js (http, fs, path, crypto modules)
-   **Frontend**: HTML5, CSS3, Vanilla JavaScript
-   **Data Storage**: JSON file system

## Prerequisites

-   [Node.js](https://nodejs.org/) (v14 or higher recommended)

## Installation

1.  **Clone the repository** (or download the source code):
    ```bash
    git clone <repository-url>
    cd URL_HTML_TAILWIND_NODE
    ```

2.  **Navigate to the project directory**:
    Ensure you are in the root folder where `App.js` is located.

## Usage

1.  **Start the server**:
    ```bash
    node App.js
    ```

2.  **Access the application**:
    Open your web browser and navigate to:
    `http://localhost:`

3.  **Shorten a URL**:
    -   Enter a long URL in the "Enter URL" field.
    -   (Optional) Enter a custom alias in the "Enter Short Code" field.
    -   Click "Shorten URL".

4.  **Use the Short Link**:
    -   The new link will appear in the "SHORTENED URLS" list.
    -   Click the link to be redirected to the original URL.
    -   Click the copy icon to copy the link to your clipboard.

## API Endpoints

The application exposes a few simple endpoints:

-   `GET /`: Serves the main HTML page.
-   `GET /style.css`: Serves the CSS file.
-   `GET /links`: Returns the list of all shortened URLs in JSON format.
-   `POST /shorten`: Accepts a JSON body `{ "url": "...", "shortCode": "..." }` to create a new short link.
-   `GET /:shortCode`: Redirects to the original URL associated with the short code.

## Project Structure

```
URL_HTML_TAILWIND_NODE/
├── App.js              # Main server entry point
├── data/
│   └── links.json      # JSON file for storing links
└── public/
    ├── index.html      # Frontend HTML
    └── style.css       # Frontend CSS
```

