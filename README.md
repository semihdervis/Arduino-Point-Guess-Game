# Arduino Point Guess Game

This project implements a turn-based point guessing game on Arduino. The objective is to guess the opponent's selected pixel using hot and cold instructions faster than they find yours. The game utilizes two Arduinos connected via serial communication.

> **🎥 Watch the demo on [YouTube](https://www.youtube.com/watch?v=zoDZ3X8Gaco&feature=youtu.be).**

## Simulation Usage

To simulate the game, you can use the Wokwi simulator. Since the simulator doesn't support two physical players, one player's input can be emulated via the serial monitor.

> **🌐 Try the simulation on [Wokwi](https://wokwi.com/projects/408512621518631937).**

### Step 1: Select a Pixel

Use the joystick to select a pixel. This position will be transmitted to the other Arduino through serial communication.

> **📷 Visit GIF: [Pixel Selection](assets/pixel_selection.gif)**

### Step 2: Enter Opponent's Selection via Serial Monitor

The top-right corner is represented as (0, 0), and the bottom-left corner as (7, 7). First, send the row number followed by pressing enter, then send the column number and press enter again.

> **📷 Visit GIF: [Enter Opponent's Selection](assets/enter_opponent.gif)**

### Step 3: Predict Your Opponent's Choice

Based on the feedback ("hot" if closer, "cold" if farther), make your next prediction.

> **📷 Visit GIF: [Prediction](assets/prediction.gif)**

### Step 4: Enter Opponent's Prediction

If the opponent correctly guesses your selection, send 1; otherwise, send 0 using the serial monitor.

> **📷 Visit GIF: [Enter Opponent's Prediction](assets/enter_opponents_prediction.gif)**