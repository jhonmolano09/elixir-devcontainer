Elixir Devcontainer Starter

A simple, ready-to-use VS Code Devcontainer configuration for Elixir development.

This starter provides a consistent, pre-configured development environment with Elixir, IEx, and common tools, allowing you to start coding immediately without worrying about local setup.

Features

Elixir & Erlang: Includes Elixir 1.19.1 and Erlang 28.1, built from the official erlang:28.1-alpine image.

PostgreSQL: A separate, linked PostgreSQL 18-alpine database service, ready for your Ecto applications.

Expert LSP: Configured to use the nightly build of the official expert LSP (via lexical-lsp.lexical) instead of Elixir-LS for the latest features.

VS Code Extensions: Pre-installs essential extensions for Elixir development:

lexical-lsp.lexical (The client for Expert)

pantajoe.vscode-elixir-credo (Credo linting)

phoenixframework.phoenix (Phoenix framework support)

Phoenix Ready: The phx_new archive is pre-installed, allowing you to generate new Phoenix projects immediately.

Hex & Rebar: Automatically installs the latest hex and rebar on container setup.

Getting Started

Clone Your Project:
Clone the repository that contains this .devcontainer configuration.

Open in Container:

Open the project folder in VS Code.

VS Code will detect the .devcontainer folder and show a notification: "Folder contains a Dev Container configuration file. Reopen folder to develop in a container."

Click the "Reopen in Container" button.

Start Coding:
That's it! The container will build, and your VS Code instance will be connected. You can open a new terminal (Ctrl+\``) and run iex` to verify your Elixir installation.

Configuration

You can easily customize this setup by editing the files in the .devcontainer folder:

.devcontainer/Dockerfile:

Change the ELIXIR_VERSION or erlang base image tag to use different versions.

Modify build-time dependencies or scripts.

.devcontainer/devcontainer.json:

Add or remove VS Code extensions from the extensions list.

Tweak LSP settings (like the lexical.server.releasePathOverride).

.devcontainer/docker-compose.yml:

Adjust the PostgreSQL version (e.g., postgres:18-alpine).

Update environment variables (like DATABASE_URL or POSTGRES_PASSWORD).
