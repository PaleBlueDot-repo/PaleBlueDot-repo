# NewsTok - Integrated Microservices Setup

Welcome to the NewsTok project! This README will guide you through the steps to integrate and run the entire application, including all the microservices and frontend components.

# Table of Contents
1. [Overview](#overview)
2. [Repositories](#repositories)
3. [Prerequisites](#prerequisites)
4. [Running the Application](#running-the-application)
   - [1. Setting Up the API Gateway and Service Discovery](#1-setting-up-the-api-gateway-and-service-discovery)
   - [2. Running the Backend Services](#2-running-the-backend-services)
   - [3. Running the Python APIs](#3-running-the-python-apis)
   - [4. Running the Frontend Applications](#4-running-the-frontend-applications)
5. [Microservices Communication](#microservices-communication)



## Overview
NewsTok is a TikTok-like news application that leverages microservices architecture. The application consists of various components, each responsible for specific tasks such as news scraping, AI and ML functionalities, news reel creation, and user interactions.


![image](https://github.com/user-attachments/assets/5b2215c5-3292-4e75-82cb-ab7f4cb616b3)


### Key Components:
- **Admin Backend**: Handles admin functionalities like news scraping and news reel creation.
- **User Backend**: Manages user interactions with the news reels.
- **API Gateway & Service Discovery**: Routes requests to the appropriate microservices and handles service discovery.
- **Python APIs**: Implements AI, ML, and news scraping functionalities.
- **Admin Frontend**: Allows admin users to manage the content and interact with the backend.
- **User Frontend**: Displays news reels to the users and captures their interactions.

## Repositories

Below are the repositories associated with each component:

- **[newstok-api-gateway](https://github.com/PaleBlueDot-repo/newstok-api-gateway)**: API Gateway and Eureka Service Discovery.
- **[newstok-admin-java-backend](https://github.com/PaleBlueDot-repo/newstok-admin-java-backend)**: Admin backend server.
- **[newstok-user-java-backend](https://github.com/PaleBlueDot-repo/newstok-user-java-backend)**: User backend server.
- **[newstok-python-apis](https://github.com/PaleBlueDot-repo/newstok-python-apis)**: Python APIs for AI, ML, and news scraping.
- **[newstok-admin-frontend](https://github.com/PaleBlueDot-repo/newstok-admin-frontend)**: Admin frontend application.
- **[newstok-flutter-frontend](https://github.com/PaleBlueDot-repo/newstok-flutter-frontend)**: User frontend application.

**Note:** Detailed instructions for downloading, installing, and running each repository are provided in the README files within each individual repository. Please refer to those READMEs for specific setup steps.

## Prerequisites

Before you start, make sure you have the following installed on your machine:

- **Java 11 or later**
- **Spring Boot**
- **Node.js & npm**
- **Flutter**
- **Python 3.x**
- **Docker (Optional for running services in containers)**

Ensure you clone all the repositories listed above.

## Running the Application

### 1. Setting Up the API Gateway and Service Discovery

First, you need to set up the API Gateway and Eureka Service Discovery:

```bash

# Build and run the Eureka-Server
cd newstok-Api-Gateway/Eureka-Server

# Build and run the API Gateway
cd newstok-Api-Gateway/ApiGateway

# Eureka Server will also start along with the API Gateway
```

### 2. Running the Backend Services

Run the Admin and User backend servers:
Given all the instructions in the newstok-admin-java-backend and  newstok-user-java-backend repositories Readme files


### 3. Running the Python APIs

Start the Python APIs that handle AI, ML, and news scraping:

```bash
# Navigate to the Python APIs repo
cd newstok-python-apis

# Install dependencies
pip install -r requirements.txt

# Run the Python API server
python app.py
```

### 4. Running the Frontend Applications

Finally, run the Admin and User frontends:

```bash
# Admin Frontend
cd newstok-admin-frontend

# Run the Admin Frontend
Given all the instructions in the newstok-admin-frontend  repositories Readme files

# User Frontend
cd ../newstok-flutter-frontend

# Get Flutter dependencies
flutter pub get

# Run the Flutter app
flutter run
```

## Microservices Communication

- **Admin Backend**: Communicates with the Python APIs for AI, ML, and news scraping tasks using API keys.
- **User Backend**: Interacts with the Admin Backend to fetch news reels and save user interactions.
- **API Gateway**: Acts as a central point, routing requests to the appropriate microservices.
- **Admin Frontend**: Allows admins to perform CRUD operations on news and news reels and interacts with the Admin Backend.
- **User Frontend**: Displays the news reels fetched from the User Backend and sends user interactions back to the backend.

