# Personal Training Notes

A random collection of notes for things that I may not remember how to do if I don't attempt them for a long time.

## Screen Casting
Quicktime offers a quick and easy way to capture the screen. 
* File
* New screen recording
* Press red record button
* Select area or whole screen
* Commence recording
* Press grey stop button or stop via menu. 
* Save file - edit if necessary.

## Video Podcasting
Methods described during the MMU Digital Skills Training by Phil Swire

BB Flashback Pro 4, Powerpoint and Sound Recorder software, available on all MMU Windows machines
- Record
- Select region to control which area of the screen is captured to avoid including open tabs and clock etc.
	- Do not select sound. Quality for sound is better if captured as a separate audio file and added.
	- Do not select web cam, unless you specifically wish to record yourself.
- Select Tools
	- Options
		- Moving Video with max quality and 30 frames per second
- Record video
It is recommended to practice first to make the overall effect smoother and more professional.
- Select Open in player 
- Select Automatically in Playback
- To remove or change the yellow highlight cursor
	- select effects
		- highlight colour
- After editing
- File 
	- Export
		- wmv (for windows)

Sound Recorder to capture audio
- Press start recording and stop at the end.

Use PowerPoint to create video
Embed videos and sound files to slides and use transitions to move through them. 
- Insert audio
	- from my pc 
- Insert video
	- from my pc
- Opt to play across slides
- use transitions to set the timing of the slide change to slightly longer than the audio or video embedded 
- Via advanced slide
	- Select no full screen to stop the presentation flipping to full screen. It also allows room to add additional text.
Export video 
- File
	- Export
		- Select presentation quality
			- Create Video




## GitHub
**PULL** down from GitHub
**PUSH** up to GitHub

## Visual Studio Code
* Datestamp - SHIFT CMD i

## Linux Commands
* **pwd** Print Working Directory (Tells you where you are)
* **ls** List (Prints a list of the files in the current directory)
* **cd** Change Directory (changes directory to the one you specify)

## Mac Stuff
* **Hashtag** - Alt 3
* **Screenshot** - shift cmd 4 then select the area you wish to capture by clicking and dragging. An image of the screen will appear on your Desktop.

##WordPress
### Themes 


## WordPress - Genesis
### Google Fonts
functions.php edit *(or duplicate and edit)* the wp_enqueue_style relating to fonts. Genesis themes usually already include at least one Google Font. 

### Genesis Featured Image
<<<<<<< HEAD
/*claire featured image code for posts* consider editing location */
=======
#### Original version - only works with posts
/*claire featured image code* consider editing location/
>>>>>>> 21c0f7bc35345b33336deafa577d658dc8533e80
add_action ('genesis_before_entry', 'fcd_add_featured');
function fcd_add_featured() {
if ( is_single() && has_post_thumbnail() ) {
echo '<div class="home-thumbnail">' . '';
genesis_image( array( 'size' => 'full' ) );
echo '</div>';
}
}

<<<<<<< HEAD
/* Alternative Code to Display Featured Image on top of the post */
add_action( 'genesis_entry_content', 'featured_post_image', 8 );
function featured_post_image() {
  if ( !is_singular( array( 'post', 'page' ) ))  return;
	the_post_thumbnail('large'); /*you can use medium, large or a custom size */
}
=======
#### Works with posts and pages
//featured image code for posts and pages* consider editing location/
add_action ('genesis_before_entry_content', 'fcd_add_featured');
function fcd_add_featured() {
if ( is_singular() && has_post_thumbnail() ) {
echo '<div class="home-thumbnail">' . '';
genesis_image( array( 'size' => 'full' ) );
echo '</div>';
}
}


Return alternative system code
>>>>>>> 21c0f7bc35345b33336deafa577d658dc8533e80

### Genesis Child Themes - creation
#### Theme Folder
Theme folder **must** contain the following:
functions.php
style.css

Ideally should also include an image 
* Create an image called screenshot (or presumably whatever suits) and save it in the theme's root folder. 

### Creating Colums in Genesis
<div class="one-third">
		<p>
		column 1
	</p>
</div>
<div class="one-third">
	<p>
		column 2
	</p>	
</div>
<div class="one-third">
	<p>
		column 3
	</p>
</div>


### Team Plugin *used with signol*
Shortcode used for TBC plugin to display specific posts from only a certain team on a website which has several contributors. 

[display-posts category="team-2" order="DESC" include_content="true"]

## Linking Source Tree to a GitHub Repo
1. Open GitHub and login
2. Open the repo you wish to clone
3. 
3. Select clone or download
4. Copy the URL to the clipboard
5. Open Sourcetree
6. Select clone from URL
7. Paste in the URL you copied from GitHub
8. Select the location on your local machine that you would like the repo to appear in **must be an empty folder** 
9. The repo from GitHub will now be cloned to your local machine and local commits can be made and pushed to GitHub using Sourcetree.

Learnt how to reset my changes so that they don't get sent to the repo. Find the file in the list of files in staging, right click and reset

## Ionic App Dev
In terminal (on mac) create a directory and enter it

ionic start --type=ionic1

give it a name (no spaces etc)

no cordova at this stage
no SDK at this stage

select app format


ionic serve - run an existing project (you have to be in the folder at the time)

ctrl c stops things
ctrl Z pauses things
% restarts things you've paused

open . Opens the folder for that project with the files in finder

## Node Red 
Run Node Red from terminal by typing node-red

Open the browser at http://localhost:1880
This will show the flows you are running / creating. 



## Pi Notes

