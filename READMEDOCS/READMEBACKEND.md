# Backend Documentation

## Table of Contents
1. [Overview](#overview)
2. [Core Components](#core-components)
3. [Application Structure](#application-structure)
4. [API Endpoints](#api-endpoints)
5. [Authentication & Security](#authentication--security)
6. [Data Management](#data-management)
7. [Video Processing](#video-processing)
8. [Caching System](#caching-system)
9. [Environment Configuration](#environment-configuration)
10. [Dependencies](#dependencies)

## Overview

This is a FastAPI-based backend application that provides video analysis and chatbot capabilities. The system integrates with Supabase for data persistence, Redis for caching and task queuing, and includes robust authentication mechanisms.

### Key Features
- Video upload and analysis
- Real-time chat functionality
- User authentication and session management
- Redis-based caching and task queue
- Supabase integration for data persistence

## Core Components

### Main Application (app.py)
The main FastAPI application file (`app.py`) serves as the entry point and contains:

Key configurations include:
- FastAPI application initialization with custom title and documentation URLs
- Environment variable loading
- Redis and Supabase client initialization
- CORS middleware setup
- Static file serving configuration

### Authentication System

The authentication system uses a session-based approach with Redis for session storage:

Features:
- Session-based authentication
- Secure cookie handling
- Redis session storage
- Configurable session lifetime
- Automatic session cleanup

### Database Integration

Database operations are handled through Supabase, with the following key features:

1. User Management:
- User creation and retrieval
- Email-based user lookup
- User existence verification

2. Chat History:
- Message storage and retrieval
- User-specific chat history
- Cached access patterns

3. Video Analysis:
- Video metadata storage
- Analysis results persistence
- Historical analysis tracking

### Redis Implementation

The application uses Redis for multiple purposes:

1. Session Management:
- Session data storage
- Session expiration handling
- User authentication state

2. File Storage:
- Temporary video file storage
- Efficient binary data handling
- Automatic cleanup mechanisms

3. Task Queue:
- Priority-based task processing
- Video processing queue
- Analysis task management

### API Endpoints

#### Chat Endpoints

1. Chat History Endpoint:
Features:
- Cached chat history retrieval
- User-specific history filtering
- Redis cache integration

2. Video Analysis History:
Features:
- Analysis history retrieval
- Cache-first approach
- User-specific filtering

3. Message Handling:
Features:
- Multi-file upload support
- Video processing queue integration
- Real-time analysis
- Cache invalidation
- Error handling

## Authentication & Security

### Session Configuration
The application uses secure session management with the following features:

1. Session Parameters:
- Configurable lifetime
- Secure cookie settings
- HTTPS-only cookies
- Cross-site request protection

2. Security Measures:
- CORS protection
- Request rate limiting
- Secure headers
- Input validation

## Data Management

### Supabase Integration

The application uses Supabase for persistent storage:

1. Connection Setup:
- Environment-based configuration
- Connection pooling
- Error handling

2. Tables:
- Users table for authentication
- Chat_messages for conversation history
- Video_analysis for analysis results

### Redis Storage

Redis is used for:
1. Session data
2. Temporary file storage
3. Task queue
4. Cache storage

## Video Processing

### Video Analysis Pipeline

1. Upload Process:
- File validation
- Temporary storage
- Queue addition

2. Analysis:
- Metadata extraction
- Content analysis
- Result storage

3. Result Management:
- Database storage
- Cache updates
- User notification

## Caching System

### Implementation Details

1. Cache Keys:
- User-specific prefixes
- Content-based hashing
- TTL management

2. Invalidation Strategy:
- Time-based expiration
- Manual invalidation
- Update triggers

## Environment Configuration

Required environment variables:

GEMINI_API_KEY
SESSION_SECRET_KEY
SUPABASE_ANON_KEY
SUPABASE_SERVICE_ROLE_KEY
SUPABASE_URL


## Dependencies

Key dependencies from requirements.txt:
- FastAPI (v0.95.2): Web framework
- uvicorn (v0.22.0): ASGI server
- python-multipart: File upload handling
- python-dotenv: Environment management
- Supabase: Database client
- Redis: Caching and queuing
- Additional utilities for video processing and security

### Installation

1. Create virtual environment:
```
python -m venv venv
```
2. Install dependencies:
```
pip install -r requirements.txt
```
3. Run the application:

uvicorn app:app --host 0.0.0.0 --port 3000 --reload


## Development Guidelines

1. Code Structure:
- Maintain separation of concerns
- Use type hints
- Follow PEP 8 guidelines

2. Error Handling:
- Use appropriate HTTP status codes
- Implement proper error messages
- Log errors appropriately

3. Testing:
- Write unit tests
- Implement integration tests
- Use test coverage tools

4. Documentation:
- Keep API documentation updated
- Document complex functions
- Maintain this README

This documentation provides a comprehensive overview of the backend system. For specific implementation details, refer to the individual source files and inline documentation. This documentation provides an extremely detailed overview of the backend system, covering all major components, their interactions, and implementation details. It's designed to give new developers a complete understanding of the system's architecture and functionality.