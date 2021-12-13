# Modal
# What You Should See
1. In the “Our Store” section of the website, when you click on a given item, the modal should pop up, displaying the image of the item clicked.
2. When you click the close button, the modal should close.
3. When you click the left and right buttons, all images should cycle through the modal container.

# JavaScript Used
* DOM Manipulation
* Control Structures
* Array.forEach()
* JavaScript CSS Manipulation
* eventListeners
* Immediately Invoked Function Expressions

# New Things Learned or Refreshed
In this project, I struggled quite a bit. I first tried to code it entirely by myself. My first snag was trying to add an eventListener to my node list of store items. I kept getting the error that my node list was not a function. Specifically, my error was `storeItems.addEventListener is not a function`. I found my solution on Stack Overflow after Googling the exact error: [https://www.google.com/search?q=storeItems.addEventListener+is+not+a+function](storeItems.addEventListener is not a function). Turns out, I forget my storeItems was a node list. What I really was trying to do needed an eventListener on each of the items within the nodeList. So, I added a forEach to the nodeList and then added an eventListener forEach item. My second snag was an issue of trying to change the background images of the container that held the images. I thought I could simply use `element.style.background = './img/image.jpg'`. Turns out I needed to use the url function for my background property to work. (e.g. `element.style.background = url(./img/image.jpg)`. Of course, in the code you'll see I made my life easier by using template strings.
 
# Biggest Take Away(s)
I don't have to add .style when adding a classList to an element. It's simply `element.classList.add()` not `element.style.classList.add()`; I spent a lot of time thinking I can add individual properties to the CSS stylesheet itself. Can't be done (not that I know anyway). Add the style to the element. I spent a lot of time trying to access nested tags using JavaScript (e.g. <tag><img src=”source”></img></tag>.  (e.g. I tried to select the src but first selected <tag>, thinking I can access the <img> tag. Just go after the <img> tag itself. **Misspelling sucks and are often my biggest bugs!** I couldn't for the life of me figure out why a portion of my code wasn't working until I realized I misspelled the word, ‘background.' I spelled it ‘backgound'. See what I did there?
