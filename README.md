Readme file for the Encyclopedia Galactica Milestone1 project at Code Institute (html/css only).

The title is a bit easy to misinterpret I suppose since the aim is nowhere near creating an online encyclopedia.

The aim is to pay tribute to my favorite author, Isaac Asimov, and the title reflects on that since his Foundation stories have an encyclopedia galactica in the background. Apart from a short about-page about the author himself, the focus will be on creating an accessible timeline of his rather long series of books placed in the same fictional future, using as a wide area of html and css functionality I can cram into it while still adhering to the K.I.S.S acronym.

That is to say, this project borrows from project idea one. The difference is of course that the historical event(s) here are fictional and set far into the future.

Since I am no graphic artist I have "borrowed" images from whereever I could find suitable ones.

Problems encountered. Either by myself or by my mentor.
-------------------------------------------------------

1. The navigation bar kinda destroyed the layout. Was fixed by using a hamburger-menu when screensize is 600px and lower.
2. The contrast in the bibliography and timeline-pages made it hard to read the text. Fixed by both styling the links-colors to something else as well as adding a intermediary semi-passthru layer between the background image and the
table.
3. The layer mentioned aboved is styled differently on bibliography and timeline. The reason is that the red border used on bibliography suits that page since the two boxes are kinda the opposites of one-another. On the timeline-page though the red border would distract from the flow of the page.
4. The menu-text at the top of every-page was obscured partially by the top-bar. Fixed by some additional padding.
5. The layout was often changing in size which made the site hard to work with. (hopefully) fixed by adding a <div> that encompasses the whole page and then applies a width: of 100% to its class.
7. The timeline-page borders on information overload. Fixed by adding <details><summary> popouts to provide further information where necessary (and styled differently so the popout text stands out). I also added a special style in the menubar-tables to indicate clearer which part of the page you're on.
7. Two pages (contact and media) uses more than one included css-file. That's because those pages uses some code from external "libraries" and how-tos and I wanted to avoid potential name-clashes on pages where those addition classes would not be in use.
8. The css for 
    #timeline-table, #timeline-table2, #timeline-table3 #timeline-table4 {
        border: 1px;
        width: 80%;
        margin-left: 10%;
        margin-right: 10%;
    }

    might look odd. Why not just use a class instead? At first I used the idea to see that I got the style to apply exactly where I wanted it to. Then I thought: why not keep it like that in case I want to style the different parts differently? I ended up not doing that, but the flexibility is there.
