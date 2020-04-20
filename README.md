# code-server

`code-server` enables running [VS Code](https://github.com/Microsoft/vscode) on any machine
anywhere and being able to access it through the browser.

- **Code anywhere:** Code on your Chromebook, tablet, and laptop with a
  consistent dev environment. Develop on a Linux machine and pick up from any
  device with a web browser.
- **Server-powered:** Take advantage of large cloud servers to speed up tests,
  compilations, downloads, and more. Preserve battery life when you're on the go
  as all intensive tasks run on your server.

Try it out:

```bash
docker run -it -p 127.0.0.1:8080:8080 -v "$PWD:/home/coder/project" -u "$(id -u):$(id -g)" codercom/code-server
```

This will start a code-server container with docker and expose it at http://127.0.0.1:8080. It will also mount
your current directory into the container as `/home/container/project` and forward your UID/GID so that
all file system operations occur as your regular user.

![Example gif](/doc/assets/code-server.gif)

## Getting Started

For a proper setup and walkthrough, please see [./doc/setup.md](./doc/setup.md).

### Requirements

- 64-bit host.
- At least 1GB of RAM.
- 2 cores or more are recommended (1 core works but not optimally).
- Secure connection over HTTPS or localhost (required for service workers and
  clipboard support).
- For Linux: GLIBC 2.17 or later and GLIBCXX 3.4.15 or later.

### Run over SSH

Use [sshcode](https://github.com/codercom/sshcode) to start code-server on any Linux
machine over SSH.

### Digital Ocean

[![Create a Droplet](./doc/assets/droplet.svg)](https://marketplace.digitalocean.com/apps/code-server)

### Releases

1. [Download a release](https://github.com/cdr/code-server/releases)
2. Unpack the downloaded release then run the included `code-server` script.
3. In your browser navigate to `localhost:8080`.

## FAQ

See [./doc/FAQ.md](./doc/FAQ.md).

## Contributing

See [./doc/CONTRIBUTING.md](./doc/CONTRIBUTING.md).

## Enterprise

Visit [our enterprise page](https://coder.com) for more information about our
enterprise offerings.
