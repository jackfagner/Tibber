Installation

Step 1: Download the Plugin
1. SSH into your Domoticz server.
2. Navigate to the Domoticz plugins directory:
   cd domoticz/plugins
3. Clone the plugin repository:
   git clone https://github.com/me-processware/Tibber.git
   
Step 2: Install Python Dependencies
1. Navigate to the plugin directory:
   cd Tibber
2. Install the required Python libraries:
   pip3 install -r requirements.txt

Step 3: Restart Domoticz
1. Restart the Domoticz service to load the new plugin:
   sudo systemctl restart domoticz.service

Step 4: Configure the Plugin in Domoticz
1. In the Domoticz web interface, navigate to Setup > Hardware.
2. Add a new hardware device.
3. Select "Tibber 1.01" from the hardware type dropdown list.
4. Enter your Tibber Access Token and other parameters as described below, or test with demo first
5. Click Add.

Configuration

Support Development
If you find this plugin helpful, consider supporting its development. A lot of time and effort has been put into this plugin. I'm not a programmer and had to figure out a lot :) Luckily, my ChatGPT Code Buddy helped me a lot and made it all possible.
Click the link to Donate via PayPal - https://www.paypal.com/donate/?hosted_button_id=SDKNVS3CQ9R4N

Features

- Fetch current price including taxes, minimum power, maximum power, average power, accumulated cost, and accumulated consumption, updated hourly at the start of every hour.
- Fetch today's minimum, maximum, and mean price including taxes.
- Fetch current Power data live if you have Tibber Watty/Pulse installed.

Devices

- Creates a Custom Sensor with name "xxxxx - Price".

How to Get Your Personal Tibber Access Token?

1. Login to create your personal token: https://developer.tibber.com
2. Copy your Tibber Access Token to the field below in the plugin.

Default Tibber Access Token
The default Tibber Access Token is a demo copied from https://developer.tibber.com/explorer.

Parameters

- Tibber Access Token: (Required) The access token for authenticating with Tibber API.
- Home ID: (Optional) The Home ID for the associated Tibber account.
- Create device for Pulse/Watty: (Optional) Option to create a device for Pulse/Watty.
- Enable Logging: (Optional) Option to enable or disable logging.

TODO

- Fix Long Shutdown/Delete Times: Improve the shutdown and deletion process to reduce the time it takes to stop or remove the plugin.
- Type Device Corrections: Ensure that all devices are created and updated correctly.
- Tibber API Compliance: Double-check to ensure that all interactions with the Tibber API follow their guidelines and rules.
  
work in progres:
  - Construct a P1 from Devices: Create a feature that consolidates data from multiple devices into a P1 meter-like functionality.
  - Charging Mechanism: Develop a mechanism that allows users to select the cheapest hours to charge devices such as electric cars, batteries, or other energy storage systems.

tips improvements or additions are welcome please let me know
