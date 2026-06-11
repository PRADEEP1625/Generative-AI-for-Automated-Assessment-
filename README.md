 Generative AI for Automated Assessment and Intelligent Question Generation

 Project Description 

Generative AI for Automated Assessment and Intelligent Question Generation is an innovative web-based application designed to automate and simplify the process of creating educational assessments using Artificial Intelligence. In traditional educational environments, preparing high-quality assessment questions requires significant time, effort, and subject expertise. Educators often spend hours creating multiple-choice questions, ensuring accuracy, maintaining relevance to the syllabus, and preparing answer keys. This project aims to address these challenges by leveraging advanced Generative AI technologies to automatically generate intelligent, context-aware, and curriculum-relevant assessment questions.
The system enables educators, trainers, and academic institutions to generate Multiple Choice Questions (MCQs) by simply providing a topic, subject name, keyword, or study material. Once the input is provided, the analyze the content and generate meaningful assessment questions along with multiple answer options and the corresponding correct answers. This significantly reduces manual effort and improves the overall efficiency of assessment preparation.
The frontend of the application is developed using Next.js 16.x with TypeScript, providing a modern, responsive, and user-friendly interface. Next.js offers excellent performance, server-side rendering capabilities, and an optimized development environment that enhances the user experience. TypeScript adds strong typing support, improving code quality, maintainability, and scalability. The frontend allows users to enter topics, submit requests for question generation, view generated questions, and manage assessment content through an intuitive interface.
The backend is implemented using FastAPI 0.136.x and Python 3.12. FastAPI is a high-performance web framework that facilitates the development of scalable and efficient RESTful APIs. The backend is responsible for processing user requests, validating inputs, handling business logic, communicating with AI services, and managing database operations. Python serves as the primary programming language due to its extensive ecosystem of AI and machine learning libraries, making it highly suitable for integrating Generative AI services.
A key feature of the system is its integration with ChatGPT AI or Gemini AI. These advanced AI models can understand context, analyze educational content, and generate high-quality questions tailored to specific topics. The generated MCQs include carefully constructed answer options and accurate correct answers, ensuring that the resulting assessments maintain educational value and relevance. This AI-driven approach provides flexibility and adaptability across various academic disciplines, including computer science, mathematics, engineering, business studies, and many other fields.
To ensure efficient storage and management of generated content, the application uses PostgreSQL 17 as its database management system. PostgreSQL serves as a centralized repository for storing generated questions, question banks, assessment records, and user-related information. The database allows users to retrieve previously generated questions, organize assessments, and maintain a structured collection of educational resources for future use.
The workflow of the system begins when a user enters a topic or study material through the frontend interface. The frontend sends the request to the FastAPI backend using RESTful APIs. The backend then constructs an appropriate prompt and communicates with the selected AI service. After receiving the generated questions from the AI model, the backend processes the response, stores the generated content in PostgreSQL, and returns the results to the frontend. The generated MCQs are then displayed to the user, who can review, edit, manage, or utilize them for assessment creation.
The primary objective of this project is to reduce the manual workload associated with question preparation, improve the efficiency and accuracy of assessment creation, and provide a scalable AI-powered solution for educational institutions. By automating the question generation process, educators can focus more on teaching and student engagement while ensuring that assessments remain diverse, relevant, and up-to-date. The project demonstrates the practical application of Artificial Intelligence in education and highlights how Generative AI can transform traditional academic processes through automation, intelligence, and scalability.

Technology Stack

| Component      | Technology              | Version |
| -------------- | ----------------------- | ------- |
| Frontend       | Next.js with TypeScript | 16.x    |
| Backend        | FastAPI                 | 0.136.x |
| Language       | Python                  | 3.12    |
| Database       | PostgreSQL              | 17      |
| AI Integration | ChatGPT AI / Gemini AI  | Latest  |

Objectives

* Automate MCQ generation using Generative AI.
* Reduce manual effort in assessment creation.
* Generate intelligent and context-aware questions.
* Store and manage question banks efficiently.
* Provide a scalable solution for educational institutions.
System Architecture

Architecture

```mermaid
flowchart TD

    User([User])

    Frontend[Next.js Frontend<br/>TypeScript]

    Backend[FastAPI Backend<br/>Python 3.12]

    AI[AI Services<br/>OpenAI / Gemini]

    DB[(PostgreSQL 17)]

    MCQ[MCQ Generation]
    Coding[Coding Question Generation]
    Assessments[Assessment Management]
    Categories[Category Management]

    User --> Frontend
    Frontend --> Backend

    Backend --> AI
    Backend --> DB

    AI --> MCQ
    AI --> Coding

    DB --> Assessments
    DB --> Categories
```
Modules 
Project Structure

```text
Generative-AI-for-Automated-Assessment/
│
├── frontend/
│   ├── public/
│   │   ├── images/
│   │   ├── icons/
│   │   └── logo.png
│   │
│   ├── src/
│   │   ├── app/
│   │   │   ├── dashboard/
│   │   │   ├── questions/
│   │   │   ├── coding/
│   │   │   ├── assessments/
│   │   │   ├── categories/
│   │   │   ├── settings/
│   │   │   ├── layout.tsx
│   │   │   └── page.tsx
│   │   │
│   │   ├── components/
│   │   │   ├── Navbar.tsx
│   │   │   ├── Sidebar.tsx
│   │   │   ├── Footer.tsx
│   │   │   ├── Loader.tsx
│   │   │   └── Button.tsx
│   │   │
│   │   ├── services/
│   │   ├── hooks/
│   │   ├── types/
│   │   └── utils/
│   │
│   ├── package.json
│   ├── tsconfig.json
│   └── next.config.ts
│
├── backend/
│   ├── app/
│   │   ├── api/
│   │   │   ├── question_routes.py
│   │   │   ├── category_routes.py
│   │   │   ├── assessment_routes.py
│   │   │   └── ai_routes.py
│   │   │
│   │   ├── services/
│   │   │   ├── openai_service.py
│   │   │   ├── gemini_service.py
│   │   │   └── question_service.py
│   │   │
│   │   ├── models/
│   │   ├── schemas/
│   │   └── database/
│   │
│   └── main.py
│
├── README.md
└── .env.local

Project Flow

User
  │
  ▼
Next.js Frontend
  │
  ▼
FastAPI Backend
  │
  ├── Question Service
  ├── Category Service
  ├── Assessment Service
  └── AI Service
           │
           ▼
    ChatGPT / Gemini
           │
           ▼
      PostgreSQL
           │
           ▼
Generated Questions
Assessment Papers
Coding Problems
Question Bank
```
