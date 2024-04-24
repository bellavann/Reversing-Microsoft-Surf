# Reversing-Microsoft-Surf
## Reverse Engineering Microsoft Edge's "Let's Surf"

## Code Credits
Code was originally gathered from https://github.com/jackbuehner/MicrosoftEdge-S.U.R.F.

### These features were added to the original S.U.R.F. (and then turned off by me) by Jack Buehner:
- Removed access to Ski Theme
- Removed game theme selector

## How to Run:
Need to download Node.js to set up a local server that will allow the index.html file to open and access the other files on the local machine.
There will be specific issues with CORS enbaled images without the server.

### In CMD:
cd edgesurf (Make sure all files are located in this directory.)
node server.js

### In browser:
http://localhost:3000/index.html
Should pull up modified surf.

### Changes Made:
- Changed surfTheme to "Let's surf - RevEng"
- Changed background to be half purple in honor of Kali purple. various lines, interface.css
- Made it so Kraken takes a life, but does not end game. (Kraken follows you after.) 9579. surf.bundle
- Under getGameCreditsModalBody, added my name
- Also added name to specialThanks
#### When game restarts
- Changed Max Lives and Current # to 5: 529+530, surf.bundle
- Set Current Boosts to 3: 534, surf.bundle
- Made it so that the game does not end even after all of the lives are gone (there are 2 invisible lives): 8710, surf.bundle
