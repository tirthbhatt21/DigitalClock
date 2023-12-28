![MasterHead](http://www.pramukhdigital.com/wp-content/uploads/2018/07/New-PNC-Animated-Banners.gif)
<div style="background:#2a2a2a;color:#fff;height:100%;width:100%;font-family: 'Fira Code';padding-left:20px;">
Created On: 28 December 2023 [Thursday]
    
***


# Description

- Digital Clock.<br/>
- here webpage has made for study & demonstration or understand how Digital Clock work.<br>



    
=========================<br>
[𝙲𝚕𝚒𝚌𝚔 𝙼𝚎 𝙵𝚘𝚛 𝙻𝚒𝚟𝚎 𝙳𝚎𝚖𝚘](https://raw.githack.com/tirthbhatt21/DigitalClock/main/Digital%20Clock/index.html) 
<br>=========================

Here I shared about used technologies and so on...

<details>
    <summary> Technologies </summary>

***

- [HTML](http://www.w3schools.com/html/default.asp) - A markup language for describing web documents.

- [CSS](http://www.w3schools.com/css/default.asp) - A style sheet language used for describing the look and formatting of a document written in a markup language.

- [Java Script](http://www.w3schools.com/js/default.asp) - A programming language of the Web.

<hr/>
</details>

<details>

<summary> Source Code </summary>

index.html
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Digital Clock - Tirth Bhatt || Developer ❤</title>
    <link href="style.css" rel="stylesheet">
    <link rel="icon" type="image/x-icon" href="logo.svg">
</head>
<body>
    <div class="clock-container">
        <div class="clock-col">
          <p class="clock-day clock-timer">
          </p>
          <p class="clock-label">
            Day
          </p>
        </div>
        <div class="clock-col">
          <p class="clock-hours clock-timer">
          </p>
          <p class="clock-label">
            Hours
          </p>
        </div>
        <div class="clock-col">
          <p class="clock-minutes clock-timer">
          </p>
          <p class="clock-label">
            Minutes
          </p>
        </div>
        <div class="clock-col">
          <p class="clock-seconds clock-timer">
          </p>
          <p class="clock-label">
            Seconds
          </p>
        </div>
      </div>

<footer>
  <p class="cells">Developed By <a href="https://github.com/tirthbhatt21"><span style="text-decoration: underline;">Tirth Bhatt</span></a> with ❤️</span></p>
     
  </footer>
      <script src="main.js"></script>
      <script src="moment.min.js"></script>
</body>
</html>
```
style.css
```css
@import url(Fonts/font.css);
.clock-day:before {
    content: var(--timer-day);
}
.clock-hours:before {
    content: var(--timer-hours);
}
.clock-minutes:before {
    content: var(--timer-minutes);
}
.clock-seconds:before {
    content: var(--timer-seconds);
}
body {
    background-image: linear-gradient(to right top, #ff5e5e, #ea4370, #cb3180, #a42d8c, #733091, #5a2d90, #3c2b8d, #00298a, #002288, #021a85, #061082, #0c027f);
    font-family: "Montserrat", "sans-serif";
    height: 98.1vh;
    display: flex;
    align-items: center;
    justify-content: center;
}
.clock-container {
    margin-top: 30px;
    margin-bottom: 30px;
    background-color: #080808;
    border-radius: 12px;
    padding: 60px 20px;
    box-shadow: 1px 1px 5px rgba(255, 255, 255, 0.15), 0 15px 90px 30px rgba(0, 0, 0, 0.25);
    display: flex;
}
.clock-col {
    text-align: center;
    margin-right: 40px;
    margin-left: 40px;
    min-width: 90px;
    position: relative;
}
.clock-col:not(:last-child):before, .clock-col:not(:last-child):after {
    content: "";
    background-color: rgba(255, 255, 255, 0.3);
    height: 5px;
    width: 5px;
    border-radius: 50%;
    display: block;
    position: absolute;
    right: -42px;
}
.clock-col:not(:last-child):before {
    top: 35%;
}
.clock-col:not(:last-child):after {
    top: 50%;
}
.clock-timer:before {
    color: #fff;
    font-size: 4.2rem;
    text-transform: uppercase;
}
.clock-label {
    color: rgba(255, 255, 255, 0.35);
    text-transform: uppercase;
    font-size: 0.7rem;
    margin-top: 10px;
}
@media (max-width: 825px) {
    .clock-container {
        flex-direction: column;
        padding-top: 40px;
        padding-bottom: 40px;
   }
    .clock-col + .clock-col {
        margin-top: 20px;
   }
    .clock-col:before, .clock-col:after {
        display: none !important;
   }
}

@media (max-width: 825px) {
    footer .cells
    {
        font-size: 1.3rem;
    }
}

footer {
    border: 0.1rem #000 solid;
    border-left: 0;
    border-right: 0;
    position: fixed;
    bottom: 0;
    right: 0;
    left: 0;
    text-align: center;
    font-size: 1.3vw; 
    background-color: beige;
    margin: 1vw 1.2vw;
}

.cells {
    display: inline-block;
    border-right: 1vh #000 solid;
    
    text-align: center;

    
    padding: 0vw 0.5vw;
    margin: 0.5vw;
}

p:last-child {
  border-right: 0;
}
```
```javascript
document.addEventListener("DOMContentLoaded", () =>
  requestAnimationFrame(updateTime)
);

function updateTime() {
  document.documentElement.style.setProperty(
    "--timer-day",
    "'" + moment().format("ddd") + "'"
  );
  document.documentElement.style.setProperty(
    "--timer-hours",
    "'" + moment().format("k") + "'"
  );
  document.documentElement.style.setProperty(
    "--timer-minutes",
    "'" + moment().format("mm") + "'"
  );
  document.documentElement.style.setProperty(
    "--timer-seconds",
    "'" + moment().format("ss") + "'"
  );
  requestAnimationFrame(updateTime);
}

```

</details>


*[Back to top](#description)*

<br/>
<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&pause=1000&color=1600F7&background=FFFFFF&center=true&vCenter=true&width=435&lines=Always+Learn+New+Things!+Keep+It+Up;Thank+You+%F0%9F%99%8F;Visit+Again...+%E2%9D%A4%EF%B8%8F" alt="Typing SVG" />


</div>
