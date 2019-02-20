# mqtt_tree

As I didn't found a light wight way to keep an overview of all topic published from various devices I wrote a small python UI.

## Installation
* install the paho-mqtt module e.g. via pip:
  * `pip install paho-mqtt`
* copy all files from this repo e.g. via git
  * `git clone ....`

## Setup
as this is in a really early stage setup is a little bit rough.
Change the line `self.connect("haus.wupp", 1883, 60)` in file `mqtt_client.py` to your needs. For option check the paho documentation.

## Run
`python mqtt_tree.py` should do the job.

### How it looks like
![mqtt_tree](https://user-images.githubusercontent.com/6035034/53057173-831a3f00-34ae-11e9-8a76-a66edc996c21.png)

nothing fancy, just an overview.

### How it works

It subscribes '#', means any topic and keep listening for changes and new topics, while in parallel feeding to received topics in the treeview of an very basic TKinter Application.
It doesn't "forget" any Topics while running, which makes it useful to monitor, whats there only temporary.

Feedback, Issues, Suggestions, Improvements, Forks all welcome. Use the Issue tracker here to get in contact. 
