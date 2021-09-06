# LocalCustomAnimation

A file for loading a custom animation

Usage:
# File Setup
Place the wrapper.html and the test.js in the same folder along with your animation and optional sound file. Rename the animation as alert_animation and the sound file as alert_sound.

Within the HTML file "wrapper.html" Ensure that you change the filetype for your video and audio as follows:

If your video is MP4 instead of webm change these lines:
`        <!-- EDIT ONLY BELOW IF THE ANIMATION IS NOT A WEBM --> <source src="alert_animation.webm" type="video/webm"> <!-- ONLY EDIT ABOVE -->`
To look like :
`        <!-- EDIT ONLY BELOW IF THE ANIMATION IS NOT A WEBM --> <source src="alert_animation.mp4" type="video/mpeg"> <!-- ONLY EDIT ABOVE -->`

and if your audio is mp3 instead of m4a change these lines:
`        <!-- EDIT ONLY BELOW IF AUDIO IS NOT m4a --> <source src="alert_sound.m4a" type="audio/mpeg"> <!-- ONLY EDIT ABOVE -->`
to look like this:
`        <!-- EDIT ONLY BELOW IF AUDIO IS NOT m4a --> <source src="alert_sound.mp3" type="audio/mpeg"> <!-- ONLY EDIT ABOVE -->`

# Streaming Software Setup

Within OBS or Streamlabs create a new browser source and select the box that says Local File:
![](image/README/1630882127918.png)

then select the wrapper.html as the local file.

Then ensure that the two checkboxes are checked:

* Shutdown source when not visible
* Refresh browser when scene becomes active

![](image/README/1630882337567.png)

Next, to be able to hear the alert go off if there is a sound:

* Ensure that the "Control audio via OBS" checkbox is checked within the source properties as well
* ![](image/README/1630900845829.png)
* Go into the Sources advanced audio properties:
* ![](image/README/1630900954396.png)
* Ensure that the dropdown on the far right reads: "Monitor and Output"
* ![](image/README/1630901004801.png)
* If you dont see it in the list ensure the source is visible first and try again.

Now when the alert goes off you should be able to hear it

Test it out by hiding and showing the source.

Now hide the source and go to Streamer.bot.

# Streamer.Bot Setup

Within Streamer.bot Create 2 Actions:

1. a new action that changes the contents of test.js  using the format:
   `var latest = "%user% Just Followed you!";`
   As shown below:
   ![](image/README/1630903015455.png)**Ensure that the checkbox that says "Append to file" is UNCHECKED**
2. call action 2 Which you make below
3. and then create another action which

* Shows the source you just made
* Add a delay that allows the animation to complete playing
* Hide the source.

4. Go to the events tab and select Action 1 as the action to occur when the desired event occurs.

   If you just want to import the actions use this import:
   `TlM0RR+LCAAAAAAABADNVk1vnDAQvVfqf0Ar5RZHBgzYqXpoEqVqVVVRG/VSchjbw2YjPrYGsllF+e+1IdslbFqVqiuFw4JnhmHm+c3z3r9+5XmzWzT1oipnx55/2BlKKNCuZp8qBflpWzdV8a5cFNC4qD4ElFvUNuq7W3vefX+zroV279KYhwFNQhLzSBAW05gI5JxknEaCBYmO4qjP1b30o8XWfbNs83xrxRJkji5fY1rc2jcFnld5Xq0uzWI+RzPINjdVu3QBl1g39cAB+QrW9ZfWNZtBXg9yGii17bPra9erqlK1xmDZ7Pp2sHiCRxeSLfKu4LPjND2rVFvYRHWaXpjqBpV7+npyeg2NrJqt6RH4HE2Tpo1t5Ohm0EqXtsE7V8/sFoyXg4vx3nrp7KCt0Rx4H20C78xUyyVqD7xzaLwesHT2ZpQIbEypd1ob7GcmMPGjUBElJBJGA0mEH2rCAkyE3eJAgB4lXeFifu3qo0d0VPd66eAIn1o3u/aEA30JpcY7l2hrfTj8Hda3kHdU8ikdfbaAu2+PzpGn3/w/9R+KAHUUJESGcWD7F5qAzwSJQ0aVllxpClP7txUGUyHw/waCnpEfusJ9iTrhTBKpqCIs8RnhmcxIkCjJORM+5Tgq3LTlh6JAbRmVr8fDN8CEA0gaICfAosgygVEiuJ9ZitCMMwjCSIupmLCpgAQDQDaPV+PhfO/SdBN6NZzpPIdljXrg7Z0bZMeiNg3LfxS1ixzW3dS/ZEGrFZb4eXNOYFN7VrjmBorRftdVa9SvwBNTreqhUvcxjSXa7kzaCkscEJk+XuSZn801e46mWcxEHEhOEsrs6KJKiLCHEImZn4BQLGJ0unTRqTydpl3sv4qXjoCCa14o4IRl1DI4EIpomYUSo4xBEr8Y8doHtfw9UYsLGoeZPRUZ05QwsFogfcoIU/bvTURj6odjcd0DtfYige7WR/Y6tnE+/AQs2qL5NQoAAA==`

# Follow Me
Feel free to follow me on twitch to see me code projects live and occasional gaming.
http://twitch.tv/melonlore