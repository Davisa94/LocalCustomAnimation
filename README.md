# LocalCustomAnimation

A file for loading a custom animation

Usage:
Place the wrapper.html and the test.js in the same folder along with your animation. Rename the animation as alert_animation.* where * is the file extension.

Within OBS or Streamlabs create a new browser source and select the box that says Local File:
![](image/README/1630882127918.png)

then select the wrapper.html as the local file.

Then ensure that the two checkboxes are checked:

* Shutdown source when not visible
* Refresh browser when scene becomes active

![](image/README/1630882337567.png)

Hide the source and go to Streamer.bot.

Within Streamer.bot Create 2 Actions:

1. a new action that changes the contents of test.js to the latest event text and then call action 2
2. and then create another action which

* Shows the source you just made
* Add a delay that allows the animation to complete playing
* Hide the source.

3. Go to the events tab and select Action 1 as the action to occur when the desired event occurs.
