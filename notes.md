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

### Team Plugin *name tbc*
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

