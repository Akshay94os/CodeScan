# CodeScan

![CodeScan Logo Placeholder](https://via.placeholder.com/150x50?text=CodeScan)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub last commit](https://img.shields.io/github/last-commit/Akshay94os/CodeScan)](https://github.com/Akshay94os/CodeScan/commits/main)

A simple, client-side web tool for basic code analysis, formatting, and minification. Paste your code, apply various operations, and get instant results directly in your browser.

## Overview

CodeScan is a lightweight, browser-based utility designed to help developers perform quick and basic operations on code snippets. It provides functionalities like code scanning (line/character count), formatting, minification, and beautification, primarily targeting JSON and JavaScript object structures. Built entirely with HTML, CSS, and vanilla JavaScript, it runs entirely in your browser without any server-side dependencies.

### Key Value Proposition

*   **Instant Feedback**: Process code snippets in real-time.
*   **Client-Side**: No data leaves your browser, ensuring privacy and speed.
*   **Simplicity**: A straightforward interface for common code manipulation tasks.
*   **No Installation**: Just open the `index.html` file in your browser.

### Target Audience

Developers, students, or anyone needing a quick tool for basic code formatting, minification, or simple analysis of JSON/JavaScript objects.

### Current Status

The project is in an early development stage, offering fundamental features. The formatting and minification capabilities are currently optimized for JSON and JavaScript object syntax.

## Features

CodeScan provides the following functionalities:

*   **Scan Code (Basic)**:
    *   Counts the number of lines and characters in the input code.
    *   *Status: Stable*
*   **Format Code**:
    *   Indents and pretty-prints JSON or JavaScript object strings.
    *   Utilizes `JSON.stringify` for structured output.
    *   *Status: Stable (optimized for JSON/JS objects)*
*   **Minify Code**:
    *   Removes whitespace and newlines from JSON or JavaScript object strings to reduce file size.
    *   Utilizes `JSON.stringify` for compact output.
    *   *Status: Stable (optimized for JSON/JS objects)*
*   **Beautify Code**:
    *   Currently, this function provides the same output as "Format Code" due to the project's current scope.
    *   Future enhancements may integrate dedicated beautification libraries for broader language support.
    *   *Status: Experimental (same as Format)*
*   **Clear All**:
    *   Resets both the input and output text areas.
    *   *Status: Stable*
*   **Error Handling**:
    *   Provides basic error messages for invalid input during formatting/minification.

## Tech Stack

*   **HTML5**: For structuring the web page content.
*   **CSS3**: For styling and layout.
*   **Vanilla JavaScript**: For all client-side logic and interactivity.

## Architecture

CodeScan is a single-page, client-side application.

*   **`index.html`**: Contains all the HTML structure, CSS styling, and JavaScript logic within a single file.
*   **User Interface**: Consists of two `textarea` elements (one for input, one for output) and a set of control buttons.
*   **Logic**: JavaScript functions directly manipulate the DOM to read input, perform operations, and display results. There are no external dependencies or server-side components.

```
.
├── README.md
└── index.html  (Contains all HTML, CSS, and JavaScript)
```

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

*   A modern web browser (e.g., Chrome, Firefox, Edge, Safari).

### Installation

No complex installation steps are required.

1.  **Clone the repository**:
    ```bash
    git clone https://github.com/Akshay94os/CodeScan.git
    cd CodeScan
    ```
2.  **Open in browser**:
    Locate the `index.html` file in the cloned directory and open it with your preferred web browser. You can usually do this by double-clicking the file.

    Alternatively, if you have a local web server (like `http-server` via npm or Python's `SimpleHTTPServer`), you can serve the directory:
    ```bash
    # Using http-server (if you have Node.js installed)
    npx http-server .

    # Using Python 3
    python -m http.server
    ```
    Then navigate to `http://localhost:8080` (or the port indicated by your server).

### Configuration

CodeScan is a client-side application and does not require any specific configuration files or environment variables. All settings are hardcoded within the `index.html` file.

## Usage

1.  **Open CodeScan**: Open the `index.html` file in your web browser.
2.  **Paste Code**: Paste your code snippet into the left-hand "Input Code" text area.
3.  **Select Operation**: Click one of the control buttons in the middle:
    *   `Scan Code`: To get basic statistics.
    *   `Format Code`: To pretty-print JSON/JS objects.
    *   `Minify Code`: To compress JSON/JS objects.
    *   `Beautify Code`: (Currently same as Format Code).
    *   `Clear All`: To clear both input and output.
4.  **View Results**: The processed output will appear in the right-hand "Output" text area.
5.  **Error Messages**: Any errors during processing will be displayed below the text areas.

### Example: Formatting JSON

**Input:**
```json
{"name":"John Doe","age":30,"isStudent":false,"courses":[{"title":"History I","credits":3},{"title":"Math II","credits":4}]}
```

**Action:** Click `Format Code`

**Output:**
```json
{
  "name": "John Doe",
  "age": 30,
  "isStudent": false,
  "courses": [
    {
      "title": "History I",
      "credits": 3
    },
    {
      "title": "Math II",
      "credits": 4
    }
  ]
}
```

## Development

Since CodeScan is a single-file project, development is straightforward.

### Setting up Development Environment

1.  Clone the repository as described in the Installation section.
2.  Open the `index.html` file in your favorite code editor (e.g., VS Code, Sublime Text).
3.  Open `index.html` in your web browser.
4.  Make changes to the HTML, CSS, or JavaScript directly within `index.html`.
5.  Refresh your browser to see the changes.

### Running Tests

There are no automated tests currently implemented for this project. Manual testing by interacting with the UI and verifying outputs is the primary method.

### Code Style Guidelines

*   **HTML**: Semantic HTML5.
*   **CSS**: Simple, inline `<style>` block.
*   **JavaScript**: Vanilla ES6+, clear function names, comments where necessary.

### Debugging Tips

*   Use your browser's developer console (F12 or Cmd+Option+I) to inspect elements, view console logs, and debug JavaScript.
*   Add `console.log()` statements within the JavaScript functions to trace variable values.

## Deployment

Deploying CodeScan is as simple as hosting the `index.html` file.

1.  **Static Hosting**: Upload the entire `CodeScan` directory (or just `index.html` if you prefer) to any static web hosting service (e.g., GitHub Pages, Netlify, Vercel, Amazon S3, Firebase Hosting).
2.  **Local Server**: Use a simple HTTP server (as mentioned in Installation) to serve the file locally.

Since it's a client-side application, no backend or database setup is required.

## Contributing

Contributions are welcome! If you have suggestions for improvements, new features, or bug fixes, please follow these steps:

1.  **Fork the repository**.
2.  **Create a new branch**: `git checkout -b feature/your-feature-name` or `bugfix/issue-description`.
3.  **Make your changes**: Implement your feature or fix the bug.
4.  **Commit your changes**: `git commit -m 'feat: Add new feature X'` or `fix: Resolve bug Y`.
5.  **Push to your branch**: `git push origin feature/your-feature-name`.
6.  **Open a Pull Request**: Describe your changes and their benefits.

### Development Workflow

*   Keep changes focused on a single feature or bug fix per branch.
*   Ensure your code is clean, readable, and follows the existing style.
*   Test your changes manually to ensure they work as expected.

### Code Review Guidelines

*   Ensure code readability and maintainability.
*   Verify that new features align with the project's goal of simplicity and client-side operation.
*   Check for potential performance issues or browser compatibility problems.

## Troubleshooting

*   **No output/errors**: Check your browser's developer console for JavaScript errors.
*   **Formatting/Minification not working as expected**: Ensure your input code is valid JSON or a simple JavaScript object. The current implementation relies on `JSON.parse` which is strict.
*   **Page not loading**: Verify that the `index.html` file is correctly located and accessible.

## Roadmap

*   **Enhanced "Scan Code"**: Add more detailed analysis (e.g., token count, syntax highlighting, basic linting suggestions).
*   **Broader Language Support**: Integrate external libraries (e.g., Prettier, Babel standalone) for more robust formatting and beautification across different languages (JavaScript, CSS, HTML, etc.).
*   **User Interface Improvements**: Better error display, syntax highlighting for input/output areas (e.g., using CodeMirror or Ace Editor).
*   **Download/Copy Options**: Buttons to easily copy output or download as a file.
*   **Settings**: Basic options for indentation levels, etc.

## License & Credits

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

### Contributors

*   [Akshay94os](https://github.com/Akshay94os) - Initial work

### Acknowledgments

*   Inspired by various online code formatters and minifiers.