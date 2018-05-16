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

After the bomb has been disarmed, it has to be moved to a 'Quarantine' separated from the maze. On placing the bomb here, the participant will be awarded points. Please see the 'Gameplay' section for more details on the scoring system.

https://raw.githubusercontent.com/arc-bphc/arc-iot/master/maze.png

# Bot specifications

## Technical Specifications

* Max Size: 350mm x 300mm x 300mm (l x b x h)
* Max Weight: 5kg
* Max Operating Voltage: 12V
* Power Supply Unit: Onboard battery (Li-Po, Li-Ion NiMH, NiCd, or Lead-acid)
* Wireless Communication: 2.4 GHz RF, WiFi, Bluetooth, NRF, or ZigBee can be used

## Other Requirements
* Commercially available ready-made robots are not allowed.
* Each team is allowed to have only one robot.
* The robot may be autonomous or manually controlled. If manually controlled, the bot must be controlled over either a wired or a wireless connection
* The robot must have an appendage for lifting and placing the bomb or pulling and pushing the bomb. This can be any mechanical setup.
* There are no restrictions on the sensors. However, to complete the competition, each robot must have a WiFi module and an RFID scanner onboard.

# Gameplay
Each bomb has four possible states:

* Armed - the initial state of the bomb.
* Disarmed - when the RFID tag of a bomb has been scanned but the bomb has not been Defused. The bomb can only be moved in this state.
* Defused - when the bomb has been successfully placed in the quarantine area after being Disarmed.
* Exploded - happens when the bomb has been moved when in an Armed state. This will result in a penalty. The bomb cannot be Defused after this.


## Individual Round

The robot will start from a box in the Arena. The participant must ensure that their robot is connected to the competition's WiFi network. The bombs and RFID tags will be placed by the competition organisers in the Arena.

The robot must go to an RFID tag in the Arena. This must be scanned by the robot to set the status of the bomb to Disarmed. On scanning the RFID tag, a display will show the number of the bomb to be Defused. This bomb must be moved to the quarantine area within 90 seconds of scanning the RFID tag. On placing the bomb in the Quarantine area, the bomb will be marked as Defused and points will be awarded for the same.

In case the player is not able to move the bomb to the Quarantine area in time, the bomb will explode and a penalty will be imposed on the team. No points will be awarded to the team after it explodes.

The bomb must not be moved till it is Disarmed (by scanning the corresponding RFID tag). In case it is moved before Disarming, the bomb will explode and a penalty will be imposed.

Each team gets a total of 5 minutes in the Arena to get as many points as they can.

### Scoring System

* Bomb defusal and Quarantining: 50 points


### Penalty

* Bomb Explosion: -30 points and the bomb cannot be defused again


## Knockout Round

After the individual rounds for all the teams are completed, the top four teams are selected for the Knockout Round.

The rules regarding bomb defusal are the same as in the Individual round. However, in the Knockout Round, two teams play at once.

One team gets 5 minutes to place the bombs in the Arena and the other team gets 5 minutes to defuse these bombs as per the rules in the Individual round. After this, the teams placing the bombs and defusing the bombs are reversed and the game is played again. The team with the highest cumulative score of setting and defusing wins.

The organizers of the competition will decide the number of bombs for the team to place in the Arena. The number of each type of bombs will be the same in both rounds.

All the bombs will initially be kept in the Bomb Quarantine part of the Arena and the team placing the bombs must lift the bombs and place it in the Bomb Maze part of the Arena. The team setting the bombs must follow these instructions:

1.Read any unscanned RFID tag on the arena.
2.Pick up a bomb from the Quarantine area using the robot.
3.Place the bomb in any of the pre-defined bomb drop areas on the competition Arena. Only one bomb may be placed in a given drop area. The RFID tag assigned to this bomb is the one scanned in step 1. Hence, only one bomb can be assinged to each RFID tag.
4.Repeat from step 1 until there is no more time left or there are no more bombs left in the Quarantine area.

The progression of the top four teams in the Knockout round is as follows:

### Scoring System

Placing Bombs
* Points awarded = Number of Bombs left after the round is over x 50 points
Defusing Bombs
* Quarantining: 50 points
### Penalty
Placing Bombs
* No penalties
Defusing Bombs
* Bomb Explosion: -30 points and the bomb cannot be defused again
# Rules and Guidelines
The organizers reserve the right to change any of the above said rules, at any time. Changes will be notified on the website and Facebook page. It is the participant’s responsibility to stay updated.

## Setup Time
* The participants will get 10 minutes of setup time for calibration and testing prior to the competition, according to a schedule that will be made available at the start of the event.
* Ensure that all of the vehicle's sensors, especially the WiFi module and wireless control are working properly.
* The bot must be placed in the starting point on the Arena, at the beginning of each round.
## Competition
* Before the start of a round, one participant from each team should be selected for controlling the robot. Only one person is allowed to control the robot until the round is completed.
* Participants will not be permitted to enter the Arena or touch any of the bombs inside or outside the Arena, during a match.
*  A robot can only move one bomb at a time.
* The robots can come in contact with the walls but should not damage it.
* Participants should not dismantle their robots before the competition results are announced as the robots might need to be checked by the organizers at a later stage to ensure that the participants have not violated any of the rules.
* In case of any dispute, the verdict of the judges is final.
## Disqualification
A team may be disqualified due to, but not limited to the following:

* The robot fails to meet any of the criteria in the Bot Specifications section.
* The robot damages a bomb when moving it.
* The participating team is not ready in time for the start of their turn.
* The robot damages the Competition Arena.

# Paritcipation
* Participants can register in teams of 1-4 people.
* Students from different educational institutes can form a team.
* All participants must have a valid ID card from their educational institute.