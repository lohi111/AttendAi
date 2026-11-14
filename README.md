# AttendAI

A Flask-based attendance demo that registers students using face encodings, captures attendance through a webcam, prevents a student from being marked twice on the same day, and displays attendance records in faculty and student dashboards.

## Requirements

- Python 3.10
- A webcam for marking attendance
- On Windows, CMake and Visual Studio Build Tools with the **Desktop development with C++** workload to build `dlib`

## Setup on Windows

From the project directory, create and activate a virtual environment:

```powershell
py -3.10 -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

Run the app from the project directory:

```powershell
python app.py
```

Open <http://127.0.0.1:5000> in your browser and allow camera access when marking attendance. Bootstrap and Font Awesome are loaded from CDNs, so the page needs internet access for those assets.

The demo faculty login is `admin` / `admin123`. Do not use these credentials or Flask's debug server for a public deployment.

## Local data

Student face encodings are created in `encodings.csv`; attendance records are written to `attendance.csv`; uploaded and captured images are stored under `static/uploads/`. These are local runtime data and are intentionally excluded from Git. A new checkout starts without registered students or attendance records.
