Step 1: GitHub Setup

Forked the CSN150 Documentation Template repository from https://github.com/ereedsanchez/CSN150-Doc-Template
.

Created this fork to document my ESP32-CAM setup process.

I’ll use this repository to track installation steps, screenshots, and notes for future assignments.

Step 2: Arduino IDE Installation (In Progress)

Downloading and installing the Arduino IDE from the official site: https://www.arduino.cc/en/software/
.

Will include screenshots once the installation is complete.

Step 3: ESP32-CAM Setup (To Be Completed)

Planning to follow the Last Minute Engineers ESP32 Arduino IDE tutorial to install board drivers and test the blink sketch.

Documentation will be updated once the ESP32 is connected and tested successfully.





_______________________________________________________________________________________________________________________________
UPDATE 


Summary:
Successfully uploaded and tested the ESP32 Blink sketch. The onboard LED blinked as expected after resolving an upload issue.

⚙️ Steps I Took

Installed the ESP32 board package in Arduino IDE using the Additional Boards URL.

Installed the CH340 driver (for USB communication).

Selected the correct board (AI Thinker ESP32-CAM or ESP32 Dev Module) and port.

Uploaded the Blink sketch to test setup.

⚠️ Error Encountered

Error message:

A fatal error occurred: Failed to connect to ESP32: Timed out waiting for packet header


Cause:
The ESP32 wasn’t in flashing mode when I tried to upload the sketch. This is a common issue when the board isn’t properly reset before upload.

Solution:

Press and hold the “BOOT” button on the ESP32 while clicking Upload in Arduino IDE.

Release the BOOT button as soon as the “Connecting…” message appears in the IDE.

The upload completed successfully afterward.

✅ Result

The Blink sketch uploaded without errors.

The onboard LED blinks every second.

Changing delay(1000) to delay(200) made it blink faster; changing it to delay(2000) made it slower.

