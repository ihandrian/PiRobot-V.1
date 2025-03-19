# PiRobot V.1

## Key Improvements Implemented

https://github.com/user-attachments/assets/c549cace-67d4-4eec-b868-973418a37e95

I've made all the improvements from [PiRobot V.0](https://github.com/ihandrian/PiRobot-V.0) with improvement such as:

### 1. Person Detection and Following

- Added a lightweight `PersonDetector` class using TensorFlow Lite and YoloV3 for efficient person detection on Raspberry Pi 3B
- Implemented a `PersonFollower` class that makes the robot follow the nearest detected person
- The system automatically downloads the required model files if they're not present
- Added controls to enable/disable detection and start/stop following
- The robot will adjust its speed and direction based on the person's position and distance


### 2. Fullscreen Video Feed with Overlay Controls

- Redesigned the interface with a fullscreen video feed
- Added a semi-transparent control panel in the bottom left corner
- Replaced text buttons with arrow icons for more intuitive control
- The control panel has 80% opacity
- Added touch support for mobile devices


### 3. System Information Panel

- Moved system information to the top of the screen
- Made it semi-transparent with white text
- Displays CPU usage, memory usage, temperature, and detection status
- Updates in real-time


### Additional Improvements

- Added visual indicators for person detection (green bounding boxes)
- Added visual indicator for the person being followed (red bounding box)
- Improved error handling for when TensorFlow Lite or YoloV3 is not available
- Added controls to adjust the following speed
- Made the interface fully responsive for different screen sizes


## How to Use
1. Clone this repository. Save all the files to your project directory.
2. Go to your dir "PiRobot-V.1" in your computer.
3. Run virtual environment of your preference, in this case I´m using `venv` to create environment:
    ```plaintext
    python -m venv PiRobot
    ```
     - Activate:
         - Windows:
          ```plaintext
          PiRobot\Scripts\activate
          ```
         - Linux/macOS:
          ```plaintext
          source PiRobot/bin/activate
          ```
      - Deactivate:
          ```plaintext
          deactivate
          ```
3. Install the required dependencies:

```plaintext
pip3 install -r requirements.txt
```


2. Run the file `main.py`:

```plaintext
python main.py
```



3. Access the control panel at `http://<your_pi_ip>:5002`
4. To use person following:
    - Toggle "Detection" to enable person detection
    - Click "Start Following" to make the robot follow the nearest person
    - Adjust the follow speed as needed

The system is optimized for Raspberry Pi 3B and uses lightweight detection models to ensure smooth performance.
### Future Development

1. **Sensor Integration**: Add classes for different sensors (ultrasonic, IR, etc.)
2. **Autonomous Navigation**: Implement path planning and obstacle avoidance
3. ~~**Computer Vision**: Add object detection using TensorFlow Lite or similar~~
4. **Data Logging**: Implement data collection for training autonomous behaviors

Support page:
- Paypal https://paypal.me/IrfanHandrian
- Buy me Coffee https://buymeacoffee.com/handrianirv
