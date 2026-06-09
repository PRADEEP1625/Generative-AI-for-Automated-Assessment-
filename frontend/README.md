Frontend – Generative AI for Automated Assessment and Intelligent Question Generation

Overview

The frontend of the Generative AI for Automated Assessment and Intelligent Question Generation system is developed using Next.js 16.x with TypeScript. It serves as the user-facing layer of the application and provides an intuitive, responsive, and interactive interface for educators and administrators to generate, manage, and review assessment questions. The frontend is responsible for collecting user input, communicating with the backend through RESTful APIs, and displaying generated assessment content in a structured format.

The primary objective of the frontend is to simplify the assessment creation process by providing a clean and user-friendly experience. Educators can enter a topic, subject, or study material and request the generation of Multiple Choice Questions (MCQs). The generated questions are then displayed instantly, allowing users to review, manage, and organize them for assessments.

Technology Stack

* Framework: Next.js 16.x
* Language: TypeScript
* Styling: CSS / Tailwind CSS
* API Communication: Fetch API / Axios
* State Management: React Hooks
* Development Environment: Visual Studio Code

Key Features

User-Friendly Interface

The frontend provides a modern and responsive interface that can be accessed from desktops, laptops, tablets, and mobile devices. The design focuses on simplicity and ease of use, enabling users to generate questions with minimal effort.

Topic-Based Question Generation

Users can enter a specific topic or subject area into the application. This information is sent to the backend, which processes the request and generates relevant MCQs using AI services.

Question Display and Management

Generated questions are displayed in an organized format with answer options and correct answers. Users can review the generated content before using it in assessments.

API Integration

The frontend communicates with the FastAPI backend through RESTful APIs. Data is exchanged in JSON format, ensuring efficient and secure communication between components.

Responsive Design

The interface is designed to adapt to different screen sizes, ensuring accessibility and usability across multiple devices.

Workflow

1. User enters a topic or subject.
2. Frontend validates the input.
3. Request is sent to the FastAPI backend.
4. Generated questions are received from the backend.
5. Questions are displayed to the user.
6. Users can review and manage generated questions.

Benefits

* Reduces manual effort in assessment creation.
* Provides a fast and interactive user experience.
* Supports scalability and future feature enhancements.
* Ensures smooth communication with backend services.
* Improves productivity for educators and institutions.

The frontend acts as the bridge between users and AI-powered assessment generation services, making the overall system efficient, accessible, and easy to use.

Project Architecture According to Your Database

+---------------------------------------------------+
|                   Frontend                        |
|            Next.js 16 + TypeScript                |
+---------------------------------------------------+
                      |
                      |
                      ▼
+---------------------------------------------------+
|                    FastAPI                        |
|                  Python 3.12                      |
+---------------------------------------------------+
                      |
       --------------------------------
       |              |              |
       ▼              ▼              ▼
+-------------+ +-------------+ +-------------+
| Question    | | Category    | | Assessment  |
| Management  | | Management  | | Management  |
+-------------+ +-------------+ +-------------+
                      |
                      ▼
+---------------------------------------------------+
|            ChatGPT / Gemini AI Engine             |
+---------------------------------------------------+
                      |
                      ▼
+---------------------------------------------------+
|                PostgreSQL 17                      |
|                                                   |
| question                                          |
| question_option                                   |
| question_category                                 |
| question_category_mapping                         |
| question_test_case                                |
+---------------------------------------------------+

Frontend Features Based On Your Database
1. AI Question Generator

Create a page:

/questions/generate

User Inputs:

Question Title
Question Type
Difficulty Level
Category
Number of Questions
Topic

Example:

Title:
Machine Learning Basics

Question Type:
MCQ

Difficulty:
Medium

Category:
Artificial Intelligence

AI generates:

Question
Options
Correct Answer
Explanation

Stores in:

question
question_option
2. Question Bank

Create:

/questions

Features:

Search Questions
Filter by Difficulty
Filter by Category
Filter by Question Type

