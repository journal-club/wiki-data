<!-- TITLE: Bomb Squad -->
<!-- SUBTITLE: The bombs have been planted. Can your robot save the day? -->

# Competition Arena
The Arena will consist of two areas:

## Bomb Maze
* The bombs in the Arena are scattered throughout a maze.
* This maze is open from the top and can be seen by the participants controlling the bot.
* The bombs are ABS cylinders of diameter 4.5cm and height 7cm. The bombs are labelled with number.
* The bomb may only be moved when it has been disarmed.
* The bomb maze section has several RFID tags scattered throughout it, each of which correspond to one bomb.
* The RFID tags are placed on the ground of the arena. The bot's design should be planned accordingly.
* The robot must scan this RFID tag (13.56 MHz) to disarm the bomb.
* The width of any route in the maze is at least 450mm.

The robot is to scan an RFID tag and send the value scanned off the tag to a server over a local WiFi network provided by the competition organisers. The robot must make a GET request in the form of <ip_address>/<secret_key>/<rfid_value>. The secret_key and ip_address will be provided on the day of the competition. Hence, an example of a such a request will be 192.168.1.100/mysecretkey/71939123002.

The server will validate whether the RFID scanned is correct, and if it is, the bomb number to be quantined will be displayed on a screen.

# Bomb quarantine

