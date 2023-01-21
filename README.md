# Enyclopedia Galactica
Despite the title, the project aim is nowhere near creating an online encyclopedia.

The aim is to pay tribute to my favorite author, Isaac Asimov, and his set of novels set in the so-called Foundation universe. A fictional future society. The title reflects that since the novels have an "Encyclopedia Galactica" in the background.

The site is targeted at "newbies" in the Asimovian universe that wants an overview and/or accssible timeline of the rather long series of books (including books by other authors set in the same universe). There will also be some additonal material such as an intro-page, a bibliography, a contact form, and some information about adapations into other media.

The site is entirely written in pure html/css, and can be seen live 
[here](https://jonthorell.github.io/encyclopedia-galactica/)
.

![mockup-picture](https://github.com/jonthorell/encyclopedia-galactica/blob/main/assets/readme-files/multi-website-mockup.png?raw=true)

# Features
## Site-wide
* The site is divided in three distinct areas. A top-bar with the title and a mock-date of when the encyclopedia was published and some copyright information.
The main part of the screen is divided into two columns. The left-hand column is a navigation-bar for the site with some links to social media.
The current page being viewed is highlighted.

![navbar](https://github.com/jonthorell/encyclopedia-galactica/blob/main/assets/readme-files/navbar.PNG?raw=true)

* Every link, site local as well as external, anywhere on the site are aria-label enabled to assist screenreaders. 

* The site is also fully responsive so can easily be used on any
device. To make it easier for devices with lower resolutions, the sidebar is hidden from view and replaced with a hamburger menu when the horizontal resolution drops below 800 pixels.

* Favicon: to make the tab the site is open in easily distinguished, a favicon has been implemented. To keep with the science-fiction and space-theme, a star seemed suitable.

## About (or startpage)
Provides some introductory text and background to the purpose of the site to make it immediately obvious what the site is all about.
![about-page](https://github.com/jonthorell/encyclopedia-galactica/blob/main/assets/readme-files/about.PNG?raw=true)
## Bibliography
Provides the canonical set of novels that Isaac Asimov himself wrote as a part of this future
timeline. This provides a set of must-read novels to make sense of the timeline.
![bibliography-page](https://github.com/jonthorell/encyclopedia-galactica/blob/main/assets/readme-files/bibiliography.PNG?raw=true)
## Timeline
A more-or-less complete timeline. It can be expanded quite a lot, but the general timeline is there. This is the meat of the project
and is what gives both casual and long-time fans of the series a very thorough explantion of the major events of the future history.

![timeline-page](https://github.com/jonthorell/encyclopedia-galactica/blob/main/assets/readme-files/timeline.PNG?raw=true)
## Quotes
A list of some more or less, in my view, funny quotes from Dr Asimov. This is basically to just add some humor to the site. See also the entry below.
![quotes-page](https://github.com/jonthorell/encyclopedia-galactica/blob/main/assets/readme-files/quotes.PNG?raw=true)
## Media
Some information on other media Asimov's novels has been converted into. This, together with the quote-page, was added to the project to make the project seem like a complete website and not sort-of disjointed.
![media-page](https://github.com/jonthorell/encyclopedia-galactica/blob/main/assets/readme-files/media.png?raw=true)
## Contact
Provides a contact-form if the user wants to get in touch with the site-owner with feedback. It doesn't really send anything anywhere, but a website with no form of user-interaction is almost no website at all.
The data entered is validated for errors (such as an empty name field), and sends the user to a thank-you page. It has been validated that the correct data is sent using a test-form, but for now it is better to
just use a basic thank-you page themed the same way as the rest of the site.
![contact-page](https://github.com/jonthorell/encyclopedia-galactica/blob/main/assets/readme-files/contact.PNG?raw=true)

![thank-you page]()
## Testing
Layout has been checked on built-in screen of laptop 1920x1080, on the external display (2560x1440) in Chrome and Edge as well as some "simulated" sizes using devtools. Some problems did not show up on the external display (or the simulated sizes for that matter) but when used on the built-in screen the problems showed up. They were rather superficial in nature and could easily be resolved. Some by enclosing it in an additional div-tag properly styled by css, some because the responsiveness was broken because of syntax errors and the like. Details follows in the list of bugs encountered.
## File names and hierarchy
All file-names are consistently in lower-case and with the appropiate extension (usually .html or .css)
The html-files are in the root-folder
The external files are all located in the assets subfolder. In there you have the folders css, OLD, and pictures.
OLD is not really used. It is there as a "backup" before a hamburger-menu was added so the assessors can see (if they choose to) what the code looked like before I added code that was not my own.
The css-folder contains three files.
1. Style.css is referenced by all html-files
2. Hamburger.css is also referenced by all html-files.
3. The reason for this is to separate code by me (style.css) from those by another (hamburger.css). Credits are included in the files.
4. player.css is only used in media.html so separated from the main style.css for the same reason as #3, and also to avoid potential name-clashes.
# Bugs encountered and fixed
The navigation bar kinda destroyed the layout in lower resolutions. Was fixed by using a hamburger-menu when screensize is 600px and lower. When in those resolutions, the sidenav is hidden from view. NOTE: my knowledge of css is not yet good enough to do that part on my own so the code for that is borrowed and adjusted to suit my site. More details are available in comments in the css-file. Everything regarding css that relates to the hamburger-menu is in the hamburger.css file, to clearly separate my code from someone elses.

The contrast in the bibliography and timeline-pages made it hard to read the text. Fixed by both styling the links-colors to something else as well as adding a intermediary semi-passthru layer between the background image and the table.

The layer mentioned aboved is styled differently on bibliography and timeline. The reason is that the red border used on bibliography suits that page since the two boxes are kinda the opposites of one-another. On the timeline-page though the red border would distract from the flow of the page.

The menu-text at the top of every-page was obscured partially by the top-bar. Fixed by some additional padding (the "About" on the start-page for example). It could have been resolved by removing the text altogether but I found it best to leave it there. That's because the sidebar is removed in lower resolutions so it's not immediately obvious where you are on the site without that piece of text.

The layout was often changing in size which made the site hard to work with. Fixed by adding a div that encompasses the whole page and then applies a width: of 100% to its class. That and additional divs and classes to divide the page
into two columns with some set width and heights in % there as well as some additonal styling for img-elements so they sclae better. The test.html shows the the layout without any distracting extra material. The new column-approach has been added to index.html, bibliography.html and the rest will follow.

The timeline-page borders on information overload. Fixed by adding "details" & "summary" tag popouts to provide further information where necessary (and styled differently so the popout text stands out). I also added a special style in the menubar-tables to indicate clearer which part of the page you're on. In the same manner as the sidebar links, i.e. using a active-class.

The media-page uses an additional included css-file. That's because that pages uses some code from an external source and I wanted to avoid potential name-clashes on pages where those additional classes would not be in use. Not to mention, to make it clear what code was written by me and which was adapted/used from other sources. In the same vein as the hamburger menu that is. So every html-file uses at least two css-files: style.css and hamburger.css. One uses three. Details included in the respective css-file.

The css for "#timeline-table, #timeline-table2, #timeline-table3, #timeline-table4"

might look odd. Why not just use a class instead? At first I used the id-idea to see that I got the style to apply exactly where I wanted it to. Then I thought: why not keep it like that in case I want to style the different parts differently? I ended up not doing that, but the flexibility is there should I want to change it.

The theming for the hamburger-menu looked wrong when page has more info than the test-page (when it was themed to use the same starfield-background as the rest of the pages that is). Removed the background-image to rectify. The test-page is still a part of the project for testing-purposes but is not linked anywhere.

The title-text flows out of the title-bar at lower resolutions. Fixed by some media-queries and altering the font-size of h1. Might be a better way of doing it, but probably involves some javascripting. It seems to work though. The h2 suffered from a similar thing and a media-query that hides it when the resolution is less than 800px wide fixes the problem there.

When resizing the browser-window, images can end up partially covered by the side-bar. An additional div plus removing the sidebar and the left-hand column using diplay:none fixed that problem.

Lighthouse warned about missing width= and height= values in img src. Added.

Lighthouse warned about forgotten aria-label tags, added.

Validation on media.html complained about a deprecation option to iframe and that css should be used instead. The code was borrowed (and properly credited), but I decided to redo it in css instead of the old-fashioned way.
See id #no-iframe-border in style.css.

## Bugs yet unfixed

Timeline page

![error-resize](https://github.com/jonthorell/encyclopedia-galactica/blob/main/assets/readme-files/resize-error.PNG?raw=true)

The main-table with the events is not resized the same way as the menu-tables when the resolution changes. So the page can end up looking like above, which is not how it is supposed to look. The two tables should always
be equal in size horizontally. This was caused by the tags not being closed in the proper order as found by the validator.
When tags had been closed properly the tables aligned correctly horizontally, although instead being pushed underneath the sidenav. Probably due to the wrong classes.

## Validation

Every html-page has been validated as has the css-files. 

index.html, bibliography.html, timeline.html, quotes.html, media.html, contact.html

Line 37,42,39, 41, 77, 43: Element ul not allowed as child of element label in this context. (Suppressing further errors from this subtree.)

Not sure why. The code seems to work, although admittedly the context is in code not by me.

Some cases where the tags were not closed in the proper order that was identified. And fixed.

CSS: No errors found

The various pages has also been checked in lighthouse, and been adjusted according to the warnings the various tools provided.

## Credits

Images found using google-image-search (more precise locations and/or credits can be provided if necessary, although I can not be sure that the site I found the images on are authorative).

Hamburger-menu code:
https://codepen.io/alvarotrigo/pen/ExwgbZv

Youtube no-related-videos-and responsiveness:
https://www.maxlaumeister.com/articles/hide-related-videos-in-youtube-embeds/

Some icono-graphy provided by Font-awsome

https://fontawesome.com/

