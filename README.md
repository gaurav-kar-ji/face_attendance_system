# Face Attendance System

A real-time biometric attendance system built using Python. This application captures video from a webcam, detects faces, compares them against a known database of images, and marks attendance with a timestamp in a CSV file.

##  Special Feature: Robust Recognition
This system utilizes the powerful **`dlib`** library (via `face_recognition`). It is highly robust to facial changes.
> **Did you know?** You can provide a training photo of a person that is **several years old**, and the system will still accurately detect and recognize them in real-time today!

## Features
* **Real-Time Detection:** Instantly identifies faces via webcam stream.
* **CSV Logging:** Automatically logs the Name and Time of entry into `Attendance.csv`.
* **Duplicate Prevention:** Ensures attendance is marked only once per session for each person.
* **Visual Feedback:** Draws a bounding box and displays the name of the identified person on the screen.

## Tech Stack
* **Python 3.x**
* **OpenCV (`cv2`)**: For image processing and webcam access.
* **Face Recognition**: For generating face encodings.
* **Dlib**: The underlying engine for face detection landmarks.
* **NumPy**: For array handling.

## Important Setup Note (Privacy)
To protect user privacy, the **`Training_images`** folder is **NOT** included in this repository. You must create this folder locally to make the system work.

### Where to add photos:
1.  Create a new folder named `Training_images` inside the main project directory.
2.  Paste clear photos of the people you want to recognize into this folder.
3.  **Naming Convention:** The filename will become the person's name.
    * *Example:* `Akshat.jpg` -> The system will log "AKSHAT".
    * *Example:* `Gaurav.png` -> The system will log "GAURAV".

## Project Structure
```text
Face_Attendance_System/
│
├── Training_images/       <-- [create this folder & add your photos here]
│   ├── Akshat.jpg
│   └── Dweepayan.jpg
│
├── main.py                # The main source code
├── Attendance.csv         # The file where attendance is stored
├── requirements.txt       # List of libraries
└── README.md              # Documentation
```
### ⚙️ How to Run
1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/gaurav-kar-ji/face_attendance_system.git](https://github.com/gaurav-kar-ji/face_attendance_system.git)
    cd face_attendance_system
    ```
2.  **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
    *(Note: This project requires `cmake` and `dlib` to be installed).*
3.  **Run the Application:**
    ```bash
    python main.py
    ```
4.  **Quit:**
    Press **'q'** on your keyboard (while the webcam window is active) to stop the program.
