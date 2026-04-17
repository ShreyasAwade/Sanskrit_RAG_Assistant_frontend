# 🧠 Sanskrit RAG Frontend (React UI)

## 📌 Overview

This is the frontend interface for the Sanskrit Retrieval-Augmented Generation (RAG) system. It provides a clean and interactive UI for users to:

* Upload Sanskrit documents (.txt / .pdf)
* Ask questions in Sanskrit (or transliterated text)
* View generated answers based on retrieved context

The frontend communicates with a Flask-based backend via REST APIs.

---

## 🚀 Features

* 📄 File upload support (.txt, .pdf)
* 💬 Chat-style question-answer interface
* ⚡ Real-time API interaction
* 🔒 Input validation (prevents querying before upload)
* 📱 Responsive UI (works on desktop and mobile)
* 🎨 Clean and modern design using Bootstrap + custom CSS

---

## 🛠️ Tech Stack

* **React.js** – UI development
* **Bootstrap** – Styling and responsiveness
* **Axios** – API communication
* **JavaScript (ES6+)**

---

## 📂 Project Structure

```
frontend/
│
├── src/
│   ├── App.js
│   ├── App.css
│   ├── index.js
│   │
│   ├── services/
│   │   └── api.js
│
├── public/
├── package.json
```

---

## ⚙️ Setup Instructions

### 1. Clone the repository

```
git clone <your-repo-url>
cd frontend
```

### 2. Install dependencies

```
npm install
```

### 3. Start the development server

```
npm start
```

The app will run on:

```
http://localhost:3000
```

---

## 🔗 Backend Integration

Ensure the backend server is running at:

```
http://127.0.0.1:5000
```

Update API base URL in:

```
src/services/api.js
```

---

## 📡 API Endpoints Used

### 1. Upload Document

```
POST /upload
```

* Sends file using FormData
* Builds retrieval index on backend

---

### 2. Query

```
POST /query
```

Request:

```
{
  "query": "धर्मः किम्?"
}
```

Response:

```
{
  "answer": "..."
}
```

---

## 🧠 Usage Flow

1. Upload a Sanskrit document
2. Wait for successful processing
3. Enter a query
4. View generated answer in chat interface

---

## Notes & Limitations

* Only one document is active at a time
* Uploading a new file replaces the previous context
* Requires backend to be running
* Model performance depends on document quality and query clarity

---

## 💡 Future Improvements

* Chat history persistence
* Multi-document support
* Typing animation for responses
* File upload progress indicator
* User session handling

---

## 👨‍💻 Author

Shreyas Awade

---

