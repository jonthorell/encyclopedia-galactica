
Readme file for the Encyclopedia Galactica Milestone1 project at Code Institute (html/css only).

The title is a bit easy to misinterpret I suppose since the aim is nowhere near creating an online encyclopedia.

The aim is to pay tribute to my favorite author, Isaac Asimov, and the title reflects on that since his Foundation stories have an encyclopedia galactica in the background. Apart from a short about-page about the author himself, the focus will be on creating an accessible timeline of his rather long series of books placed in the same fictional future, using as a wide area of html and css functionality I can cram into it while still adhering to the K.I.S.S acronym.

That is to say, this project borrows from project idea one. The difference is of course that the historical event(s) here are fictional and set far into the future.

Since I am no graphic artist I have "borrowed" images from whereever I could find suitable ones.

Layout has been checked on built-in screen of laptop 1920x1080, on the external display (2400x3000)
as well as some "simulated" sizes. Some problems did not show up on the external display but when
used on the built-in screen the problems showed up. They were rater superficial in nature and
could easily be resolved.

Problems encountered. Either by myself or by my mentor.
-------------------------------------------------------

1. The navigation bar kinda destroyed the layout. Was fixed by using a hamburger-menu when screensize is 600px and lower. NOTE: my knowledge of css is not yet good enough to do that part on my own so the code for that is borrowed and adjusted to suit my site. More details are available in comments in the css-file. Everything regarding css that relates to the hamburger-menu is in the hamburger.css file, to clearly separate my code from someone elses.
2. The contrast in the bibliography and timeline-pages made it hard to read the text. Fixed by both styling the links-colors to something else as well as adding a intermediary semi-passthru layer between the background image and the
table.
3. The layer mentioned aboved is styled differently on bibliography and timeline. The reason is that the red border used on bibliography suits that page since the two boxes are kinda the opposites of one-another. On the timeline-page though the red border would distract from the flow of the page.
4. The menu-text at the top of every-page was obscured partially by the top-bar. Fixed by some additional padding.
5. The layout was often changing in size which made the site hard to work with. (hopefully) fixed by adding a <div> that encompasses the whole page and then applies a width: of 100% to its class.
7. The timeline-page borders on information overload. Fixed by adding <details><summary> popouts to provide further information where necessary (and styled differently so the popout text stands out). I also added a special style in the menubar-tables to indicate clearer which part of the page you're on. In the same manner as the sidebar links, i.e. using a active-class.
7. Two pages (contact and media) uses more than one included css-file. That's because those pages uses some code from external "libraries" and how-tos and I wanted to avoid potential name-clashes on pages where those addition classes would not be in use. Not to mention, to make it clear what code was written by me and which was adapted/used from other sources. In the same vein as the hamburger menu that is. So every html-file uses at least two css-files: style.css and hamburger.css. Two uses three.
8. The css for 
    #timeline-table, #timeline-table2, #timeline-table3 #timeline-table4 {
        border: 1px;
        width: 80%;
        margin-left: 10%;
        margin-right: 10%;
    }

    might look odd. Why not just use a class instead? At first I used the id-idea to see that I got the style to apply exactly where I wanted it to. Then I thought: why not keep it like that in case I want to style the different parts differently? I ended up not doing that, but the flexibility is there should I want to change it.
9. The theming for the hamburger-menu looked wrong when page has more info than the test-page. Removed the background-image to rectify. The test-page is still a part of the project for testing-purposes but is not linked anywhere.
10. The title-text flows out of the title-bar at lower resolutions. Fixed by some media-queries and altering the font-size of h1. Might be a better way of doing it, but probably involves some javascripting.
11. When resizing the browser-window, images can end up partially covered by the side-bar. An additional div fixed that problem.



