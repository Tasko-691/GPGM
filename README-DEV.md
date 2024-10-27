# GPG Manage (GPGM) - Development Documentation

## Introduction

This README file documents the development phase of GPG Manage (GPGM), an evolving tool aimed at simplifying the management and distribution of GPG keys across different key servers. This document serves as a guide to understand the development process, current features, and future plans.

## Current Status

The current version of GPGM is in the initial development phase. The core features being developed include:

1. **Command Line Interface (CLI)**: A basic CLI interface is provided with the following commands:
    - `help` (`-h`): Display help information.
    - `send` (`-s`): Send GPG keys to multiple servers.
    - `verify` (`-v`): Verify the presence of GPG keys on the listed servers.
    - `revoke` (`-r`): Deploy revocation certificates.

2. **Code Structure**: The project is structured around the Go programming language, ensuring easy compilation and deployment, especially on Linux systems.

## File Overview

- **`main.go`**: The main entry point of the application, containing logic for parsing commands and executing corresponding functions.
- **`gpg-keyservers.json`**: A JSON file to list GPG key servers. This will be used to interact with different servers to send, verify, or revoke keys.

## Current Features

- **Command Execution**: The current CLI interface can parse user commands, display help messages, and call placeholder functions for sending, verifying, and revoking GPG keys.
- **Message Management**: A centralized map (`messages`) is used to store all user-facing messages. This simplifies the maintenance of textual output and allows for future localization.

## Planned Features

- **GPG Key Management**: The functionality to send GPG keys to multiple key servers will be implemented, using the list from `gpg-keyservers.json`.
- **Verification and Synchronization**: Functions to verify the presence of GPG keys across multiple servers, ensuring availability and redundancy.
- **Revocation Certificate Deployment**: Deployment of revocation certificates to servers to ensure that invalid or compromised keys are properly revoked.

## Getting Started

To get started with GPG Manage (GPGM):

1. **Clone the Repository**: Use Git to clone the project repository.
   ```sh
   git clone <repository-url>
   ```

2. **Build the Project**: Compile the Go code.
   ```sh
   go build -o gpgm main.go
   ```

3. **Run GPGM**: Use the CLI to execute commands.
   ```sh
   ./gpgm help
   ```

## Contributing

During this development phase, contributions are welcome. To contribute:
- Fork the repository.
- Work on the `dev` branch (or create feature-specific branches).
- Make your changes and submit a pull request for review.

## Notes

This is a development-phase documentation (`README-DEV.md`) and will evolve as the project progresses. The current focus is on establishing a functional base to build and test core features.

## License

This project is licensed under the **GNU GENERAL PUBLIC LICENSE Version 3**. Future releases will include an appropriate open-source license.

