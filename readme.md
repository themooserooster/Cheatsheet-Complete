# Creating a Hacker Cheatsheet

## Intro

We're going to use this cheatsheet to memorize 11 commands on 3 different topics you'll see again and again:
* General Keyboard Shortcuts. These will literally work just about anywhere on a computer.
* Navigating Folders in the Command-Line. These will save your life one day. Like soon.
* Committing Your Work with Git. This is how programmers protect and share all the code they write.

You will use these so many times that one day you will do all these things without even thinking about it. That day is not today, so we're going to create a cool-looking cheatsheet that we can refer to over and over again.

I know what your're thinking: *Ugh, why can't you just point me to this so I can just read it later?*

Because half of you won't, that's why :P But also because:  
* Every time you say, write, or read something you make another copy in your brain.
* Every time you say, write, or read something you make another copy in your brain.
* Every time you say, write, or read something you make another copy in your brain.
* Every time you say, write, or read something you... *say it with me now*

No seriously. That's how you memorize stuff. You say/ write/ read it a bunch until you know it in your sleep. And that's what we're going to do today.

Here's the fun bonus, we're going to learn some fun CSS and make it look cool while we're at it. The faster you get through the basic stuff, the more time will have to play around and trick out our own individual cheatsheets.

## Steps:

1. Open C9 and find the username_github_io workspace you created in a previous class.

1. In your workspace file navigator, right-click and select *Create File*. Name it <code>cheatsheet.html</code>

1. Create *doctype*, *html*, *head*, and *body* elements. like so:

        <!DOCTYPE html>
        <html>
            <head>
                <title></title>
            </head>
            <body>

            </body>
        </html>

1. Find the title element inside the head element. Write "My Hacker Cheatsheet" in it.

        <title>My Hacker Cheatsheet</title>

1. Time for the goods. We'll wrap it all in HTML in a bit, but how about we just write it out in plain English first so we can focus on code next. Write (or copy/paste, this *is* a cheatsheet after all) the following block out in the *body* element of you page.

        My Hacker Cheatsheet
            Keyboard Shortcuts
                Ctrl-S
                Save file

                Ctrl-C
                Copy Text

                Crtl-V
                Paste Text

                Ctrl-X
                Cut Text

                Ctrl-Z
                Undo Change

            Navigating Folders in the Command-Line

                cd
                Change directory

                cd ..
                Go back outside the current directory

                ls
                List files and directories in the current directory

            Committing Your Work To Git

                git add .
                Stage all new changes so they'll be included in the next commit

                git commit -m "Your commit message goes here"
                Commit all currently staged changes so they can be pushed. Be sure your commit message says what you just changed in your code.

                git push
                Push all your most recent work to GitHub

1. Let's wrap our cheatsheet in some HTML. Well what does wrap mean? Simply means if we have either some text or some HTML code we've written, we're going to pust some HTML around that. For instance if I have the phrase "Hello World!" and I want to make that the main headline of my page, I want to wrap it in an <code>h1</code> element like

        <h1>Hello World!</h1>

    So lets wrap our headlines in header elements. Wrap "My Hacker Cheatsheet" in an <code>h1</code>. Then wrap our 3 topics each in <code>h2</code> elements. Don't forget your opening AND closing tags or things will get wonky fast.

1. Lets make our commands into lists
