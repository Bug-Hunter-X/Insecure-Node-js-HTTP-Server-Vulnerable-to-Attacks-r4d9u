# Insecure Node.js HTTP Server
This repository demonstrates a vulnerable Node.js HTTP server and its secure counterpart. The insecure server is missing crucial security measures, making it susceptible to common attacks. The secure version addresses these vulnerabilities, offering a more robust and protected implementation.

## Insecure Server (`insecureServer.js`)
The `insecureServer.js` file contains a basic HTTP server that's vulnerable due to the absence of essential security headers and error handling. Running this server without proper mitigation exposes it to several risks, including denial-of-service (DoS) attacks.

## Secure Server (`secureServer.js`)
The `secureServer.js` file provides a more secure version of the server.  It includes the following improvements:

* **HTTP Strict Transport Security (HSTS):** Ensures that the server is accessed only over HTTPS, preventing man-in-the-middle attacks.
* **X-Frame-Options:** Protects against clickjacking by controlling where the server's content can be embedded.
* **Content-Security-Policy (CSP):** Reduces the risk of cross-site scripting (XSS) attacks by defining allowed sources for scripts, styles, and other resources.
* **Error Handling:** Includes comprehensive error handling to prevent unexpected crashes and information leaks.

## How to Run
1. Clone this repository.
2. Navigate to the repository's directory.
3. Run `npm install` to install dependencies (if any).
4. Run `node insecureServer.js` to start the insecure server.
5. Run `node secureServer.js` to start the secure server.

## Learning Points
This example highlights the importance of implementing proper security measures in any Node.js application.  Ignoring these can lead to serious vulnerabilities and compromise user data and system stability.