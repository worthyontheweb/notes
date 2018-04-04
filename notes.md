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
- use transitions to set the timing of the slode change to slightly longer than the audio or video embedded 
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
* Hashtag - Alt 3
* Screenshot - shift cmd 4 then select the area you wish to capture by clicking and dragging. An image of the screen will appear on your Desktop.

##WordPress
### Themes 


## WordPress - Genesis
### Google Fonts
functions.php edit *(or duplicate and edit)* the wp_enqueue_style relating to fonts. Genesis themes usually already include at least one Google Font. 

### Genesis Featured Image
/*claire featured image code*/
add_action ('genesis_before_entry', 'fcd_add_featured');
function fcd_add_featured() {
if ( is_single() && has_post_thumbnail() ) {
echo '<div class="home-thumbnail">' . '';
genesis_image( array( 'size' => 'full' ) );
echo '</div>';
}
}

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
3. Select clone or download
4. Copy the URL to the clipboard
5. Open Sourcetree
6. Select clone from URL
7. Paste in the URL you copied from GitHub
8. Select the location on your local machine that you would like the repo to appear in **must be an empty folder** 
9. The repo from GitHub will now be cloned to your local machine and local commits can be made and pushed to GitHub using Sourcetree.

