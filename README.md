# API Request Builder

A fast, privacy-first, open-source API client for building, testing, and debugging HTTP requests directly in your browser.

## Features

- **HTTP Request Editor**: Supports GET, POST, PUT, PATCH, DELETE, HEAD, and OPTIONS.
- **Request Configuration**: Easily configure URL, query parameters, request headers, and authentication (Bearer, Basic, API Key).
- **Body Parsing**: Support for JSON, Form Data, and Raw Text.
- **Response Viewer**: Inspect status codes, response times, payload size, headers, and formatted JSON.
- **Local Persistence**: All data (history, collections, environments) is stored securely in your browser using IndexedDB. No backend servers, no tracking.
- **Environments**: Manage environment variables with `{{VARIABLE}}` syntax for easy switching between dev/staging/prod.

## Browser Limitations & Privacy Architecture

This application runs 100% locally in your browser. 
- **Privacy First**: We have no backend. Your requests are made directly from your browser to the target API. Your API keys and secrets never leave your machine.
- **CORS Limitations**: Because this is a browser-based client, requests are subject to Cross-Origin Resource Sharing (CORS) policies. You can only successfully query APIs that return the appropriate `Access-Control-Allow-Origin` headers. If an API restricts browser access, requests will fail with a fetch error.
- **No Remote Code Execution**: User-provided JavaScript is never executed. Responses are parsed securely.

## Installation & Development

To run this project locally:

1. Clone the repository
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the development server:
   ```bash
   npm run dev
   ```

## Contributing

Please see [CONTRIBUTING.md](CONTRIBUTING.md) for details on how to contribute.

## Roadmap

- Add Collections and Folder management.
- Import and Export workspaces to JSON.
- Add cURL import and generation capabilities.
- Advanced authentication flows (OAuth2).
