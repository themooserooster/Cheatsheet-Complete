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

2. In your workspace file navigator, right-click and select *Create File*. Name it <code>cheatsheet.html</code>

3. Create *doctype*, *html*, *head*, and *body* elements. like so:

        <!DOCTYPE html>
        <html>
            <head>
                <title></title>
            </head>
            <body>

            </body>
        </html>

4. Find the title element inside the head element. Write "My Hacker Cheatsheet" in it.

        <title>My Hacker Cheatsheet</title>

5. Time for the goods. We'll wrap it all in HTML in a bit, but how about we just write it out in plain English first so we can focus on code next. Write (or copy/paste, this *is* a cheatsheet after all) the following block out in the *body* element of you page.

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

6. Let's wrap our cheatsheet in some HTML. Well what does wrap mean? Simply means if we have either some text or some HTML code we've written, we're going to pust some HTML around that. For instance if I have the phrase "Hello World!" and I want to make that the main headline of my page, I want to wrap it in an <code>h1</code> element like

        <h1>Hello World!</h1>

    So lets wrap our headlines in header elements. Wrap "My Hacker Cheatsheet" in an <code>h1</code>. Then wrap our 3 topics each in <code>h2</code> elements. Don't forget your opening AND closing tags or things will get wonky fast.

7. Lets make our commands into lists

    Wrap each section of the commands in a `ul` tag and then wrap each command in a `li` tag
    
    ```html
    <ul>
        <li>
            Ctrl-S
            Save file
        </li>

        <li>
            Ctrl-C
            Copy Text
        </li>
        
        <li>
            Crtl-V
            Paste Text
        </li>
        
        <li>
            Ctrl-X
            Cut Text
        </li>
        
        <li>
            Ctrl-Z
            Undo Change
        </li>
    </ul>
    ```

8. Now we are going to wrap line within the `li` tags with a `span` tag.

    ```html
    <ul>
        <li>
            <span>Ctrl-S</span>
            <span>Save file</span>
        </li>

        <li>
            <span>Ctrl-C</span>
            <span>Copy Text</span>
        </li>
        
        <li>
            <span>Crtl-V</span>
            <span>Paste Text</span>
        </li>
        
        <li>
            <span>Ctrl-X</span>
            <span>Cut Text</span>
        </li>
        
        <li>
            <span>Ctrl-Z</span>
            <span>Undo Change</span>
        </li>
    </ul>
    ```
    
9. Between each command and description of that command, let's add an arrow. Add the following between each command and description.

    ```html
    <span>--></span>
    ```
    
10. Now we are going to add classes to the commands and the arrows. Classes are used to distinguish and group elements together for a bunch of purposes. For our purpose, we are going to use them to style our cheatsheet.

    ```html
        <li>
            <span class="command">Ctrl-S</span>
            <span class="arrow">--></span>
            <span>Save file</span>
        </li>
    ```
    
11. And finally let's add our CSS. Copy the following into the head of your html

    ```html
        <style>
            body {
                width: 80%;
                margin-left: auto;
                margin-right: auto;
                margin-top: 0px;
                font-family: Arial, sans-serif;
            }

            h1 {
                background-color: red;
                color: white;
            }

            h2 {
                background-color: gold;
            }

            li {
                background-color: gray;
                color: white;
            }

            h1, h2, li {
                padding: 7px;
                margin-top: 7px;
                border-radius: 5px;
            }

            [class="command"] {
                font-weight: bold;
                font-family: Courier;
            }

            [class="arrow"] {
                font-weight: bold;
                font-family: Courier;
                margin-right: 20px;
                margin-left: 20px;
            }
        </style>
    ```
