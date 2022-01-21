Notes for getting sketch onto github:

Need to either do this before creating your local project folder, or have a different name for project on github & start a second folder during this project

Need to create a PAT (Personal Access Token) to use instead of your github password

# Making the github repository:

login to github.com

click on the '+' and start a new repository

give the new repository a name, this will be the name of your project. it will be difficult to change this later, so choose carefully

make it public

check 'initialize with a readme'

don't need to pick a license right now

click 'Create Repository'

*You have a repository on github!*

*github has now generated a URL ending in .git for you*

*you will need it in a minute*

to find the .git URL within your repo:

click on the green "Code" button that has a down arrow

the link will be under the "HTTPS" tab

# Creating a PAT (Personal Access Token) on github to authenticate Git operations

link to github tutorial: https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token

verify your github email if you haven't yet

in the upper right corner, click your profile pic, and click settings

in settings, click 'Developer Settings' in the left sidebar

in Developer Settings, click 'Personal Access Tokens' in the left sidebar

click the button that says 'Generate new token'

give your token a descriptive name

select an expiration date

in the scopes, select 'repo' (& maybe 'workflow', not sure if it's necessary but I selected it)

click the green button that says 'Generate token'

copy the token, and paste it somewhere safe like a password (github will not show it again once you leave this page)

*You now have a PAT!*

*It will be used in place of your github password in the terminal*

# Using the Terminal to get your project on the internet

open a terminal window

navigate to the folder that is / will be holding your project folder
*NOT THE PROJECT FOLDER ITSELF*

type:

git clone <repository .git link>

//replace <repository .git link> with the .git link from your github repository, then press enter

//( example: git clone https://github.com/davisRose/project0.git )

*A connected folder with the same name as your github repository has been created in the parent folder that you navigated to in the terminal!*

*This new folder should only show that it contains a README.md file at this point*

*A hidden folder named ".git" is included within this new folder, if you see it, don't mess with it or add anything to it*

open finder, and go to your new project folder

open another finder window to copy or duplicate the files that you want in your repository

paste or move the files you want into your new project folder

*Now those files you just added to the folder are also in your repository*

in the terminal where you ran git clone, type 'cd projectname' (replacing projectname with your new folder's name) to move into your newly created/cloned repository folder

*git status is a command that is useful to know, allows you to check if your branch is up to date*

try it now to check if everything is as it should be, type & enter:

git status

*if everything is working, the terminal will return something like this:

> On branch main
> Your branch is up to date with 'origin/main'.

> Untracked files:
>> (use "git add <file>..." to include in what will be committed)

>>> README.txt
>>> addons/
>>> index.html
>>> p5-test.js
>>> p5.js
>>> p5.min.js
>>> p5.pre-min.js
>>> sketch.js

> nothing added to commit but untracked files present (use "git add" to track)

if you get information like below, it is telling you that you have not committed certain files:

> Changes to be committed: 
>> (use "git reset HEAD <file>..." to unstage) 

>>> new file: README.txt
>>> new file: index.html
>>> new file: p5.js
>>> new file: p5.sound.js
>>> new file: sketch.js

that’s useful because now you know you should commit so you don’t lose your work*

> For this next step, Jesse's instructions didn't work for me
> 
> Jesse's instructions:
>> type: 
>> git add .
>> git commit -am’first commit’
> 
> I found a solution at this link:
>> https://stackoverflow.com/questions/7080803/how-can-i-commit-files-with-git


make sure you are still *in* your project folder in the terminal

type & enter: 

git add .

then, type & enter:

git commit -a -m "first commit"

*Now you're up to date locally! The local folder is being tracked by git. But this is only local, it’s not available on the internet yet.*

To get it online, in other words to make it available on the internet, type & enter:

git push origin main

*Whenever you want to commit and push to github, aka every time you save your sketch file, you just type & enter: 

git commit -a -m "some useful message here"

git push origin main

note: your terminal might not say (main), you can check if you‘re in a valid repository by typing git*

at this point your code is saved online, but isn't published yet

## NOTE:
> The first time I did this, the terminal asked for my GitHub username & password 
> When doing it again for this test, it did not!
>> If you are prompted to enter your GitHub username & password, 
>> *Use the PAT you created earlier instead of your password!!*
> I don't remember which command prompted it the first time, unfortunately.
> So, just keep in mind that you'll need your PAT in place of your password when using the terminal. 

# Publishing your code on the internet / GitHub 

// This part also differs slightly from Jesse's instructions
// Jesse directs to 'github pages' in the repo settings
// But, github changed that to a separate tab in settings called 'pages'

From your GitHub repository's main page, navigate to the repository's 'Settings' tab

In the left sidebar, click the 'Pages' tab

Under 'Source', click the drop down button that says 'None'

Under 'Select branch', select 'main'

Under the '(root)' folder drop down, select '/ (root)'

Save!

This will give you a link to view your project:

"Your site is ready to be published at <link>."

Your link will always be something like https://your-github-username.github.io/your-repository-name/

It might take a few minutes to start working. It's a free service, so it can take a while.

*Once your project is working at that link, you're all done!*



















