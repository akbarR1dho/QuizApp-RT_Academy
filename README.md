# QuizApp

An interactive and modern web-based Quiz Application built with **Laravel** and **TailwindCSS**. This application relies entirely on **JSON files** for data storage (no SQL/NoSQL database required), making it extremely lightweight and easy to customize.

---

## Prerequisites
Before running this project, ensure your system has the following installed:
1. [PHP](https://www.php.net/downloads.php) (Version 8.2 or newer)
2. [Composer](https://getcomposer.org/download/)
3. [Node.js & npm](https://nodejs.org/)

---

## Installation Steps (Setup)

Follow the steps below to run the application locally:

### 1. Open Terminal
Navigate your terminal or command prompt to the `quizapp` project directory.

### 2. Install PHP Dependencies
Run the following command to install all required Laravel PHP packages:
```bash
composer install
```

### 3. Environment Configuration (`.env`)
Copy the `.env.example` file and rename it to `.env`:
```bash
cp .env.example .env
```
*(Note: This application does not require database connection configurations in the `.env` file since it uses JSON)*

### 4. Generate Application Key
Generate the app key for Laravel:
```bash
php artisan key:generate
```

### 5. Install Frontend Dependencies (TailwindCSS)
Run the following command to install the necessary Node.js packages:
```bash
npm install
```

---

## How to Run the Application

To run this application with proper styling, you need to run both the backend (Laravel) and frontend (Vite/TailwindCSS) servers simultaneously.

Open **2 (two) separate terminals** in your project directory:

**Terminal 1 (Backend - Laravel):**
```bash
php artisan serve
```

**Terminal 2 (Frontend - Tailwind/Vite):**
```bash
npm run dev
```

Once both are running, open your browser and go to:
**`http://127.0.0.1:8000`**

---

## How to Add New Quiz Data
Quiz data files are located in the `storage/app/quizzes/` folder. 
To add a new quiz, simply create a new `.json` file inside that directory using the following format:

```json
{
  "title": "Quiz Topic Name",
  "time_limit_seconds": 60,
  "questions": [
    {
      "id": 1,
      "question": "First Question?",
      "options": {
        "a": "Option A",
        "b": "Option B",
        "c": "Option C",
        "d": "Option D"
      },
      "answer": "b"
    }
  ]
}
```

Happy learning and playing! If you have any further questions, feel free to explore the source code.
