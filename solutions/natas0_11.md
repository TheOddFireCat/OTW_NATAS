# NATAS Levels 1 - 11
## Level 0 - 1
<details> 
  <summary><b>Level 0 Solution</b></summary>
  
  &nbsp;&nbsp;By right clicking on a page in a browser (at least in my experience with Chrome) you can select the 
  option "Inspect" this brings up the Developer Tools side menu.
  <br><br>
  
  In the HTML code in the Elements tab we can look around and find the password for Level 1 
</details>
<hr>
<details>
  <summary><b>Level 1 Solution</b></summary>
  
  &nbsp;&nbsp;The devs now disabled our ability to right click, however that doesn't stop us as there's a keyboard 
  shortcut to open up the DevTools side menu. F12
  <br><br>
  
  In the HTML code in the Elements tab we can look around again and find the password for Level 2 
</details>

## Level 2
<details> 
  <summary><b>Solution</b></summary>
  
  &nbsp;&nbsp;By now, we're sort of used to having the DevTools open, so we look around there.
  This time the answer isn't in plane sight, but we have a clue.
  There is a small image in the page thats invisible, and we get the directory its pulled from.
  <br><br>
  
  Appending the location to our URL takes us to where the image is stored, and we find a text file as well, and
  within, we find the password for level 3
</details>

## Level 3
<details> 
  <summary><b>Solution</b></summary>
  
  &nbsp;&nbsp;Looking around the Elements tab we don't get much besides a hint that even Google won't find it
  this time. The reference here is related to how search engines function. <br><br>
  
  In order to actually get results, search engines employ the use of Web Crawlers, these are bots that search
  the web and catalog the sites and webpages within. This raises security concerns regarding sensitive pages
  that we wouldn't perhaps want cataloged and then be possible to search up. <br>
  There is a way to stop the bot from cataloging however and that is to list the pages and directories we want 
  to conceal in a text document called `robots.txt`.<br><br>

  Appending `/robots.txt` to the URL brings us to that documents contents and we find a directory.
  <br><br>
  
  Appending the directory to our URL greets us with a similar view to level 2, and we find the password to
  level 4
</details>

## Level 4
<details> 
  <summary><b>Solution</b></summary>
  
  &nbsp;&nbsp;This time, there isn't anything in DevTools. We rely on the text provided on the page.<br><br>
 
  The site expects us to come from the level ahead, level 5. that isn't possible however. <br>
  So we instead use
  one of these; 
    <ol>
      <li>Burpsuite</li>
      <li>An extention to modiffy the referer</li>
    </ol>
  <br><br>

  <details>
    <summary><b>Burpsuite</b></summary>
    &nbsp;&nbsp;Using the Intercept tab you can modify the request to the site and change the `Referer` header
    to the URL it expects, and then send it over. I myself didn't use Burpsuite for this however.
  </details>
  <details>
    <summary><b>Browser extension</b></summary>
    &nbsp;&nbsp;I have found two extensions that work for this.
    <ul>
      <li>On Chrome: Referer Control</li>
      <li>On Firefox: Referer Modifier</li>
    </ul><br><br>
    With Referer Control, you enter the URL of the site you want the Referer changed when you visit it, select
    custom, and then what you want the Referer to be. <br>
    With Referer Modifier, it's universal so you just put what you want the Referer to be.
  </details>
  
  Reloading the page gives us the text with the password for level 5
</details>

## Levels 5 - 11 TBA
