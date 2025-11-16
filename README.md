# QuietSentinel

A simple, lightweight, and privacy-respecting monitoring system for a child's Ubuntu laptop.

## Overview

This application provides a local-only web dashboard to view a child's screen time and application usage. It is designed to be transparent and non-intrusive.

The system runs as a single Docker container that serves a static HTML page. This page fetches and displays data from a log file, providing a simple and effective way to monitor usage without the need for a database or complex backend.

## Getting Started

### Prerequisites

- Docker

### Installation

1. Clone this repository.
2. Run `docker-compose up -d`.

The dashboard will be available at `http://localhost:8080`.

## How It Works

The `docker-compose.yml` file defines a single service that uses the `nginxdemos/hello` image. This service is configured to serve a custom `index.html` file and a `data` directory containing the log files.

The `index.html` file contains a simple JavaScript application that fetches the log file and displays the data in a table.