The operating system for a pi needs to be set up on an SD card before you can use the pi

Shutting down a Pi before shutdown is not straight forward. 

### To Change  Pi Password
Ctrl Alt & F1
login - username
Passwd - will let you change your password, but asks for existing one first


## Screenly OSE
[Screenly](https://www.screenly.io/ose/) is a way to run on-screen displays using a Raspberry Pi. 
The most straight forward way is to download a Screenly version of the Raspberry Pi operating system (known as an image) and use that version. 

Flash an SD card using [Etcher](https://etcher.io/) or something similar this will clear the SD card of anything and add the new information. 
Add the SD card to the Raspberry pi and connect it to a screen via HDMI, a keyboard using a USB port, an ethernet connection and a power supply. 

The Raspberry Pi will now boot up and display a screen from screenly with the details of its IP address and a password. Visit the IP address as a url on a computer and it will bring up the Screenly content management system where you can add the assets you wish to display eg videos, pictures etc. By default the asset list will include a Clock, A Weather widget and a Hacker News stream and they will appear on the screen attached to the Raspberry Pi and loop through for approx 10 seconds each. 

You can switch the various assets on and off. Select Add Asset to upload your content to the system. 

The screen attached to the Pi will continue to loop through any available content. 

Double check that the content hasn't been allocated an end date for display. 


### Node-Red

Can use a Pi to run Node-Red *notes based on DigiLabs Set Up of Pi*

Run the Pi through the terminal 

ssh pi@pi

Means that the terminal is now running the Pi and the cursor will switch to Pi@raspberrypi:~$

node-red-start starts node when it runs off the Pi *this is due to the changes we had to make for the version of the operating system*

Open the browser at pi:1880 

This will show the flows you are running / creating.

To view the dashboard if you've created one or have an input area *e.g. for the twitter search thing where you have to include a search term* open the browswer at pi:1880/ui

If you are running a flow using the worldmap node open the browser at -  pi:1880/worldmap


### Screens
Screens lets you run extra screens that won't be interupted if the connection drops. 

screen creates a new screen

screen -ls *lists the screens running*

screen -r followed by the number displayed in the list *will switch to that particular screen*



##Websites of Interest

* theyworkforyou.com
* ifthisthenthat.com
* 

### Raspberry Pi Configuration Updates
Used for things such as updating the password and changing the time on a Pi

sudo raspi-config *using super user powers to update the configuration of the Pi*
Updating the time is linked to the localisation. If the pi doesn't know it's in the UK it won't display the correct time, especially during BST. Updates require restarting the Pi which appears to reset the time - requires more info




####Update Pi Password

CTRL Alt F1 *opens terminal*
login *name of pi*
Passwd

*default is: login pi pw raspberry*



 worklog entry 2018-01-30 15:23:29
## Creating 'Squared' in Markdown and / or HTML
As DH2 is actually DH² attempted to find out how to 'write' that. Thanks to Dave I know now about Unicode which is accessed via Ctrl Cmd  and Spacebar 

## Spotlight
Macs have a search facility other than finder called Spotlight which you access by pressing cmd and the space bar.

## Genesis 404 page wip
The DH2 site is running a genesis child theme. The live theme is dh2-parallax-pro named after the Genesis child theme that the customised child theme is based upon. 

The default 404 page isn't particularly attractive and is in the process of being customised. 

I have included a custom 404 error image created on Canva and some additional text which i have added through a customised widget which i created. For some reason this method is resulting in the selected widgets disappearing from the widgets panel whenever that page is refreshed although the widgets chosen continue to work on the 404 page. 

Will investigate further before full roll out. 

## LED Curtain
### Create video
Create the asset (gif file or movie) on the Legend app or alternative software. The finished item should beeither an AVI or a GIF file, with AVI being the preferred option. The video / gif will be rendered at **96 x 80 pixels** (each light on the LED curtain is one pixel) 

### Deploy to Curtain
The curtain is controlled by the Toshiba Windows laptop.

Open LED Show T9 program
*Cartoon cats - The system will display a window containing cartoon cats offering help - they won't help you, even if you try as the options for help don't work.*

Select the green cross to Add blank page

Control Page - this affects the size of the 'window' The size needs to be set to 96 x 80 and the position of the window also needs to be updated otherwise the curtain will try to display a portion of the display and almost certainly in the wrong place.

Select the green cross to Add file window

Select Add video or Add Gif, depending on the format you are trying to display. 

Make sure that everything plays as you wish (press play?) and select Save As. This will save the file and details. The system will then display a player and you can close the laptops lid. The LED Curtain will continue to display in your absence. 

##Google Analytics
Hierarchy is Organisation
Account
Property
View

### Google Analytics Reporting
Rename the automatically created view as Raw Data and don't mess with it. This provides a way to get back to previous information.

Create a new view called Master View

Create a third view called Test and use this to try out new views and reports etc. 

### To exclude internal traffic by IP address
Filters
Add filter to view
Predefined
select exclude traffic from IP address
Select equals
add my IP address
Save

### Reporting
Customisation
Dashboards
Create
Select private or shared

## Gatsby
This is to create a site locally created with Gatsby

Open terminal and enter the directory you'd like to create the site in. 
gatsby new name-of-new-gatsby-site
cd name-of-new-gatsby-site/
gatsby develop
Site will now be visible at http://localhost:8000
To edit open the files in vs code and open src/pages/index.js The site will update in real time. 
The site won't be visible if you close vs code. To restart it, you need to return to the directory holding the site and type gatsby develop.