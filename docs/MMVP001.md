# Micro MVP 001

In this version the user:
- Can acess the page localhost/test_mvp_001
- The page will show data about two players 
- The user will play for the two players
- The game starts with each player having 100 Live Points
- There will be only attack rounds and the first round is the Player 1 time to attack.
- There will be only one button that causes a random number of LP be subtracted from the oponent.
- Once the attack was done, its the oponnents round.
- The game ends when a LP of any player become less than 1.

# Tech Solution

- [ ] Install a brand new Laravel app
- [ ] Install "Inertia" for the front-end
- [ ] Change the "Welcome" page for the HTML version of the project landingpage
- [ ] Create the route, controller and blank page to the url "/test_mvp_001"
- [ ] Create a fixed layout (HTML only) with:
    - LP of the players
    - Signal to show wich player is atacking
    - Button to attack
    - Message for the end of the Match telling wich player won.
- [ ] All the logic has to be in the backend
- [ ] The front end will only show the data and send the "attack" signal
