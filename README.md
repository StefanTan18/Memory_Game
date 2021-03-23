# Pre-work - *Memory Game*

**Memory Game** is a Light & Sound Memory game to apply for CodePath's SITE Program. 

Submitted by: **Stefan Tan**

Time spent: **6** hours spent in total

Link to project: <https://glitch.com/edit/#!/zinc-jolly-bill>

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
* [ ] Buttons use a pitch (frequency) other than the ones in the tutorial
* [x] More than 4 functional game buttons
* [x] Playback speeds up on each turn
* [x] Computer picks a different pattern each time the game is played
* [ ] Player only loses after 3 mistakes (instead of on the first mistake)
* [ ] Game button appearance change goes beyond color (e.g. add an image)
* [ ] Game button sound is more complex than a single tone (e.g. an audio file, a chord, a sequence of multiple tones)
* [ ] User has a limited amount of time to enter their guess on each turn

The following **additional** features are implemented:

- [ ] List anything else that you can get done to improve the app!

## Video Walkthrough

Here's a walkthrough of implemented user stories:
![](https://i.imgur.com/lyZDvue.gif)
![](https://i.imgur.com/eUKsibY.gif)
![](https://i.imgur.com/BWLYJtO.gif)
![](https://i.imgur.com/hcssQZs.gif)

## Reflection Questions
1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here. 

I used w3schools and Geeks for Geeks to review HTML, CSS, and Javascript as I haven’t coded in those languages in a while. I also looked at Stack Overflow and Google Developer when I was dealing with two separate problems on playing the audio when clicking on the buttons.

2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words) 

A challenge that I encountered when I was creating this submission was having the audio play whenever a button is clicked. This is separate from the problem involving a different browser not supporting AudioContext(). When I first encountered the issue, I was surprised as I was expecting it to work fine as I followed the pre-work instructions perfectly. To overcome it, I know I must first identify the exact issue which is causing the audio not to play. A perfect way to identify the issue is through the use of the JavaScript console. In the JavaScript console, I noticed there was a warning stating, “The AudioContext was not allowed to start. It must be resumed (or created) after a user gesture on the page.” It identified the line number and the file from which this warning originated from. I played around with the code at first and realized after the site loaded a few more times, the audio began playing just fine. This just made me more perplexed as it shows that there wasn’t any problem regarding the instantiating of the AudioContext() and the function that plays the tones. On the JavaScript console, it actually provided a link to a Google Developer page which explained a policy change regarding autoplay. It explained the error clearly, and it advised me to call resume() at some time after the user interacted with the page. I decided to add the resume() function in the guess() function as that was when the user interacts with the page by clicking on the button. Unfortunately, this did not fix the issue completely as the audio only plays after the user clicks the button once. Although this issue may not be completely fixed, I will continue to look for ways to solve it and will update it once I do. 

3. What questions about web development do you have after completing your submission? (recommended 100 - 300 words) 

A question that I have about web development after completing my submission was “How do web developers ensure that the website performs as expected in all the different web browsers that there is?” This question occurred to me as I was having trouble playing audio when clicking a button. I looked over the instructions presented to make sure that I didn’t do anything wrong but to no avail. I narrowed the problem to a line instantiating the AudioContext() with the help of the JavaScript console. I ended up having to search the problem up on the internet where I found out it was due to Safari the browser not supporting it. As not every browser supports the same thing, how do web developers solve this problem? Do they end up having to make a compromise by choosing to work with only the popular browsers or is there a way to circumvent this problem? These were just some of the questions I had while working on this submission.

4. If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words) 

If I had a few more hours to work on this project, I would spend them working to improve the user experience. Clarity is a big priority when it comes to improving the user experience. To make it clear to the user how the game works, I would create a tutorial section as well as a run-through of how the game works through images and/or video. The user will be prompted with the tutorial when they first visit the site, and they are free to visit the tutorial whenever they want after that either by clicking on a button. Another feature that could be added is difficulty levels for the game. To make a more difficult level, the time between each clue can be shortened and the number of buttons and clues can be increased. By giving the user options on how difficult they want the game to be, it will make their experience a lot more enjoyable. The user would be able to freely switch between levels either through buttons or a drop-down menu which both could be added. They could challenge themselves by choosing a more difficult level if they feel like they are able to accomplish their current level with ease.



## License

    Copyright Stefan Tan

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.