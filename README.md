# Phlow Mirror Request

> Mirror any incoming HTTP request easily using [Phlow](https://phlow.dev/).

**Phlow Mirror Request** is a flow that captures all the data from an incoming HTTP request (such as headers, body, path, method, client IP, etc.) and sends it back as a structured JSON response.

This is extremely useful for:
- Testing integrations and webhooks
- Debugging HTTP request contents
- Simulating echo servers
- Inspecting requests sent by applications or third parties

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

---

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://github.com/codespaces/new?repo=phlowdotdev/phlow-mirror-request)
