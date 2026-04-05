# Seatwork #2 - Getting to know CSS Position and z-index.
### This seatwork will ask you to implement the different CSS position on a given code.
### short link to this .md file is: https://bit.ly/4c61P9K
#### Resources (also found in Khub week 5)
- [4 Minute Youtube Video on CSS Position](https://www.youtube.com/watch?v=YEmdHbQBCSQ)
- [CSS Position Tutorial](https://roycan.github.io/CssPositioningZIndexLab/)

### Instructions: 
1. This is individual submission in khub, but you can work with a partner.  When you submit in khub please place both your names in the submission bin.
2. Guided Activity (30 minutes), please follow what is being required.  

    - Make a copy of this .md file to your Q4 repository and name it as **SectionLNseatwork2.md** example **9LiCruzSeatwork2.md**. Place it in your q4 repository vscode local computer. Committing frequently to your Github repository.  
    - Copy the code below and paste it inside a new file (name it as SectionLNseatwork2.html). Place this file in the same location where the .md file is saved. 
    - Change the content values of the meta tags to your names for author/s and the date today for revised.
    - Please do the following tasks that will ask you to reposition HTML elements then answer the guided question for each task on the .md file. Commit changes to the .md file and to the .html file as well.
    **- This seatwork is worth 20pts and should be submitted by the end of the period** The link to [KHub submission bin](https://khub.mc.pshs.edu.ph/mod/assign/view.php?id=15481).
      - Submit the links to your .md file and .html file.

```html
<!DOCTYPE html>
<html>
<head>
  <meta name="author" content="<your names>" />
  <meta name="revised" content="<date today>" />
  <style>
    body { font-family: Arial, sans-serif; }
    .header, .footer {
      background: lightblue;
      padding: 10px;
    }
    .footer {
       opacity: 0.5;
    }
    .sidebar {
      background: lightgreen;
      width: 150px;
      height: 200px;
    }
    .content {
      background: lightyellow;
      width: 300px;
      height: 200px;
    }    
  </style>
</head>
<body>
  <div class="header">Header</div>
  <div class="sidebar">Sidebar</div>
  <div class="content">Main Content</div>
  <div class="footer">Footer</div>
</body>
</html>
```
### Step 1 (Static vs Relative):

- Add in css ```position: relative; top: 20px; left: 20px;``` to .sidebar.

- Guided Question: What changed compared to the default static positioning? Try to give different values to top and left or you can change it to bottom, right.
- I noticed that it does the opposite of what you put, like when you put top 20px it goes 20px down. But the layout behind it appeared to not change.

### Step 2 (Fixed):

- Add in css ```position: fixed; bottom: 0; width: 100%;``` to .footer.

- Guided Question: What happens when you scroll the page? Why does the footer behave differently from position relative?
- I noticed that it sticks to the bottom no matter how much I scroll. It doesn't go up or down, unlike position relative wherein it moves within the page layout.


### Step 3 (Absolute):

- Add in css ```position: absolute; top: 66px; left: 200px;``` to .content.

- Guided Question: What is the effect of position: absolute on an element? How is it different from fixed?
- I noticed that it moves to  a specific part of the page and it overlaps with other elements as well. But it doesn't stay stuck to the screen and can still disappear when I scroll.

### Step 4 : (Absolute)

- Add in html ```<div class="notice">Notice!</div>``` and include the css below:

```css
.notice {
    position: absolute;
    top: 60px;
    left: 400px;
    background: orange;
    padding: 10px;
    z-index: 2;
}
```

- Give .content a z-index: 1.

- Guided Question: Why does the notice appear on top of the content? What happens if you swap the z‑index values?
- The notice seems to stay on top of the content because it has a higher z-index value. If I swap the values, it seems to go under the main content.

- Challenge: 
    * What changes that you have to do on the code that will position .notice box on the top right corner of the .content box? Please write the code on paper as well (both html and css on the part of .notice and .content).
    * Try to change the position of .content to relative then to fixed. What do you observed each time?
    - When I changed it to relative, it stays in the layout and I could move it slightly based on the values of top and left. With fixed, though, it does not move when scrolling and it becomes attached to screen.
    * What do you observe on about the effect of z-index on .notice and .content boxes?
    -The z-index controls which element appears on top. I noticed higher z-index values make the element appear more on the front, while lower ones make them appear more on the bottom or appear less.

3. Please answer the following reflection questions (15 minutes)

    a. Could you summarize the differences between the CSS position values (static, relative, absolute, fixed)? 

    - Static position value is the default one, and it makes it stay on its normal layout. Relative moves the object a bit from its original spot by the opposite (top; 20px moves it 20px to the bottom instead of to the top). Absolute places it exactly on a position and removes it from the original layout. Fixed positioning makes it fixed to the screen and it cannot be removed by scrolling.

    b. How does absolute positioning depend on its parent element?

    - Position: absolute is placed relative to the nearest parent with a position (like relative/absolute/fixed).

    c. How do you differentiate sticky from fixed (you can research on sticky)?
    - Position: sticky makes an element act normal at first, but when you scroll to or reach a certain point it becomes fixed. Unlike fixed, it only sticks within its parent container and stops when the parent ends.

    d. If you were designing a webpage for a school event, how might you use positioning to highlight important information? Please give concrete examples.

    - Positioning can be very useful in displaying important information. For example, I can use position: fixed to make an emergency announcements in case there is a natural disaster during an event unscrollable, positioned at the center of a page and viewable by all. We can also apply this same principle for important details a viewer must know at all times when accessing a website, which we can fix to a sidebar or a section near the top of a page.
