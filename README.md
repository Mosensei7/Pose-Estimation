🏋️ AI Trainer – Pose Detection & Exercise Counter

This project is an AI-powered fitness trainer that tracks exercises in real-time using OpenCV and Mediapipe.
It detects human body landmarks, calculates joint angles, and counts repetitions (e.g., bicep curls).

🚀 Features

Pose Detection using Mediapipe.

Track body landmarks & calculate joint angles.

Detect right/left arm curls.

Live progress bar and rep counter.

Displays FPS for performance monitoring.

📂 Project Structure
AITrainer/
│── PoseModule.py      # Pose detection & angle calculation class
│── AItrainer.py       # Main exercise counter (bicep curls example)
│── AiTrainer/curls.mp4  # Sample workout video
│── AiTrainer/test.jpg   # Sample test image
│── README.md          # Documentation

⚙️ Installation

Clone the repository and install dependencies:

git clone https://github.com/Mosensei7/AITrainer.git
cd AITrainer
pip install -r requirements.txt

requirements.txt
opencv-python
mediapipe
numpy

▶️ Usage

Run the exercise trainer:

python AItrainer.py


Default input is a sample curls.mp4 video.

Replace with your own video or webcam by modifying:

cap = cv2.VideoCapture(0)   # for webcam

📊 Output

Green progress bar fills as you complete a curl.

Rep counter shows completed curls.

Angle values can be displayed for debugging.

FPS counter shows real-time performance.

Example (screenshot):


🛠️ How It Works

PoseModule detects human landmarks using Mediapipe Pose.

Selects key points (e.g., shoulder → elbow → wrist).

Calculates angle at the elbow joint.

Maps angle range to percentage (0–100%).

Counts reps when the arm completes full curl + extension.

✨ Future Improvements

Add support for multiple exercises (push-ups, squats, lunges).

Voice or sound feedback when a rep is completed.

Workout history tracking & performance analytics.

Integration with mobile app (Flutter).

📜 License

This project is licensed under the MIT License.

🔗 Author: Mohsen Ibrahim
