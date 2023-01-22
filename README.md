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

![topbar](https://github.com/jonthorell/encyclopedia-galactica/blob/main/assets/readme-files/topbar.PNG?raw=true)

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
As can be seen, there are parts marked with a ">" sign. That can be clicked to reveal further information.

Like this:

![foldout](https://github.com/jonthorell/encyclopedia-galactica/blob/main/assets/readme-files/foldout.PNG?raw=true)

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

The form consists of:
* Name (type text, required)
* E-mail (type email, required)
* Question if the user had heard of Isaac Asimov before or not (type radio, required)
* Improvement suggestions (type textarea, not required)
* A clear-form button (button type, reset)
* A submit-button (button type, submit)

![contact-page](https://github.com/jonthorell/encyclopedia-galactica/blob/main/assets/readme-files/contact.PNG?raw=true)



![thank-you page](https://github.com/jonthorell/encyclopedia-galactica/blob/main/assets/readme-files/thank-you.PNG?raw=true)


# Technologies used

* HTML (for validation results, see further down) was used for the structure of the website.
* CSS (for validation results, see further down) was used (in external css-files for the most part. More details under filenames further down) to style the site.
* Gitpod as IDE. Sometimes with notepad++ on the side to easier see several areas of the code simultaneously.
* Git from inside gitpod and Github for deployment. 
* GIMP for some basic image-resizing
* Font awsome for social-media images as well as the thumbs-up and thumbs-down icons used on the timeline page.

# Deployment

All code was entered into its respective file from within Gitpod. 

The source is hosted on github and deployed using git pages and the commands:

* git add .
* git commit -m "Commit message"
* git push

# Testing

## Responsiveness
Layout has been checked on built-in screen of laptop 1920x1080, on the external display (2560x1440) in Chrome and Edge as well as some "simulated" sizes using devtools. Some problems did not show up on the external display (or the simulated sizes for that matter) but when used on the built-in screen the problems showed up. Most were rather superficial in nature and could easily be resolved. Some by enclosing it in an additional div-tag properly styled by css, some because the responsiveness was broken because of syntax errors, incorrectly targeting the wrong class or id, and the like. Details follows in the list of bugs encountered. One had me stumped for quite a while though. In lower resolutions, text tended to get cut of at the right-hand side and not everything would be displayed.

Now after the bugs have been squashed the site responds to different screen-sizes as intended and no errors as far as I can see when it comes to stretched images, overflow issues, nor elements stacked on top of eachother.

## Functional testing

### Links
All links has been clicked to make sure they take you where they are supposed to, both internally to the site (navbar and internally within primarily the timeline page where there are id-anchors present) was well as to wikipedia, twitter, and so on. With or without target="_blank".

### Form

There is only one form. On the contact-page. As of now, it is not doing anything. It just re-directs the user to thankyou.html with a generic thank-you message with no feedback on what you had entered in the form. However, during development another page was used that did provide that feedback. It was used for debugging-purposes to make sure the correct data was sent to the server. The code is still there (commenteded out) in the contact-form if one wants to take a look.

Some of the fields in the form are set to be of a required type and that they can not be empty. That can still be checked even with the generic thankyou.html used as the "active" part. It is impossible to get to it if you leave the name blank, does not provide a valid e-mail (well, one that conforms to the standard user@domain.com format at any rate), or clicks one of the radio-buttons. Works as intended in other words.

# File names and hierarchy
All file-names are consistently in lower-case and with the appropiate extension (with the exception of pictures, either .html or .css)
The html-files are in the root-folder
The external files are all located in the assets subfolder. In there you have the folders css, OLD, and pictures.
OLD is not really used. It is there as a "backup" before a hamburger-menu was added so the assessors can see (if they choose to) what the code looked like before I added code that was not my own.
The css-folder contains three files.
1. style.css is referenced by all html-files
2. hamburger.css is also referenced by all html-files.
3. The reason for this is to separate code by me (style.css) from those by another (hamburger.css). Credits are included in the files.
4. player.css is only used in media.html so separated from the main style.css for the same reason as #3, and also to avoid potential name-clashes.

# Comments on css

Not a bug, but something I think needs to be explained. In style.css you can find this:

```css
#timeline-table,
#timeline-table2,
#timeline-table3,
#timeline-table4 {
  /* styles the different "era" tables on timeline page */
  border: 1px;
  width: 80%;
  margin-left: 10%;
  margin-right: 10%;
}
```
It might look odd. Why not just use a class instead? At first I used the id-idea to see that I got the style to apply exactly where I wanted it to. Then I thought: why not keep it like that in case I want to style the different parts differently? I ended up not doing that, but the flexibility remains there should I want to change it.

# Bugs encountered and fixed

1. The navigation bar kinda destroyed the layout in lower resolutions. Was fixed by using a hamburger-menu when screensize is 800px and lower. When in those resolutions, the sidenav and the lefthand column is hidden from view. NOTE: my knowledge of css is not yet good enough to do that part on my own so the code for that is borrowed and adjusted to suit my site. More details are available in comments in the css-file. Everything regarding css that relates to the hamburger-menu is in the hamburger.css file, to clearly separate my code from someone elses.

2. The contrast in the bibliography and timeline-pages made it hard to read the text. Fixed by both styling the links-colors to something else as well as adding a intermediary semi-passthru layer between the background image and the table.

3. Not a bug per se, but a layout issue. The layer mentioned aboved is styled differently on bibliography and timeline. The reason is that the red border used on bibliography suits that page since the two boxes are kinda the opposites of one-another. On the timeline-page though the red border would distract from the flow of the page. The same style could have been used, I just felt it was better to make some adjustments.

4. The menu-text at the top of every-page was obscured partially by the top-bar. Fixed by some additional padding (the "About" on the start-page for example). It could have been resolved by removing the text altogether but I found it best to leave it there. That's because the sidebar is removed in lower resolutions so it's not immediately obvious where you are on the site without that piece of text.

5. The layout was often changing in size (meaning: the responiveness was not perfect) which made the site hard to work with. First fix was by adding a div that encompasses the whole page and then applies a width: of 100% to its class. 
That was not enough though. It needed a re-factoring of the layout. The main part of the page is now always in two strict colums. One left-hand side (a div, 20% in width) containing the navbar. Another div on the right, 80% in width-size.
A no-frills test.html exist to show the basic layout after the re-factoring.

6. The timeline-page borders on information overload. Fixed by adding "details" & "summary" tag popouts to provide further information where necessary (and styled differently so the popout text stands out). I also added a special style in the menubar-tables to indicate clearer which part of the page you're on. In the same manner as the sidebar links, i.e. using a active-class.

Here it can be see what the expand means:

![expand](https://raw.githubusercontent.com/jonthorell/encyclopedia-galactica/ecc57ac2d4af34e65e550e3978f1d7fc21a6d53c/assets/readme-files/html-validation/expand.PNG)

And the addtional styling:

![table-styling](https://github.com/jonthorell/encyclopedia-galactica/blob/main/assets/readme-files/styling-table.PNG?raw=true)

7. Not really a bug per se, but an explanation. The media-page uses an additional included css-file. That's because that pages uses some code from an external source and I wanted to avoid potential name-clashes on pages where those additional classes would not be in use. Not to mention, to make it clear what code was written by me and which was adapted/used from other sources. In the same vein as the hamburger menu that is. So every html-file uses at least two css-files: style.css and hamburger.css. One uses three. Details included in the respective css-file.

8. The theming for the hamburger-menu looked wrong when page has more info than the test-page (when it was themed to use the same starfield-background as the rest of the pages that is). It had been styled with the same stars background image as the rest of the site, but that made the links next to impossible to read no matter what font color used. Removed the background-image to rectify. (The test-page is still a part of the project for testing-purposes but is not linked anywhere).

9. The title-text flowed out of the title-bar at lower resolutions. 

![title-bar](https://github.com/jonthorell/encyclopedia-galactica/blob/main/assets/readme-files/topbar.PNG?raw=true)

Fixed by some media-queries and altering the font-size of the top line. Might be a better way of doing it, but probably involves some javascripting. It seems to work though. 
The second line suffered from a similar thing and a media-query that hides it when the resolution is less than 800px wide fixes the problem there.

10. When resizing the browser-window, images could end up partially covered by the side-bar. 
An additional div, removing the sidebar and the left-hand column using diplay:none plus refactoring the entire code into fixed (in percentage) into two columns fixed that problem and responsiveness issues in general.
The test-page used to come up with how the code should look to implement two columns can be found here:

[test-page](https://jonthorell.github.io/encyclopedia-galactica/test.html)

11. The two columns do not cover all screen-estate in height on purpose. The bottom part was left out as a fix to an annoying bug: the end of the body-tag was cut off and it could not be scrolled down to reveal it no matter what the overflow: settings were set to.

12. Lighthouse warned about missing width= and height= values in img src. Added.

13. Lighthouse warned about forgotten aria-label tags, added.

14. Validation on media.html complained about a deprecation option to iframe and that css should be used instead. The code was borrowed (and properly credited), but I decided to redo it in css instead of the old-fashioned way.
See id #no-iframe-border in style.css.

15. The main-table with the events is not resized the same way as the menu-tables when the resolution changes. So the page can end up looking like below, which is not how it is supposed to look. The two tables should always
be equal in size horizontally. This was caused by the tags not being closed in the proper order as found by the validator.
When tags had been closed properly the tables aligned correctly horizontally, although instead being pushed underneath the sidenav. The refactoring into two-column mode fixed that problem.

![error-resize](https://github.com/jonthorell/encyclopedia-galactica/blob/main/assets/readme-files/resize-error.PNG?raw=true)

# Bugs yet unfixed

## Timeline page

An error caused by a ul nested beneath a label, which apparently is not allowed. See under html-validation for details.

# Validation

Every html-page has been validated as has the css-files. 

## HTML

All files were validated using [v3 validator](https://validator.w3.org/)
All together 8 files, 7 being in use on the site and one test file.

![index.html](https://github.com/jonthorell/encyclopedia-galactica/blob/main/assets/readme-files/html-validation/html-index-result.PNG?raw=true)
![bibliography.html](https://github.com/jonthorell/encyclopedia-galactica/blob/main/assets/readme-files/html-validation/html-bibliography-result.PNG?raw=true)
![timeline.html](https://github.com/jonthorell/encyclopedia-galactica/blob/main/assets/readme-files/html-validation/html-timeline-result.PNG?raw=true)
![quotes.html](https://github.com/jonthorell/encyclopedia-galactica/blob/main/assets/readme-files/html-validation/html-quotes-result.PNG?raw=true)
![media.html](https://github.com/jonthorell/encyclopedia-galactica/blob/main/assets/readme-files/html-validation/html-media-result.PNG?raw=true)
![contact.html](https://github.com/jonthorell/encyclopedia-galactica/blob/main/assets/readme-files/html-validation/html-contact-result.PNG?raw=true)
![thankyou.html](https://github.com/jonthorell/encyclopedia-galactica/blob/main/assets/readme-files/html-validation/html-thankyou-result.PNG?raw=true)

A few notes on those images. As can be seen, it is the same error in all of them. The "offending" code comes from the hamburger-menu code I borrowed and adapted for this site.
Unfortunately, I did not notice the problem early enough or I might have been able to find a solution to the issue. As it is, there are two options:

  * Remove the offending code. Which, unfortunately, will make the responsiveness of the site to suffer.
  * Leave it as-is for now.

The code works, even though with an error from the validator, so I opted to leave it for now. Not optimal so something to add to the to-do list.

Compare it with index2.html. The same as index.html except that the hamburger-menu code has been removed (this is the test-file mentioned). And here there are no
errors.

![index2.html](https://github.com/jonthorell/encyclopedia-galactica/blob/main/assets/readme-files/html-validation/html-index2-result.PNG?raw=true)

The other note is: as can be seen by the screenshots, I have uploaded the html-file into the validator.

The reason for that is: the online-checker with URL is not trustworthy.

My site has been deployed to github pages. BUT when I tried to use a URL from there to validate against I got a lot more errors regarding classes and mismatched tags for things I have not written or even seen.
It seems the URL input functionality of the validator drags in additonal css/html files that are unrelated to my project.

Or rather: it did that on first try. Now it seems to mostly work as intended. It could not access my bibliography.html page so I still do not trust it fully though. The erros and what not that are relevant are the same though so it should not matter.
The html-files that I did upload to the validor are included as they were at the time in the html.zip file.


## CSS

All files were validated using

[jigsaw](https://jigsaw.w3.org/css-validator/)

Currently offline. Earlier versions of the files were validated as 100% correct, but I did not take screenshots then since it was still very much a work-in-progress. As of now I can not get new results.

## Lighthouse

All pages have been run through lighthouse with similar results. To begin with, the settings used were:

![settings](https://github.com/jonthorell/encyclopedia-galactica/blob/main/assets/readme-files/lighthouse/default.PNG?raw=true)

Here are the reports, and some comments below.

Index

![index](https://github.com/jonthorell/encyclopedia-galactica/blob/main/assets/readme-files/lighthouse/index.PNG?raw=true)

Bibliography

![bilbiography](https://github.com/jonthorell/encyclopedia-galactica/blob/main/assets/readme-files/lighthouse/bibliography.PNG?raw=true)

Timeline

![timeline](https://github.com/jonthorell/encyclopedia-galactica/blob/main/assets/readme-files/lighthouse/timeline.PNG?raw=true)

Quotes

![quotes](https://github.com/jonthorell/encyclopedia-galactica/blob/main/assets/readme-files/lighthouse/quotes.PNG?raw=true)

Media

![media](https://github.com/jonthorell/encyclopedia-galactica/blob/main/assets/readme-files/lighthouse/media.PNG?raw=true)

Contact

![contact](https://github.com/jonthorell/encyclopedia-galactica/blob/main/assets/readme-files/lighthouse/contact.PNG?raw=true)

Thank you

[thankyou](https://github.com/jonthorell/encyclopedia-galactica/blob/main/assets/readme-files/lighthouse/thankyou.PNG?raw=true)

First off, I do not pay much attention to the performance score since it fluctuates a little but has never dropped below 98%. And a lot of the tips lighthouse has provided in how to improve that value are things I have little to no control over since I do not
control the webserver as such.



# To-do

1. Fix the bug regarding the hamburger-menu so all files are considered error-free as far as the validator goes.
2. Create a proper submit-script so the data is actually sent somewhere as well as making the thankyou.html able to acknowledge the data that was sent.
3. Improve the color-contrast

# Credits

Images found using google-image-search (more precise locations and/or credits can be provided if necessary, although I can not be sure that the site I found the images on are authorative).

Hamburger-menu code:
[codepen](https://codepen.io/alvarotrigo/pen/ExwgbZv)

Youtube no-related-videos-and responsiveness:
[maxlaumeister](https://www.maxlaumeister.com/articles/hide-related-videos-in-youtube-embeds/)

Some icono-graphy provided by 
[fontawsome](https://fontawesome.com/)

