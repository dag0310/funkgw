# funkgw
Easy control of [Intertechno](http://intertechno.at/) radio-LAN gateway devices via UDP sockets.

This example uses 4 commands for controlling shutters (up/down) and a light (on/off), which can be customized as needed.

# Usage
- Upload the files to a web server with PHP support
- Access the [index.html](index.html) from within your LAN
- Press a button to send a UDP command to the gateway

## Customizing commands
- Download [Hercules by HW group](https://www.hw-group.com/products/hercules/index_en.html)
- Go to the UDP tab
- Enter the broadcast IP of your network or the IP of your module for "Module IP" (use an IP network scanner like [Angry IP Scanner](http://angryip.org/download)
- Enter 49880 for "Port" and "Local port"
- Click the "Listen" button
- Execute the command in the Intertechno app and a comma-separated string of data should appear in the "Received data" text area.
- Use this string in [api.php](api.php) and map it to a custom command of yours
- Add controls to the [index.html](index.html) file with the newly added command as parameter for the click event
