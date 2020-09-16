ezLuckyDrawer
=======
ezLuckyDrawer is a trivially simple JQuery "Slot Machine Construction Kit". Its only dependencies are jQuery and the jQuery Easing library. It can be allowed to run randomly or to go to a pre-specified .

Minimal Usage
-----
    <link href="ezslots.css" rel="stylesheet" type="text/css" />
    <script src="jquery-1.11.3.js"></script>
    <script src="jquery.easing.1.3.js"></script>
     <fetch() JSON Data from an sample json database file >
    <script src="slot.js"></script>
    
 
Understanding the Code
----------------------
The code starts with the pattern as storing "this" in a private variable "that". It then sets member variables with a mix of values from the options map and hard-wired defaults.

The init function is defined but only called once the other member functions are set. It creates the appropriate number of window/reels.

The CSS suggest the structure ezslots generates:

    .ezslots>.window>.slider>.symbol>.content

* ezslots - a class assigned to the containing div
* window - refers one of the reel-viewing windows
* slider - this is the part that actually moves.
* symbol - container for a single symbol that will show up in the window
* content - where the symbol actually "lives" (needed for horizontal and vertical centering)
* Data - i had used json data from an api to fetch the winner details .
*winner - winner is shown using a modal
Heights and width are manually and redundantly applied to ensure consistency with the animation.

Also, each reel window is given the class "window_#" where # is its position in the ezslots div.

