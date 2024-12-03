# Get Songs Microservice

A Flask-based microservice that retrieves lyrics of a popular band's songs from a MongoDB database. This microservice supports a RESTful API and is a key component of the band's website application.

---

## Table of Contents

- [About the Project](#about-the-project)
  - [Key Features](#key-features)
  - [Solution Architecture](#solution-architecture)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
  - [Installation](#installation)
- [Usage](#usage)
- [Development and Deployment](#development-and-deployment)

---

## About the Project

The **Get Songs Microservice** enables:
- Storing and retrieving song lyrics from MongoDB.
- Exposing APIs to query popular songs.
- Providing health status endpoints for monitoring.

This microservice is part of a multi-service application built for a popular music band.

### Key Features

- **MongoDB Integration**: Stores and fetches lyrics.
- **RESTful APIs**: CRUD operations for lyrics.
- **Health Endpoint**: Monitor the service.

### Solution Architecture

- **Frontend**: Consumes lyrics data via API.
- **Backend**: Flask REST API with MongoDB for persistence.
- **Deployment**: Hosted on RedHat OpenShift.

---

## Tech Stack

- **Framework**: Flask
- **Database**: MongoDB
- **Driver**: PyMongo
- **Deployment**: RedHat OpenShift

---

## Getting Started

### Installation

1. Install virtual environment:
   ```bash
   cd /Back-End-Development-Songs
   bash ./bin/setup.sh
   ```

2. Start
   ```bash
   MONGODB_SERVICE=localhost MONGODB_USERNAME=root MONGODB_PASSWORD=password flask run --reload --debugger
   curl -X GET -i -w '\n' localhost:5000/health
   ```

---

## Usage

- GET `/health`: Check microservice health.
- GET `/count`: Count the number of documents in the songs collections of the band database.
- GET `/song`: List.
- GET `/song/<id>`: Read.
- POST `/song`: Create.
- PUT `/song/<id>`: Update a song.
- DELETE `/song/<id>`: Delete a song.

---

## Development and Deployment

### Testing

- Run tests using pytest

### Deployment

- Build and push Docker image.
- Deploy to RedHat OpenShift.
