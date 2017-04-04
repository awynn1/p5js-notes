# GitHub Pages - Publishing your work

1. Go to [Github.com](Github.com) and create a new Repository.
2. Click the Copy to Clipboard Button that contains the Git URL link.
3. Go back to Cloud 9 and inside the TERMINAL (if the terminal isn't there, go to the menu and click VIEW > CONSOLE) type:

```git
    git init
    git remote add origin <PASTE GIT URL HERE>
    git add .
    git commit -m "first commit"
    git push origin master
```

**Note**: Use your brain. Above when I wrote `<PASTE GIT URL HERE>`, you are copying and pasting the git url from the github repository that you created in steps 1 and 2.

**Second Note**: When I wrote `"first commit"` this is a message that can be anything. You don't have to write `"first commit` every single time.

4. After `git push origin master`, you will have to login to your GitHub account. Type in your username then your password.

**Note**: Your password is hidden from your view. Most people think that their terminal froze because they don't see any characters. Trust that the terminal is still taking your password as you type.

5. Go Back to GitHub. 
6. Click Settings
7. Scroll Down to GitHub Pages
8. Click the Dropdown Menu under "Source"
9. Click Master Branch
10. Click Save
11. Refresh the Page and then scroll down to find your published link

## "But what if I still get a 404 error?!?!?!"

Don't trip chocolate chip. Go back into Cloud 9 and go into your `index.html` file. Anywhere in the `<body></body>` add a single `space`. Then save the file. 

In your terminal run just these 3 commands:
```bash
    git add .
    git commit -m "fixed html for ghpages"
    git push origin master
```
