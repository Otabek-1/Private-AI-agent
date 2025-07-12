# Private-AI-Agent

**AI-integrated personal automation agent that does the digital work you ask for.**

---

## 🧠 Description

Private-AI-Agent is a smart assistant that receives tasks from you in natural language and executes them, mimicking how a person would operate on documents and data.

It is focused on automating operations with `.doc`, `.docx`, and `.xlsx` files. You give it an instruction and the corresponding files — it will analyze them, fix if needed, and perform your task. All progress is shown to you in real-time.

---

## 🛠 Technologies

* **Node.js** — for backend task processing and server logic
* **ReactJS** — for frontend UI and real-time task monitoring
* **Socket.io** — for real-time communication
* **Multer** — for file uploads
* **docx4js / mammoth** — for reading `.docx` documents
* **xlsx** — for generating or editing Excel files
* **iconv-lite** — for encoding detection and conversion
* **LibreOffice (headless)** — for converting `.doc` to `.docx` when necessary

> ⚠️ No Python-based tooling is used in the current version. The backend is entirely powered by Node.js and JavaScript.

---

## ⚙️ Core Features (MVP)

### ✅ Natural Language Task Input

You can give instructions like:

```
"Read names and scores from this docx file and write them in two rows in Excel."
```

### ✅ File Upload Interface

Upload `.doc`, `.docx`, or `.xlsx` files along with your task.

### ✅ File Preprocessing & Validation

Every file goes through a rigorous validation pipeline:

* Check if the format is supported (`docx`, `doc`, `xlsx`)
* Check encoding (UTF-8 or Windows-1251)
* Check for empty files
* Analyze internal structure

### ✅ Auto-fix when possible

* `.doc` files are auto-converted to `.docx`
* Non-UTF-8 encodings are auto-converted (e.g. Cyrillic in Windows-1251)
* If auto-fix fails, the task fails gracefully with notification

### ✅ Real-time Task Progress

You see each stage of the task in real-time:

* ✅ Task received
* 🟡 Checking files...
* ⚙️ Processing task...
* ✅ Done (with download link)
* ❌ If error, detailed reason shown

### ✅ Dashboard Notification System

All status updates and errors are pushed live to the frontend via sockets.

---

## 📦 Folder Structure (planned)

```
private-ai-agent/
├── client/           # React frontend
├── server/           # Node.js backend
│   ├── routes/       # API endpoints
│   ├── sockets/      # Real-time logic
│   ├── tasks/        # Task handlers (docx → xlsx etc)
│   ├── utils/        # File checkers, encoders, etc
│   └── uploads/      # Temporary uploaded files
└── README.md
```

---

## 🚀 Future Plans (v2)

* Add support for **desktop-level automation** using Python (e.g., PyAutoGUI)
* Visual on-screen agents that perform actions inside applications
* Browser-based RPA features
* Intelligent NLP interpreter for understanding more complex commands

---

## ✅ Example Task Workflow

1. You upload a `.doc` file and write:
   *"Extract student names and scores, and save to Excel"*
2. Server detects `.doc` format → converts to `.docx`
3. Reads Cyrillic text → encodes properly
4. Extracts relevant data
5. Generates Excel file
6. Sends it back + shows progress live

---

## 👨‍💻 Owner

**CodeCraft Ltd**

* Author: *Otabek Burhonov*
* Signature: `-_-Sign`

> “Built to make boring work disappear.”
