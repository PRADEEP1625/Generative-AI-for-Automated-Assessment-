Backend – Generative AI for Automated Assessment and Intelligent Question Generation

Overview

The backend of the Generative AI for Automated Assessment and Intelligent Question Generation system is developed using FastAPI 0.136.x and Python 3.12. It serves as the core processing layer of the application and is responsible for handling requests, implementing business logic, communicating with AI services, and managing database operations.

The backend receives requests from the frontend whenever a user wants to generate assessment questions. It processes the user input, interacts with ChatGPT AI or Gemini AI, and returns generated Multiple Choice Questions (MCQs) along with answer options and correct answers. The backend also stores generated content in PostgreSQL 17, enabling efficient management of question banks and assessment records.

Technology Stack

* Framework: FastAPI 0.136.x
* Programming Language: Python 3.12
* Database: PostgreSQL 17
* AI Integration: ChatGPT AI / Gemini AI
* API Architecture: RESTful APIs
* Data Validation: Pydantic
* Database Connectivity: SQLAlchemy

Core Responsibilities

Request Processing

The backend receives requests from the frontend through REST APIs. Each request contains information such as the topic, subject, or study material provided by the user.

AI Integration

The system integrates with advanced Large Language Models (LLMs) such as ChatGPT AI or Gemini AI. These models generate context-aware MCQs based on user-provided topics.

Business Logic

The backend implements the rules and logic required for generating, validating, and managing assessment questions. It ensures that the generated content meets the desired format and quality standards.

Database Management

All generated questions and assessment-related information are stored in PostgreSQL 17. This enables efficient retrieval, modification, and management of data.

API Development

FastAPI is used to create high-performance RESTful APIs. These APIs serve as the communication layer between the frontend and backend.

Workflow

1. User submits a topic from the frontend.
2. Backend receives the request.
3. Input is validated using FastAPI and Pydantic.
4. Prompt is generated for ChatGPT AI or Gemini AI.
5. AI service returns generated MCQs.
6. Questions are processed and formatted.
7. Generated content is stored in PostgreSQL.
8. Results are returned to the frontend.
9. Frontend displays generated questions to the user.

Database Operations

The backend interacts with PostgreSQL to:

* Store generated questions.
* Manage assessment records.
* Maintain question banks.
* Retrieve previously generated content.
* Support future analytics and reporting features.

Advantages of FastAPI

* High performance and speed.
* Automatic API documentation.
* Easy integration with Python AI libraries.
* Strong support for asynchronous programming.
* Scalable architecture for large applications.

Benefits

* Automates assessment question generation.
* Reduces manual workload for educators.
* Ensures centralized storage of assessment data.
* Supports scalable AI-powered educational solutions.
* Provides secure and efficient API communication.

The backend serves as the intelligence layer of the system, connecting user requests, AI services, and database storage to create a complete automated assessment generation platform.

