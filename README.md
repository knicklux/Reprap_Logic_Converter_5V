# Reprap_Logic_Converter_5V
This small PCB can be used to make life with common Reprap Z_Probes easier by converting the 12V/24V sensor logic to 5V logic.

Steps:
 * read this README to the end
 * wiring
 * configure Marlin (pullup resistors)
 * test

Pins:

Hold the PCB so you can read the input numbers X4, X3 and X2.

X4: Sensor Interface
	Left: 	Signal
	Middle:	GND
	Right:	12V or 24V

X3: PCB Power supply
	Left:	GND
	Right:	12V or 24V

X2: 5V Logic Output
	Left:	GND
	Right:	5V logic Sensor output, pullup required

Wiring:

Always pay attention to pin assignment! 

1) Connect the Sensor to X4

2) Connect 12V or 24V from your PSU to X3

3) Connect X4 to your RAMPS/Rumba/Rambo (your printer's mainboard in general) Z_Min signal (s) and ground (-)

Marlin:

Enable Z-Endstop pullup in Configuration.h:
  #define ENDSTOPPULLUP_ZMIN

Test:

Better safe than sorry, test carefully and with care. Helpul commands: M119, M48
