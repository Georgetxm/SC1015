# Accessible Tic Tac Toe

## Access the deployed version of the application [here](https://ttt-frontend-pink.vercel.app/)
Enter a game ID on 2 browsers and start playing agaisnt each other.
## Both the Frontend and the Backend have to run for the application to work.
## Instructions to Start the Frontend

1. Clone the repository with `git clone https://github.com/Georgetxm/ttt-frontend`
2. Run `npm install` or `yarn install` to install the packages for frontend
3. Run `npm start ` or `yarn start` to start the React project on the local machine
## Instructions to Start the Backend

1. Clone the repository with `git clone https://github.com/Georgetxm/ttt-backend`
2. Run `npm install` or `yarn install` to install the packages for frontend
3. Run `npm start ` or `yarn start` to start the Express Server on the local machine   
# Design Decisions
When designing for the accessible the application’s colours were chosen to be contrasting so that the visually impaired is able see. This is based on the contrast ratio that attains the WCAG AAA standards (8.37:1). The application was also created to be accommodating to a screen reader user.

To keep the app simple, the user is first greeted with just a input and a “join” room button. After joining a room, the user will be told to wait till a second player enters. Then the game starts, for accessibility the movement to each cell’s button can be done with a keyboard (tab key) and be screen readable to tell the position (e.g. “top right”). An announce board button is used to tell users the state of the board.   
# Infrastructure
The frontend of the application was built on React and the backend with Express. Socket.IO was used to handle the game communications back and forth with the server (emit and on events). It is also used to ensure that each room does not have more than 2 players. Both the frontend and backend are deployed on Platform-as-a-Solution (PAAS) platforms for convenience and speed purposes.
# Improvements / Planned to-dos
1. Annoucement of the board status with a socket listener after every move.
2. Improved UI
3. Replay feature
4. Exit room
5. Win Counters
