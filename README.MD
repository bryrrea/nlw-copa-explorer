# NLW COPA (NLW WORLD CUP)  

## 1.Introduction  
The football (soccer) World Cup is one of the biggest sporting events and takes place every four years. Brazil is the biggest winner of this competition with 5 titles, followed by Italy and Germany (4 titles each).  
The NLW, meanwhile, is a free event offered by [Rocketseat](https://www.rocketseat.com.br/). The event takes place over an entire week in order to teach basic and advanced concepts of web and app development. This edition (the 10th) was divided into two tracks: **Explorer** (for those with little or no development experience) and **Ignite** (for those with some development experience). In this edition, the Explorer track developed a calendar of World Cup matches, while the Ignite track developed an app to make a World Cup sweepstake.  

## 2.Who am I, my background and my track  
Hi, I'm Bryan! I'm a Brazilian Biochemical Engineer graduating in April 2022. I've always had a lot of appreciation for technology, development and programming, but only recently decided to start studying deeper into the field (from NLW eSports, to be precise).  
I started getting involved with programming at the end of 2019. In early 2020 (already during the pandemic), I was selected for a Python minicourse that was offered by Stanford University (**Code In Place**). I studied the minicourse and became really passionate about the development area. After four weeks, I was able to create my [final project](https://github.com/bryrrea/code_generator_to_boxes_of_medicines).  
Later, Rocketseat offered the [WorkshopDev Special](https://www.youtube.com/playlist?list=PL85ITvJ7FLohGTWaE_p0J6B-TLmQbN4ka), which an app was built that would serve as a hub for ideas and study. Unfortunately I couldn't make it to the end of that special week (I got sick), but it was there that I fell in love with web development. However, the college classes started again in the "emergency" modality (it was the name they gave to avoid saying it would be online) and it became impractical to study Engineering and Development at the same time, since the college professors filled us with activities to make up for their insecurities and lack of didactics.  
After graduating in April of this year, I started studying Data Analysis more in depth, and I remembered my desire to study web development when I received Rocketseat's registration invitation to [NLS eSports](https://github.com/bryrrea/nlw-esports-explorer). After the event, I created my first "solo" front-end project: a link aggregator called [linkhub](https://bryrrea.github.io/linkhub). I used only HTML and CSS to create this page.  
I am currently taking the lessons from the Free Code Camp course, and for training purposes I have started to "reinvent" the projects they use in the course. I have named this personal project [Free Code Camp Remake](https://github.com/bryrrea/FreeCodeCampRemake). In addition, I'm taking Rocketseat's [Discover track](https://app.rocketseat.com.br/discover) (an introductory web development course made available for free by the educators), and the [Orange Tech+](https://web.dio.me/track/81278323-8916-401b-8446-03118eaff280) bootcamp (by DIO in partnership with Banco Inter). So, being a beginner, I again chose participating in the Explorer track.  

## 3.Technologies and tools used  

|<img src="./assets-readme/html.svg" alt="Ícone do HTML" width="32px" style="color:#E34F26;" /> <img src="./assets-readme/css.svg" alt="Ícone do CSS" width="32px" style="color:#1572B6;" /> <img src="./assets-readme/javascript.svg" alt="Ícone do JavaScript" width="32px" style="color:#F7DF1E;" /> <img src="./assets-readme/git.svg" alt="Ícone do GIT" width="32px" style="color:#F05032;" /> <img src="./assets-readme/github.svg" alt="Ícone do GitHub" width="32px" style="color:#181717;" />|
|:--:| 

## 4.Project Prototype  

 |**Mobile version**|**Desktop version**|
 |:----------------:|:-----------------:|    
|<img src="./assets-readme/mobile.jpg" alt="Imagem da versão mobile" height="256px" />| <img src="./assets-readme/desktop.jpg" alt="Imagem da versão desktop" width="256px" />|  

## 5.HTML structure  
As you can see in the images above, in the mobile version it is desirable that the cards are one below the other, while in the desktop version it is desirable that the cards are one next to the other. Thus, we should use a concept known as **"mobile first"**, i.e, we develop the application first thinking about mobile devices and then thinking about larger screen sizes.  
With this in mind, the application was developed with the following structure:  

 - The `<head></head>` element provides vital application information, such as `<meta />` elements to designate the application's characters and responsiveness, and `<link />` elements to point to the links in the font used (Roboto) and to point to the css file;
 - The `<body></body>` contains everything that is important to appear on the user's screen, plus the script that will automate the creation of the cards;
 - Inside the `<body></body>`, we have a `<header></header>` with the *NLW Copa* logo and the application "call" (Calendar);
 - A `<div></div>` was created with an **id** which receives a value (**"app"**) and inside that div we have the entire application;
 - Inside the **"app"** we have the `<main></main>`, i.e, we have all the cards inside this element. Therefore, this element gets the **id** **"cards"** attribute;
 - Inside the `<main></main>` we have a `<div></div>` with attribute ***class*** **"card"**. This element will represent each card that will appear on the screen. In each card, we have:
    - An `<h2></h2>` element containing the date and a `<strong></strong>` element containing the day of the week on which the match will take place;
    - Since the grouping of games is by date, we can treat each game of the same date as an element of an unordered list. Therefore, we use the element `<ul></ul>` to create an unordered list for each date, and each game within `<ul></ul>` is stored in an element `<li></li>`;
    - Each element `<li></li>` has two elements `<img />` (one for each team in the match), and one element `<strong></strong>` (to highlight the time of the match). The `<img />` contain the location where the flags of the teams have been saved (in *svg* vectors).  

## 6.CSS Rules  

### 6.1.Overall  
 - A **reset** of the **`margin`** and **`padding`** properties was performed, since browsers originally have their own values for these properties. Additionally, the `box-sizing` property was set to `border-box` ensuring that boxes take into account the content, the borders, the ***`margin`** and **`padding`** when calculating their size;
 - The **Roboto** font was set for the entire `<body></body>`;
 - The application's wallpaper was provided in the application's prototype. The image was initially positioned at the center of the horizontal and 68% of the vertical, ensuring that the layout of the wallpaper was faithful to the one presented in the prototype;
 - Still thinking about the background, a color (#121214) was incorporated to make an interesting effect with the wallpaper;
 - As for the positioning, in short, the elements that originally have **display inline** were used to arrange them side by side, and the **Flexbox Model** was used to position the other elements on the screen.  

### 6.2.Cards  

 - To make the cards lie one below the other we used the `flex-direction: column;` property so that each card occupied a row in a single column;
 - The borders of the cards were rounded, and the bottom border of each card was given a yellow color;
 - By using the **Flexbox**, the **gap** property (responsible for producing a spacing between elements contained inside the same parent element) was unlocked;
 - **Flexbox Model** will help with the app responsiveness;
 - **`justify-content`** property of the elements `<li></li>` was set to **`space-between`** so the elements inside each `<li></li>` have a certain horizontal spacing between them;
 - The date and the day of the week appear in a box with rounded borders. These borders have a color too;
 - The `<img />` containing the svg has been resized to 50X50 px;
 - The spacing between elements was defined by the **`margin`** property, and the padding of the elements was defined by the **`padding`** property. Several different types and measurements (in pixels) of **`margin`** and **`padding`** were defined;
 - The **`width`** property was set to **`fit-content`** to make the content fit the width available for distribution in some elements, such as in the **`#app`** and the `<h2></h2>` element of the **`.card`**;
 - The content of the `<span></span>` element was written entirely in lowercase so that we could use the **`text-transform`** property, set to **uppercase`** (all uppercase characters).  

### 6.3.Texts and lists  

 - The texts have two font sizes and types: sizes 14 and 36 px; type 700 (bold) and 900 (black). All texts have the same color (#e1e1e6), except for the `<h2></h2>` elements (#f7dd43);
 - The list decorations (dots) have been removed;
 - Each list item has a top border with its own color to indicate a separation between the items.  

## 7.Script  
A **script** was written to provide an introduction to JavaScript. The goal of the **script** was to somewhat automate the creation of the cards, since it would be a snippet of HTML code that would be repeated several times in the HTML of the app. To do this, two functions were created:  

 - **createGame** Function: This function takes as attribute a National Team, a time, and another National Team (**player1**, **hour**, and **player2**). Inside it, it is asked to return the elements `<li></li>` and their components (the image of National Team 1, the time and the image of National Team 2). This is done by interpolation, since the svg files containing the flags of the National Teams have been named following a pattern ("*icon-NationalTeam.svg*", which is replaced in the interpolation by `icon-${player1}.svg`, for example);
 - **createCard** Function: This function takes as attribute a date (**date**), a day of the week (**day**) and the games (**games**). Here you will create the HTML elements needed to build the daily cards for the games. Again, the replacement is done by interpolation, where **date** and **day** are placed in the **cards** elements `<h2></h2>` and `<span></span>`, while the **games** attribute is placed in the `<ul></ul>` element.  

>NOTE: The elements used to create the cards have been moved from the HTML document into **script**, leaving only the main **div** (**`#app`**) in the **body** of the HTML (in addition to **script**, of course).  

The script is run inside `main.js` itself. I think it would be best to separate the two functions into two different js files, since they are two different "features". This would help make everything more organized (in my view), since the script would call the two functions as modules/functionalities.  

## 8.Responsiveness  
Responsiveness is what ensures that the front-end will appear on all screen sizes without error or breakage. The layout can be a little different, but without being accidentally broken by not adapting to the size of a screen. This is why it is common to use the **"mobile first"** model, since it is very common for new developers not to realize that the layout of their app or website can break when displayed on mobile devices.  
Responsiveness is handled in CSS with the use of **`@media`**. It must be followed by a size and after that the properties can be written as normal inside the selectors.  

```css
@media (max-width: 700px) {
    selector {
        propriety01: value01;
        propriety02: value02;
    }    
}
```  

As you can see above, a maximum size of 700 px was set for the original properties 01 and 02 to change.  
In this project, a minimum value of 700 px was set for some properties to change, i.e., such properties will only change on the screen of devices with a **viewport** (user's browser usage area) larger than 700 px. Also, according to the prototype, it is desirable for the desktop version to display two cards per row (one next to the other). Below is the snippet that will change the page layout on devices with screens that have a viewport larger than 700 px:  

```css
@media (min-width: 700px) {
    #cards {
        flex-direction: row;
        flex-wrap: wrap;
        max-width: 670px;
    }
}
```  

As in common mobile screen sizes it was originally defined that the direction of the Flexbox should be **columns**, for devices with larger screens it is desirable that the **`flex-direction`** be changed to *row*. For have only two cards appearing per row, it was necessary to make a calculation taking into account the width of two cards plus the spacing between them (which is originally 32 px). Thus, it was concluded that the maximum acceptable width (**`max-width`**) on a row to hold two cards is 670 px. Finally, the **`flex-wrap`** property was set to **`wrap`**, since this property guarantees that a third card is placed below the two. It is worth noting that the height of the aligned cards in a row will always be equal to the height of the largest card in that row.  

## 9.Animations  
Animations are written in the CSS document. For this project, an animation was proposed in which the cards appear from top to bottom, one after the other.  
In the CSS document, the animations are created from **`@keyframes`**. Each animation must have a name so that it can be called in the selector where the effect will occur. This is called from the property **`animation`**.  
We only worked with 3 cards in this code example, and thus the transition animation of the cards could be done manually within the CSS itself from the **nth-child** pseudo-selector. However, since there would not be only 3 cards in the original app, it is necessary to automate the transitions. To do this, a variable was created in the **script** to control the transition time. This variable was interpolated inside the **style** attribute of the **div** element that receives the **id "card"**, that is, this variable is incremented **inside** the **createCard** function.  

## 10.Styling the project  
In the project prototype (available at [Figma](https://www.figma.com/file/DMEo8R17aIzn7qjVmAYzoW/Calend%C3%A1rio-de-Jogos-(Community)?node-id=0%3A1)), you can see that some colors can be switched between green, yellow and blue (colors of the Brazilian national team). The color of the bottom border of the cards and the color of the background are the styles that can be switched in this project. For this, variables must be created in the CSS to be able to make changes based on them.  
Four variables have been created in the **root** of the HTML document:  

 - `--card-h2-border-color`: variable created to store the border color of the card element `<h2></h2>`, and can take three colors (`#746615`, `#338AF3` or `#047C3F`);
 - `--card-primary-border-bottom-color`: variable created to store the color of the bottom border of the cards, can take three colors (`#f7dd43`, `#338AF3` or `#047C3F`);
 - `--card-bg-color`: variable created to store the color of the card background, and can take three colors (`#1d1c19`, `#202024` or `#1A1F1B`);
 - `--bg`: variable created to store the **background** image of the page. From the **url** function, you can pass the location where the images are located. For this project, three different backgrounds were saved in the **assets** folder: **`bg-yellow`**, **`bg-blue`** and **`bg-green`**. The images have been saved in svg format.  

## 11.Code refactoring  
Refactoring is something common in a developer's day-to-day life, since it is necessary to present the code in the most organized and functional way possible in order to facilitate its maintenance.  

 - When the HTML snippet was moved into **JS script**, the `<header></header>` was moved into **JS script** to illustrate the refactoring later. Therefore, since the `<header></header>` did not need to be changed constantly, it was moved back into the HTML document;
 - The `<main></main>` element has also been placed in the HTML document again, since what is changed is **inside** the element;
 - After these changes, the app presented a different look than the original. Since the changes are made to the **div** **id "cards"**, it was necessary to change the **querySelector** in JavaScript to the **id "cards"**, since it previously pointed to the **id "app"**;
 - The characters "`" are called **string literals** and are used to represent blocks of **strings** in a JavaScript document. However, the variable that calls the **createCard** function does not have blocks of **strings**. Therefore, the use of **string literals** becomes unnecessary. Thus, since **string literals** and interpolation characters are deleted, we concatenate the **createCard** function calls. Below is a before and after example to illustrate what is being said here:  

    ```javascript
    document.querySelector("#*cards*").innerHTML = `
    ${createCard(
        "24/11",
        "quinta",
        createGame("brazil", "16:00", "serbia") +
        createGame("switzerland", "07:00", "cameroon")
    )}

    ${createCard(
        "28/11",
        "segunda",
        createGame("brazil", "13:00", "switzerland") +
        createGame("cameroon", "07:00", "serbia")
    )}

    ${createCard(
        "02/12",
        "sexta",
        createGame("brazil", "16:00", "cameroon")
    )}
    `
    ```  

    ```javascript
    createCard("24/11", "quinta", createGame("brazil", "16:00", "serbia") + createGame("switzerland", "07:00", "cameroon")) +
    createCard("28/11", "segunda", createGame("brazil", "13:00", "switzerland") + createGame("cameroon", "07:00", "serbia")) +
    createCard("02/12", "sexta", createGame("brazil", "16:00", "cameroon"))
    ```  

 - The positions of the page background image were removed, since the background image was later saved as svg in the **assets** folder, with the exact cropping. Thus, the properties **`background-position-x`** and **`background-position-y`** were joined into a single property (**`background-position`**) which receives only the value **`top center`**, i.e., **`top`** on the Y axis and **`center`** on the X axis;
 - - Still regarding **background**, the properties **`background-repeat`** and **`background-size`** have been added with the values **`no-repeat`** and **`cover`** (respectively), so that the background image covers the whole available screen.  

