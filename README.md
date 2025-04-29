# Phlow Mirror Request

> Easily mirror any incoming HTTP request using [Phlow](https://phlow.dev/).

**Phlow Mirror Request** is a simple flow designed to capture and return all the details of an incoming HTTP request, including headers, body, path, method, client IP, and more, as a structured JSON response.

This repository serves as an example of how to use [Phlow](https://phlow.dev/) to create and execute flows.

This flow is particularly useful for:
- Testing and debugging webhooks
- Inspecting HTTP request contents
- Simulating echo servers
- Analyzing requests from third-party applications or services

## How to Use

To execute the flow from a remote package, run:

```bash
phlow https://github.com/phlowdotdev/phlow-mirror-request/archive/refs/heads/main.zip
```

Alternatively, if you have the flow locally, you can execute it directly using:

```bash
phlow .
```

This will start a local HTTP server that mirrors any received requests.

## Example Response

A request like:

```bash
GET http://localhost:3000/
Authorization: 123456
User-Agent: PostmanRuntime/7.43.3
```

Will respond with:

```json
{
  "body": "",
  "headers": {
    "cache-control": "no-cache",
    "host": "localhost:3000",
    "authorization": "123456",
    "user-agent": "PostmanRuntime/7.43.3",
    "connection": "keep-alive",
    "accept-encoding": "gzip, deflate, br",
    "accept": "*/*",
    "postman-token": "..."
  },
  "uri": "/",
  "query_params": {},
  "body_size": 0,
  "path": "/",
  "method": "GET",
  "query_string": "",
  "client_ip": "127.0.0.1:38454"
}
```

## About Phlow

**[Phlow](https://phlow.dev/)** is a lightweight, modular, and fast runtime engine for executing flows written in YAML or custom scripting (`phs`), designed with simplicity, modularity, and high performance in mind.

### Get Started with Phlow Today!

Ready to simplify your workflows and debug HTTP requests effortlessly? Download and start using **Phlow** now by visiting [Phlow.dev](https://phlow.dev/) and explore its powerful capabilities.

Happy flowing!