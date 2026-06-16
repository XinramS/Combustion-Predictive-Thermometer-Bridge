Requirements
	•	EspHome Builder
	•	MQTT running on Home Assistant
	•	ESP32C6 Board or similar
	•	flashingtoool such as esptool.py
  
Instructions
	•	Get the ssid and password of your Wi-FI
	•	Get your mqtt broker address (address of home assistent)
	•	Get you mqtt username and password
	•	Get the MAC address of your Combustion probe

Fill out the yaml file with the above data.

Compile in ESPHome.

I then downloaded the bin file and flashed using esptool in a terminal window on a Mac:

esptool.py --chip esp32c6 --port /dev/cu.usbmodem14301 --baud 460800 write_flash 0x0 /Users/marnix/Downloads/esp32c6-combustion-bridge.factory.bin

The probe will then appear under MQTT and can be added to your dashboard.

Created using Gemini and Claude
