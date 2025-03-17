# Streamlit-Desktop

This repository provides tools to package your Streamlit application (`app.py`) into a standalone desktop executable, enabling users to run it offline without requiring deployment or an internet connection.

## Prerequisites

* Node.js and npm (Node Package Manager) installed.

## Getting Started

1.  **Prepare your Streamlit application:**
    * Replace the contents of `streamlit-app/streamlit-app.py` with the code from your Streamlit application.

2.  **Install dependencies:**
    * Open a terminal or command prompt and navigate to the root directory of this repository.
    * Run the following command:
        ```bash
        npm install
        ```

3.  **Dump the Streamlit application:**
    * Execute the following command to bundle your Streamlit application:
        ```bash
        npm run dump streamlit-app
        ```

4.  **Set the environment to production:**
    * Set the `NODE_ENV` environment variable to `production`:
        ```bash
        set NODE_ENV="production"
        ```
        * (For Linux/macOS users: `export NODE_ENV="production"`)

5.  **Serve the application (Windows):**
    * To test the application before building, run:
        ```bash
        npm run servewin
        ```
    * If the application runs successfully, proceed to the next step.

6.  **Build the executable:**
    * Run the following command to create the executable:
        ```bash
        npm run dist
        ```

7.  **Locate the executable:**
    * The executable file (`winter.exe`) will be located in the `dist/unpacked-win-win32-x64` directory.

8.  **Run the application:**
    * Execute `winter.exe`.
    * Allow approximately 10 seconds for the application to initialize.

## Directory Structure
Streamlit-Desktop/                                                 
├── streamlit-app/                                                 
│   └── streamlit-app.py  (Your Streamlit application)                                                 
├── dist/                (Output directory for the built executable)                                                 
│   └── unpacked-win-win32-x64/                                                 
│       └── winter.exe     (The executable file)                                                 
├── package.json                                                 
├── package-lock.json                                                 
└── ...                                                 

## Notes

* The build process may take some time.
* The output directory name of the executable may vary slightly depending on your operating system and node configuration.
* Ensure that any required Python dependencies for your Streamlit application are correctly installed within the bundled environment.
* For other operating systems, modify the serve and build scripts accordingly.

## Contributing

Contributions are welcome! Please feel free to submit pull requests or open issues.
