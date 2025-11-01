# reception_autoamtion
 * Ultrasonic Sensor Relay Control for Arduino Uno
 *
 * This code reads the distance from an HC-SR04 ultrasonic sensor.
 * If an object is detected *closer* than a set threshold (e.g., 400 cm),
 * it will activate a relay.
 *
 * TIMER LOGIC:
 * 1. When an object is detected, the relay turns ON and a 15-minute timer starts.
 * 2. If another object is detected *during* that 15 minutes, the timer resets to 15 minutes.
 * 3. If 15 full minutes pass *since the last detection*, the relay will turn OFF.
  


* WIRING GUIDE: (Same as before, pins are the same on Uno)
 * * Arduino Uno    |   Component
 * ---------------------------------------
 * 5V             ->   HC-SR04 VCC pin
 * 5V             ->   Relay Module VCC pin
 * GND            ->   HC-SR04 GND pin
 * GND            ->   Relay Module GND pin
 * Pin D12        ->   HC-SR04 TRIG pin
 * Pin D11        ->   HC-SR04 ECHO pin
 * Pin D7         ->   Relay Module IN (Input) pin




* !!! SAFETY WARNING - MAINS VOLTAGE !!!
 * Be extremely careful if your relay is switching high voltage (like 110V/220V AC).
 * - Always disconnect power before working on high-voltage wiring.
 * - Ensure no exposed wires.
 * - If unsure, ask a professional electrician for help.
 * - This code assumes an "Active LOW" relay module (common type).
 * This means sending a LOW signal turns the relay ON, and HIGH turns it OFF.
 */
