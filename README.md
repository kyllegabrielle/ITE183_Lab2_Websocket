# ITE183 Laboratory 2: WebSocket Server

**Name:** [Your full name]  
**Course and Section:** [Your course and section]

## Overview

This project implements a real-time multi-client chat server using
Bonezegei Scripting Language. It serves a browser-based chat interface,
handles WebSocket connections, broadcasts messages to connected clients,
and displays a custom page for undefined routes.

## Features

- HTTP route handling
- Browser-based WebSocket chat interface
- Client identification and welcome messages
- Real-time message broadcasting
- Connection and disconnection logging
- Custom page for undefined routes

## Requirements

- Bonezegei Scripting Language v1.3.3
- Bonezegei package manager (`bzg`)
- Linux or GitHub Codespaces
- A web browser

## Installation

Install Bonezegei using the laboratory-provided commands:

```bash
wget https://github.com/bonezegei/Bonezegei_Scripting_Language/raw/refs/heads/main/Release/Latest/Bonezegei-x86.deb
sudo apt install ./Bonezegei-x86.deb
```

Verify that the installed version is 1.3.3:

```bash
bonezegei -v
```

Install the project dependencies:

```bash
bzg install
```

## Running the Server

```bash
bzg run
```

For local Linux execution, open:

```text
http://localhost:8000
```

For GitHub Codespaces, forward port `8000` from the Ports panel and
open its forwarded URL in a browser.

The client uses the current page's host and selects `ws:` or `wss:`
according to the page protocol.

## Testing

1. Open the chat URL in two browser tabs or windows.
2. Confirm that both clients connect and receive welcome messages.
3. Send a message from the first client and check the second.
4. Send a reply from the second client and check the first.
5. Close a client and inspect the terminal for the disconnection event.
6. Open `/invalid` to display the custom page for undefined routes.

## Screenshots

### Bonezegei Version

![Version verification](documentation/01-version.png)

### Dependency Installation

![Dependency installation](documentation/02-install.png)

### Server Startup

![Server startup](documentation/03-server-startup.png)

### Connected Client

![Connected client](documentation/04-connected-client.png)

### Multi-client Broadcasting

![Client A](documentation/05-client-a.png)

![Client B](documentation/06-client-b.png)

### Server Events

![Server events](documentation/07-server-events.png)

### Custom 404 Page

![Custom 404 page](documentation/08-404-page.png)

## References

- ITE183 Laboratory 2: WebSocket Server laboratory guide
- Instructor-provided example:
  https://github.com/msuiit-ph/BSL_HTTP_and_WebSocket

The implementation follows the laboratory guide, with an updated
WebSocket URL for Codespaces and a customized browser interface.

## License

MIT License. See `LICENSE`.