Database:

question
question_category
question_category_mapping
3. Category Management

Create:

/categories

Features:

Computer Science
│
├── Data Structures
├── Operating Systems
├── AI
└── DBMS

Database:

question_category

Supports hierarchy because:

parent_question_category_id

already exists.

4. Coding Question Management

Your schema contains:

coding_snippet
question_test_case

This means you can create coding assessments.

Frontend:

Question:
Write a program to reverse a string.

Starter Code:
public class Main {

}

Test Cases:
Input: hello
Output: olleh

Database:

question
question_test_case
5. Descriptive Question Module

Your schema already supports:

descriptive_text
descriptive_char_limit

Frontend:

Explain the concept of Normalization.

Limit:
500 words

AI can generate:

Question
Answer Key
Explanation

Frontend Modules 
frontend/
│
├── public/
│   ├── images/
│   ├── icons/
│   └── logo.png
│
├── src/
│   │
│   ├── app/
│   │   ├── page.tsx
│   │   ├── layout.tsx
│   │   ├── globals.css
│   │   │
│   │   ├── dashboard/
│   │   │   └── page.tsx
│   │   │
│   │   ├── questions/
│   │   │   ├── page.tsx
│   │   │   ├── create/
│   │   │   │   └── page.tsx
│   │   │   ├── generate/
│   │   │   │   └── page.tsx
│   │   │   └── [id]/
│   │   │       └── page.tsx
│   │   │
│   │   ├── categories/
│   │   │   ├── page.tsx
│   │   │   └── create/
│   │   │       └── page.tsx
│   │   │
│   │   ├── coding-questions/
│   │   │   ├── page.tsx
│   │   │   └── generate/
│   │   │       └── page.tsx
│   │   │
│   │   ├── descriptive-questions/
│   │   │   ├── page.tsx
│   │   │   └── generate/
│   │   │       └── page.tsx
│   │   │
│   │   ├── assessments/
│   │   │   ├── page.tsx
│   │   │   ├── create/
│   │   │   │   └── page.tsx
│   │   │   └── [id]/
│   │   │       └── page.tsx
│   │   │
│   │   └── settings/
│   │       └── page.tsx
│   │
│   ├── components/
│   │   │
│   │   ├── common/
│   │   │   ├── Navbar.tsx
│   │   │   ├── Sidebar.tsx
│   │   │   ├── Footer.tsx
│   │   │   ├── Button.tsx
│   │   │   └── Loader.tsx
│   │   │
│   │   ├── questions/
│   │   │   ├── QuestionCard.tsx
│   │   │   ├── QuestionForm.tsx
│   │   │   ├── OptionList.tsx
│   │   │   └── QuestionTable.tsx
│   │   │
│   │   ├── categories/
│   │   │   ├── CategoryForm.tsx
│   │   │   └── CategoryTree.tsx
│   │   │
│   │   ├── coding/
│   │   │   ├── CodeEditor.tsx
│   │   │   ├── TestCaseForm.tsx
│   │   │   └── TestCaseTable.tsx
│   │   │
│   │   └── assessments/
│   │       ├── AssessmentForm.tsx
│   │       └── AssessmentTable.tsx
│   │
│   ├── services/
│   │   ├── api.ts
│   │   ├── question.service.ts
│   │   ├── category.service.ts
│   │   ├── assessment.service.ts
│   │   └── ai.service.ts
│   │
│   ├── hooks/
│   │   ├── useQuestions.ts
│   │   ├── useCategories.ts
│   │   └── useAssessments.ts
│   │
│   ├── types/
│   │   ├── question.ts
│   │   ├── category.ts
│   │   ├── assessment.ts
│   │   └── api.ts
│   │
│   ├── utils/
│   │   ├── constants.ts
│   │   ├── validators.ts
│   │   └── helpers.ts
│   │
│   └── styles/
│       └── custom.css
│
├── .env.local
├── package.json
├── tsconfig.json
├── next.config.ts
└── README.md

