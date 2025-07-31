<img width="391" height="65" alt="Hexavore" src="https://github.com/user-attachments/assets/d653607c-b5eb-41de-987f-6ab36786857c" />

A browser-based real-time puzzle game created with JavaScript, HTML, and CSS.

## Overview
Built upon qualitative research and an emphasis on UX design fundamentals, *Hexavore* is a visually and sonically engaging gaming experience.

Each level features a unique puzzle based around a hex-grid. Players must overcome both static and randomly generated obstacles in order to reach the goal hex and win the level.

The player's fastest times are also recorded on a leaderboard accessed at the end of the final level. Through bombs, shockwaves, and goblins galore, can you race against against the clock to beat 
your best time and win the game?

## Design and Usage
1. ***MAKE SURE AUTOPLAY IS ENABLED (REFRESH AFTER ENABLING) IN YOUR BROWSER IN ORDER TO HEAR THE MUSIC.***
2. As a front-end application with no server or database, *Hexavore* can be played locally by simply opening the index.html file in any web broswer after cloning or saving this repository.
3. Each level is designed in a separate HTML file with inline JavaScript. All of the CSS styling for each level of the game is pulled from styles.css.
4. To begin, the user must click the starting hex (yellow triangle) until it reaches its darkest blue color state. Clicking on it at that point will cause it to "pop" and expand blue to the surrounding tiles,
   which are now "claimed", allowing the process to be repeated.
5. There are multiple obstacles in the user's way, which include:
     - **Walls:** Grey tiles, pre-arranged for each level, cannot be claimed or directly destroyed, user must move around them
     - **Leaves:** Green tiles, randomly spawn on hex-grid, cannot be claimed, user must click on them to destroy them and progress
     - **Bombs:** Red tiles, randomly spawn on hex-grid, cannot be claimed, clicking on them causes the bomb to "explode" and reset every tile around it (including claimed tiles), does not destroy walls
     - **Towers:** Purple tiles, spawn at center of level, cannot be claimed or destroyed, intermittently release a shockwave that destroys leaves and sets each claimed tile back to its previous state
     - **Goblin:** Final boss of game, randomly hops around the hex-grid and resets claimed tiles to unclaimed if the goblin lands on them, can be killed by blowing up a bomb while the goblin is on or next to it
6. The user must navigate through each level and obstacle in order to get to and claim the goal hex (orange triangle), progressing them to the next level.
7. Upon winning, the user will see their fastest times recorded on the leaderboard. The user can replay the game to try to beat their time.
8. The hex-grid was implemented using a map data structure, with all of the interactivity being designed around event listeners/handlers. Every obstacle (except walls) were implemented using asynchronous timing
   functions, and local browser storage is used to ensure continuity in the background music and keep track of the user's times.
9. Animations and visuals were implemented using CSS keyframes (except the goblin, which was a frame-by-frame animated GIF).

## Example
<img width="1790" height="872" alt="gameplay" src="https://github.com/user-attachments/assets/4be65463-13b6-4296-82df-896a11fd53bc" />
