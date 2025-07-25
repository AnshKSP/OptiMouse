# 🚀 OptiMouse: Hands-Free Computer Control

Optimouse is a Python application that allows you to control your computer's mouse and perform various actions using only your eyes and voice. It leverages your webcam for eye-tracking and your microphone for voice commands, providing a seamless, hands-free navigation experience.

This project is built for accessibility and to explore new ways of human-computer interaction.

---

## ✨ Features

* **Eye-Tracking Mouse Control:** Move your cursor across the screen by simply looking around. The application uses MediaPipe's Face Mesh to track your eye movements in real-time.
* **Blink to Click:** Perform a left-click by blinking with both eyes.
* **Voice-Activated Commands:** Activate a voice assistant by saying "Hey Google" to perform a wide range of actions.
* **Comprehensive Voice Commands:**
    * **Navigation:** Click, scroll up/down, close windows.
    * **Web Browse:** Open specific websites (Google, YouTube, Gmail, Maps) or search for any topic.
    * **System Control:** Adjust or mute system volume, play music, and stop the program.
* **Text-to-Speech Feedback:** The application provides voice feedback to confirm when it's activated and listening for commands.

---

## 🛠️ How It Works

1.  **Initialization:** The script starts by initializing the webcam, the Text-to-Speech engine, and Mediapipe's FaceMesh model.
2.  **Eye Tracking:** It captures video from the webcam and processes each frame to detect facial landmarks. The coordinates of the left eye are used to control the position of the mouse cursor.
3.  **Blink Detection:** The Eye Aspect Ratio (EAR) is calculated for both eyes. When the EAR drops below a certain threshold for both eyes simultaneously, it registers a blink and triggers a mouse click.
4.  **Voice Command Listener:** A separate thread runs in the background to listen for the "Hey Google" activation phrase. Once activated, it listens for and executes a predefined set of commands.

---

## 🚀 Getting Started

To get Optimouse running on your local machine, follow these steps.

### Prerequisites

* Python 3.x
* A webcam
* A microphone

### Installation

1.  **Clone the repository:**
    ```sh
    git clone [https://github.com/your-username/your-repository-name.git](https://github.com/your-username/your-repository-name.git)
    cd your-repository-name
    ```
2.  **Install the required packages:**
    Create a `requirements.txt` file with the following content:
    ```text
    opencv-python
    mediapipe
    pyautogui
    numpy
    SpeechRecognition
    pyttsx3
    googletrans==4.0.0-rc1
    ```
    Then, run the installation command:
    ```sh
    pip install -r requirements.txt
    ```
    *Note: You may also need to install PortAudio if you encounter issues with PyAudio (a dependency of SpeechRecognition). `brew install portaudio` on macOS or `sudo apt-get install portaudio19-dev` on Debian/Ubuntu.*

---

## Usage

1.  Run the main script from your terminal:
    ```sh
    python main.py
    ```
2.  The application will start, and you will hear an introductory message. A window showing your webcam feed will appear.
3.  Move your eyes to control the mouse cursor.
4.  Blink with both eyes to perform a click.
5.  Say "Hey Google" to activate the voice command listener.
6.  Press the 'q' key on the keyboard while the webcam window is active to quit the program.

### Available Voice Commands

Once activated, you can use the following commands:

* `click`
* `scroll up`
* `scroll down`
* `close window`
* `open browser`
* `open youtube`
* `open gmail`
* `open google maps`
* `search for [your query]`
* `play music`
* `increase volume`
* `decrease volume`
* `mute volume`
* `stop program`
* `stop listening` / `ok google` (to deactivate voice commands)

---

## 📂 File Structure

```
.
├── main.py      # Main script containing the core application logic.
└── utils.py     # Optional file for helper functions.
```
### 🚀 Run It

Install the required packages:

```bash
pip install -r requirements.txt
```
