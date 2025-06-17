# MCP-Server

A Node.js server implementation using the Model Context Protocol (MCP) SDK. This project provides weather-related tools via MCP, including weather alerts and forecasts for US locations using the National Weather Service (NWS) API.

## Features
- **Weather Alerts**: Get real-time weather alerts for any US state.
- **Weather Forecast**: Retrieve detailed weather forecasts for any US location (latitude/longitude).
- Built with [@modelcontextprotocol/sdk](https://www.npmjs.com/package/@modelcontextprotocol/sdk) and [zod](https://www.npmjs.com/package/zod).

## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/silky-x0/MCP-Server.git
   cd MCP-Server
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Build the project:
   ```sh
   npm run build
   ```

## Usage

Run the server (after building):
```sh
node build/index.js
```

The server will start and listen for MCP requests via stdio.

---

## Using with Claude Desktop

You can use MCP-Server as a custom tool in Claude Desktop (Anthropic's desktop app) by following these steps:

1. **Build the project** (if you haven't already):
   ```sh
   npm run build
   ```
2. **Open Claude Desktop** and go to the "Tools" section.
3. **Add a new custom tool**:
   - Set the tool type to **MCP (Model Context Protocol)**.
   - For the command, enter the path to your built server, for example:
     - On Windows:
       ```
       node C:\path\to\your\project\build\index.js
       ```
     - On macOS/Linux:
       ```
       node /path/to/your/project/build/index.js
       ```
   - Give your tool a name, e.g., `Weather MCP Server`.
4. **Save** and enable the tool. Now you can use the weather tools (`get-alerts`, `get-forecast`) directly from Claude Desktop!

---

### Available Tools
- `get-alerts`: Get weather alerts for a US state (e.g., `CA`, `NY`).
- `get-forecast`: Get weather forecast for a location by latitude and longitude.

## Screenshots

> ![Tools](https://github.com/user-attachments/assets/80b74fff-7636-4a81-8007-15a7d3df6e28)

> ![Query result](https://github.com/user-attachments/assets/9f1950b3-a557-45a4-8cbe-6a92b1ab0ec7)

> 
> 

## Contributing
Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

## License
[ISC](LICENSE)
