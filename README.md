[README.txt](https://github.com/user-attachments/files/33172271/README.txt)
# skate-64
made this with claude opus 5.5 and i made some with hand love yall


Skate 64 - development build 0.2.0-dev6

PLAY.bat            Starts the game in Castle Grounds.
BUILD_ENGINE.bat    Builds the engine with Skate 64's additions: Mario Mode on M, and keyboard
                    play. Run it once (it needs Rust, which this PC has). The first build
                    compiles the whole engine and takes a long while. PLAY.bat then uses it.

What PLAY.bat does the first time:
  1. Your Super Mario 64 ROM and your Skate 3 disc image are checked. Neither is changed.
  2. Every level of the game is built from your ROM into data\maps (they stay on this PC).
  3. The Skate 3 engine prepares the skater, animations, physics and maps from your Skate 3
     disc image. Its own setup window opens and starts by itself. This is the slow part.
     It needs internet once, and several GB of free disk space while it works.
  4. The game starts in Castle Grounds.

Mario is the skater: on the board you see Mario, on Skate 3's own board, doing what the
Skate 3 skater does. His model is read from your ROM into data\maps each time you play.

The whole game is there: walk or skate up to the castle's doors to go in, jump into a
painting to go to its course, use the pipes and holes. Doors inside a level are simply open.
A level takes a few seconds to load. Levels have their ground, walls and water, but none of
the game's enemies, coins, stars or moving platforms.

Keys once BUILD_ENGINE.bat has run (an Xbox-style controller works too):
  M                 switch between Skate Mode and Mario Mode
  W A S D           left stick: steer and lean on the board; run as Mario
  Arrow keys        right stick: tricks on the board (hold Down, then tap Up, to ollie);
                    turn the camera as Mario
  Space             A: push on the board; jump as Mario
  Left Ctrl         B: brake on the board; punch as Mario
  Left Shift        X: push with the other foot; punch as Mario
  F                 Y: get off / on the board
  Q / E             left / right trigger: grabs; crouch as Mario
  Z / C             LB / RB; crouch as Mario
  Backspace         leave the level you are in (back to the castle, by its painting);
                    on a controller, hold Back for a second
  Esc               the engine's menu

sm64.dll is Super Mario 64's own movement code (the open libsm64 project) built for this PC.
It reads Mario from your ROM. It is for this PC only and is not part of anything published.

Reports are written to data\logs.
