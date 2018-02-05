# Personal Training Notes

## Screen Casting
Quicktime offers a quick and easy way to capture the screen. 
* File
* New screen recording
* Press red record button
* Select area or whole screen
* Commence recording
* Press grey stop button or stop via menu. 
* Save file - edit if necessary.


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

## Genesis Fonts
//* Enqueue Lato Google font
add_action( 'wp_enqueue_scripts', 'sp_load_google_fonts' );
function sp_load_google_fonts() {
	wp_enqueue_style( 'google-font-lato', '//fonts.googleapis.com/css?family=Lato:300,700', array(), CHILD_THEME_VERSION );
}
