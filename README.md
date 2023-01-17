# Enyclopedia Galactica
Readme file for the Encyclopedia Galactica project at Code Institute.

Despite the title, the project aim is nowhere near creating an online encyclopedia.

The aim is to pay tribute to my favorite author, Isaac Asimov, and his set of novels set in the so-called Foundation universe. A fictional future society. The title reflects that since the novels have an "Encyclopedia Galactica" in the background.

The site is targeted at "newbies" in the Asimovian universe that wants an overview and/or accssible timeline of the rather long series of books (including books by other authors set in the same universe). There will also be some additonal material such as an intro-page, a bibliography, a contact form, and some information about adapations into other media.

The site is almost entirely written in pure html/css with some javascript in there.

# Features
For now the site consists of 6 pages. At the top of the page a banner will always be there to make sure there is no mistaking what site you're on as well as showing copyright information. On the left-hand side there will always be a navigation bar with links to the other parts of the site (and highlighting which you're currently on) as well as links to social media. Both will adapt to different resolutions.

"Always" on the left-hand side is not quite true. When the screen-resolution is lower than 600px wide, it gets replaced by a hamburger-menu.

For additonal clarity for newbies, "pop-outs" has been enabled so you get at ">" where an additonal comment may be necessary.

Every html-page has been validated as has the css-files. The various pages has also been
checked in lighthouse, and been adjusted according to the warnings the various tools
provided.



## About
Provides some introductory text and background.
## Bibliography
Provides the canonincal set of novels that Isaac Asimov himself wrote as a part of this future
timeline.
## Timeline
A more-or-less complete timeline. It can be expanded quite a lot, but the general timeline is there.
## Quotes
A list of some more or less, in my view, funny quotes from Dr Asimov.
## Media
Some information on other media Asimov's novels has been converted into.
## Contact
Provides a contact-form if the user wants to get in touch with the site-owner with feedback.
## Testing
Layout has been checked on built-in screen of laptop 1920x1080, on the external display (2400x3000)
as well as some "simulated" sizes using devtools. Some problems did not show up on the external display (or the simulated sizes for that matter) but when used on the built-in screen the problems showed up. They were rather superficial in nature and could easily be resolved. Some by enclosing it in an additional div-tag properly styled by css, some because the responsiveness was broken because of syntax errors and the like. Details follows in the list of bugs encountered.
## File names and hierarchy
All file-names are consistently in lower-case and with the appropiate extension (usually .html or .css)
The html-files are in the root-folder
The external files are all located in the assets subfolder. In there you have the folders css, javascript, OLD, and pictures.
OLD is not really used. It is there as a "backup" before a hamburger-menu was added so the assessors can see (if they choose to) look what the code looked like before I added code that was not my own.
The javascript folder contains one script, referenced by the contact-page. It was NOT written by me but was added to provide some mean of re-sizing the input form. Details in css-file and under credits.
The css-folder contains four files.
1. Style.css is referenced by all html-files
2. Hamburger.css is also referenced by all html-files.
3. The reason for this is to separate code by me (style.css) from those by another (hamburger.css). Credits are included in the files.
4. input.css and player.css are only used in contact.html and media.html respectively. They are also separated from the main style.css for the same reason as #3, and also to avoid potential name-clashes.
# Bugs encountered and fixed
The navigation bar kinda destroyed the layout in lower resolutions. Was fixed by using a hamburger-menu when screensize is 600px and lower. NOTE: my knowledge of css is not yet good enough to do that part on my own so the code for that is borrowed and adjusted to suit my site. More details are available in comments in the css-file. Everything regarding css that relates to the hamburger-menu is in the hamburger.css file, to clearly separate my code from someone elses.

The contrast in the bibliography and timeline-pages made it hard to read the text. Fixed by both styling the links-colors to something else as well as adding a intermediary semi-passthru layer between the background image and the table.

The layer mentioned aboved is styled differently on bibliography and timeline. The reason is that the red border used on bibliography suits that page since the two boxes are kinda the opposites of one-another. On the timeline-page though the red border would distract from the flow of the page.

The menu-text at the top of every-page was obscured partially by the top-bar. Fixed by some additional padding (the "About" on the start-page for example). It could have been resolved by removing the text altogether but I found it best to leave it there. That's because the sidebar is removed in lower resolutions so it's not immediately obvious where you are in the page without that piece of text.

The layout was often changing in size which made the site hard to work with. (hopefully) fixed by adding a div that encompasses the whole page and then applies a width: of 100% to its class.

The timeline-page borders on information overload. Fixed by adding "details" & "summary" tag popouts to provide further information where necessary (and styled differently so the popout text stands out). I also added a special style in the menubar-tables to indicate clearer which part of the page you're on. In the same manner as the sidebar links, i.e. using a active-class.

Two pages (contact and media) uses additional included css-files. That's because those pages uses some code from external "libraries" and how-tos and I wanted to avoid potential name-clashes on pages where those additional classes would not be in use. Not to mention, to make it clear what code was written by me and which was adapted/used from other sources. In the same vein as the hamburger menu that is. So every html-file uses at least two css-files: style.css and hamburger.css. Two uses three. Details included in the respective css-file.

The css for "#timeline-table, #timeline-table2, #timeline-table3, #timeline-table4"

might look odd. Why not just use a class instead? At first I used the id-idea to see that I got the style to apply exactly where I wanted it to. Then I thought: why not keep it like that in case I want to style the different parts differently? I ended up not doing that, but the flexibility is there should I want to change it.

The theming for the hamburger-menu looked wrong when page has more info than the test-page. Removed the background-image to rectify. The test-page is still a part of the project for testing-purposes but is not linked anywhere.

The title-text flows out of the title-bar at lower resolutions. Fixed by some media-queries and altering the font-size of h1. Might be a better way of doing it, but probably involves some javascripting. It seems to work though.

When resizing the browser-window, images can end up partially covered by the side-bar. An additional div fixed that problem.

## Bugs yet unfixed

Timeline page

The main-table with the events is not resized the same way as the menu-tables when the resolution changes.

## To-Do

Add alt="Whatever" to all links in nav-menu (hamburger and on screen)

## Credits

Images found using google-search (more precise locations and/or credits can be provided if necessary, although I can not be sure that the site I found the images on is authorative).

Hamburger-menu code:
https://codepen.io/alvarotrigo/pen/ExwgbZv

Input-resize code:
https://codepen.io/shshaw

Youtube no-related-videos-and responsiveness:
https://www.maxlaumeister.com/articles/hide-related-videos-in-youtube-embeds/

Some icono-graphy provided by Font-awsome

https://fontawesome.com/





