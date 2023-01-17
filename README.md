# Enyclopedia Galactica
Readme file for the Encyclopedia Galactica project at Code Institute (html/css only).

Despite the title, the project aim is nowhere near creating an online encyclopedia.

The aim is to pay tribute to my favorite author, Isaac Asimov, and his set of novels set in the so-called Foundation universe. A fictional future society. The title reflects that since the novels have an "Encyclopedia Galactica" in the background.

The site is targeted at "newbies" in the Asimovian universe that wants an overview and/or accssible timeline of the rather long series of books (including books by other authors set in the same universe). There will also be some additonal material such as an intro-page, a bibliography, a contact form, and some information about adapations into other media.

The site is almost entirely written in pure html/css with some javascript in there.

# Features
For now the site consists of 6 pages. At the top of the page a banner will always be there to make sure there is no mistaking what site you're on as well as showing copyright information. On the left-hand side there will always be a navigation bar with links to the other parts of the site (and highlighting which you're currently on) as well as links to social media. Both will adapt to different resolutions.

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