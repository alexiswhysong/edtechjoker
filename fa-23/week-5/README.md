# Week 5: More JS Ecosystem shhhhhtuff
- This is not react just loading into the index.html :) https://github.com/M18ab/react-app/blob/main/public/index.html
- Many of you didn't get it working
- This was rough... by design.
- Now, we'll use working examples from people who did, to learn about all 3 and slow down (slightly)

## Common issues / general feedback
- "error when running `npm start`" - npm command must be run from the project root. Clone the project, you have to be in that directory to run commands
- VueJS deployment on vercel needed to be the VueJS + Vite; this came up in class.
- Ensure you mark your repos public on github. Private repos we can't see and can't be graded. Verify your work is public so it can be reviewed
- "Should I run commands from inside VSCode or terminal window?" USUALLY it doesn't matter, but if you have an issue running a command from inside VSCode, make sure you attempt in another window just to rule that out

## Activity 1: fork / play with classmates working examples
For each of these, let's go through and do this together. With each of these I want you to do the following..
- Go to the example, fork the example to your own github
- clone it to your machine
- `npm install`
- `npm start`
- `code .` or just open VScode
- As I go through, follow along so you can understand the structure

If we cover yours, come get a (completely useful, great, awesome.. sticker)
- top React example: https://github.com/Jps709/create-react-app
- top Angular example: https://github.com/ashnaabhide/angular
- top VueJS example: https://github.com/Pandaalifter/card-chad

## Activity 2 / Part 1 of homework
Now we should have some fundamental understanding of what's where, you have a working copy of a classmate's card for each one.
Now knowing this..
- Hollow out their portions of this so that it's your card CSS and HTML
- attempt to get your JS in there as well on the Vue One
- Push all 3 back to their respective github locations
- Ensure the demo rebuilds on vercel / it's wired up to vercel (you can add projects in after the fact via vercel)

## Thursday
### Developer workflow tips
- Github: Setup SSH keys https://docs.github.com/en/authentication/connecting-to-github-with-ssh/about-ssh
- Github: **FORK** means you have a copy of someone's codebase on your github account
- Github / Your machine: **CLONE** means you are bringing that code onto your personal computer. Always get repos either via the **SSH** option OR **Github Desktop**
- **Github Desktop** in the GUI, select your project (top left, or create new, or add from Github). Then Hit **Open in VSCode**
- **VSCode** your code will be open on the left **for your local copy**. Go to the toolbar for VSCode and hit "Terminal" and new Terminal if one is not already open
- **this opens the folder tree / command line to the same spot VSCode is looking** . Here is where you type `npm install` and when that finished, `npm start` or `npm run dev` or whatever the command is you are looking to run

### Terminal basics
everything you do in a GUI is just a button mapped to running a command in the CLI. The GUIs differ between Linux, Mac, Windows, but the commands are very similar in most instances or exactly the same.

- you are in a folder; that folder is your code
- the "directory tree" / structure goes all the way back to the root of your hard drive `C:\` or `/`
- `cd` is for CHANGE DIRECTORY to go up it's `cd foldername` to go down it's `cd ../`
- `ls -las` will give you a LISTING of the files in the current directory
- `cwd` CURRENT WORKING DIRECTORY will print out where you currently are in case you forget
- `mkdir` MAKES A DIRECTORY
- `code FILENAME` SHOULD open the file in VSCode (could vary based on OS)
- `open .` will work to allow you to open a finder / folder in your GUI (could vary based on OS configuration)
- `npm` a program that runs node, package, manager commands (`yarn` is a different program but runs the same commands)
- `git add -A` - add everything to git bc we want to track these changes (this is also visible on the left side of VSCode)
- `git commit -m "the message"` commits the changes (this is also visible on the left side of VSCode)
- `rm` is for REMOVE so you can delete things via CLI. you delete it, it's gone, unless you bring it back via version control

## Short lecture for context of where we go next
- Now that we've got the basis for workflow, location, building demos to present them.. it's time to move into the world beyond them
- We have JS, where the web started, then we had jQuery to prop it up, then we had frameworks to make component like things
- Now, it's time for where all development is heading and where you can best invest your time learning and building
- I changed my entire career focus, outlook, and professional affiliations based on this technology standard..
- Why web components, understanding how Wcs interplay with other libraries, who’s using them and why
- Short lecture: https://docs.google.com/presentation/d/1heprQE0TXrKgc1T1ISnvlpUREREFIAehArEncg_I9-o/edit?usp=sharing

## Homework
Two parts;

### Part 1 Links to all 3 repos with your card working in Angular, React, Vue
- easy if your following along in class Tues. If your struggling here DM / ask after lecture / office hours
- Follow the steps from above to pull your code in locally

### Part 2
- Run through ALL Lit.dev tutorials on "Build" and "Build" found here https://lit.dev/tutorials/ so that you understand how we'll be building going forward
- Create a new (empty) github repo with a name for your card. Let's call it `my-card` or `cyber-chad` or some name for your card but make sure it has a `-` and is all lowercase; clone it locally from github so you have a copy of a blank repo on your computer with which to start working
- Run the command found here https://open-wc.org/guides/ in order to create a new element called `my-card`.
  - create a new "application" called the name of your repo (my-card, cyber-chad, etc)
  - Note: in the options via CLI, if you see a `O` circle this is a checkbox. move between them using the arrow keys and hit spacebar to select each option
  - When it asks you to write files to disk, pick yes. When it asks to install via npm / yarn, install via npm.
  - Also note: We will be using open-wc the rest of the semester in some capacity so best to familiarize yourself with the community docs
- `npm start` and you'll be able to develop using this locally / see a live reloading environment that has a spinning svg
- Take this boilerplate repo, looking in `src` for source and `index.html` for the "demo" page that's launched **and port your CSS / HTML to this approach**
  - If that was easy, then take a stab at doing this w/ your JS events in your buttons, if not then just getting code in place is fine.
  - `document.querySelector` is global but in a web component, `this.shadowRoot.querySelector` is for querying JUST inside your component
- Push results back up to github (make sure it's a public repo)

## LINT DISABLE
if you get an error in your `open-wc` code when you go to commit to github. Go into `package.json` and delete this block from it
```
  "husky": {
    "hooks": {
      "pre-commit": "lint-staged"
    }
  },
```
This is ensuring coding conventions match a certain specification. The feedback is useful usually but some times can be limiting to newbees.

## Submission
- Gist linked to Canvas
- Links to all 3 github repos of the port of your card hopefully looking correct in React, Angular, Vue+Vite
- Link to your github repo for making a card in `open-wc`
- Answers to these questions
- 5 similarities between the open-wc repo structure and your react / vue / angular structures
- Was this easier, harder, or the same difficulty as exploring the frameworks?
- Any concept, structure, terminology, etc that your struggling with and need additional guidance at the end of this homework / 1st 5 weeks (1/3 of course)
- Try to hook this up to vercel (code up on github, then add the project via vercel.com . You'll need to change "output" to `dist` in your settings). If you attempt this and it doesn't work don't worry about it but if it does work, add that link into your gist so we can see it built
![vercel GUI for settings](https://user-images.githubusercontent.com/329735/217584610-449ee034-ff60-49c5-8c8d-41f6283aa512.png)

## Final notes on this week
Try your best, ask questions. We're going to go from complex / big idea / world view sorta stuff back into details. The frameworks were mostly so that we have an idea of where the world used to be. Now we'll start drilling into web components and JS within this context as it really is the future of the web (and the future is here now).
