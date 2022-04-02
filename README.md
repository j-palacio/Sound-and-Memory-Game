# Pre-work - *Memory Game*

**Memory Game** is a Light & Sound Memory game to apply for CodePath's SITE Program. 

Submitted by: Juan Palacio

Time spent: 10 hours spent in total

Link to project: (insert your link here, should start with https://glitch.com...)

## Required Functionality

The following **required** functionality is complete:

* [x] Game interface has a heading (h1 tag), a line of body text (p tag), and four buttons that match the demo app
* [x] "Start" button toggles between "Start" and "Stop" when clicked. 
* [x] Game buttons each light up and play a sound when clicked. 
* [x] Computer plays back sequence of clues including sound and visual cue for each button
* [x] Play progresses to the next turn (the user gets the next step in the pattern) after a correct guess. 
* [x] User wins the game after guessing a complete pattern
* [x] User loses the game after an incorrect guess

The following **optional** features are implemented:

* [x] Any HTML page elements (including game buttons) has been styled differently than in the tutorial
* [x] Buttons use a pitch (frequency) other than the ones in the tutorial
* [x] More than 4 functional game buttons
* [x] Playback speeds up on each turn
* [x] Computer picks a different pattern each time the game is played
* [x] Player only loses after 3 mistakes (instead of on the first mistake)
* [ ] Game button appearance change goes beyond color (e.g. add an image)
* [ ] Game button sound is more complex than a single tone (e.g. an audio file, a chord, a sequence of multiple tones)
* [x] User has a limited amount of time to enter their guess on each turn

The following **additional** features are implemented:

* [x] Rolling high score tracker
* [x] Volume slider


## Video Walkthrough (GIF)

If you recorded multiple GIFs for all the implemented features, you can add them here:

![Stop and Start game button](https://i.imgur.com/SK73leq.gif)

![Winning the game](https://i.imgur.com/VNYLgsA.gif)


![3 Mistakes and Game over features](https://i.imgur.com/URRio2n.gif)

![](gif4-link-here)

## Reflection Questions
1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here. 

• Codecademy: HTML, CSS, and JavaScript fundamentals
• StackOverflow: info on dynamically changing html paragraph text, setTimeout and setInterval
• GitHub: reviewed other code bases to help debug my code and learned how to implement the optional mistake feature.


2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words) 

The most difficult part of this submission was creating the countdown timer that would give the player a set amount of time to repeat the pattern. I wanted a timer that was: 1) visible to the player, 2) would end the game if it hit 0, but reset at the start of each round, and 3) wouldn’t start counting down until the sequence was done playing, so that the user would always have 20 seconds to enter their guesses. The first item I wanted to tackle was the syntax for dynamically changing html text so that it would be visible to the player. Luckily, I was able to find the answers on Stack Overflow and GitHub.  However, implementing the next two tasks to create the countdown timer was not as straightforward. Following an example from W3schools, I used a count variable to tack the number of times countDown() is called and make sure the countDown function is set to be run in an interval of 1000ms and called 20 times.  The most difficult part was knowing where to place setInterval and clearInterval in a logic circuit. I wasn’t able to terminate the countDown() function in some cases and ran into an infinite loop even though I applied clearInterval(). I tried to debug by setting up breakpoints using console.log () and found that my clearInterval() was called correctly. I also searched for possible solutions on many different forums. And eventually, one suggestion worked! When I put an extra clearInterval() before calling setInterval(), I was able to terminate the countDown() in the correct time. I realized that the cause of this bug might be that I was calling several setInterval() and countDown() at the same time as I modified guess() and stopGame() to reset countDown() and start over again at a new turn of guessing. After all this I kept receiving a parsing error that stumped me and my game stopped working. In the end, while searching for a way to debug my code, I stumbled upon a StackOverflow post that said to create a setTimeout() that recursively called a secondary setTimeout(). By setting the first one to have a delay equal to the longest note, and the second one to have a 1 second delay, I was able to create the timer that I wanted. I spent a lot of time debugging this feature and other features, but these challenges helped to better understand how functions were called. l learned how to create a web app using HTML, CSS, and JavaScript. Most importantly, it has given me more confidence in tackling similar projects.

3. What questions about web development do you have after completing your submission? (recommended 100 - 300 words) 

I found using glitch to create this project was very efficient because of its file structure. The tutorial was easy to understand and follow along with. However, when I try to add more features, the project becomes more difficult to complete, and a simple parsing error can stop your application from working. Therefore, for larger projects would it not be more efficient to use an IDE like Visual Studio Code? And would it be more logical to use React to compile the different files? Also, I wonder how much more efficient it would be to test the functionality of my code in an IDE like Visual Studio Code compared to Glitch? How can you use VSC to make a web application? Lastly, how do you implement a back-end into an HTML, CSS, and JavaScript project?

4. If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words) 

If I had a few more hours to work on this project, I would spend more time adding some additional features such as changing the styling of the title of the game to a 3-D font. I would add images to the game buttons and change the color of the general background. Next, I would implement different game button sounds. Rather than a single tone, I would apply an audio file or try to get the sequence to play out some sort of series of notes. I would likely require an already existing database of what pitch each note is at, or I would have to manually figure it out/create a program to parse the sounds. I would also clean up some of the functions in my JavaScript file. I would insert comments, so everyone and I would know what each bit of code does. Lastly, I would spend more time reading through my code to better understand and be able to implement sound synthesis functions in future projects as well as help improve my fundamentals in HTML, CSS, and JavaScript for future projects.


## Interview Recording URL Link

[My 5-minute Interview Recording](https://youtu.be/MghzrrQviHo)


## License

    Copyright [Juan Palacio]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.