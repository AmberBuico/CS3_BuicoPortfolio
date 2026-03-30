# Seatwork #2: CSS Position and z-index

**Name:** [Your Name]  
**Partner:** [Partner's Name]  
**Date:** March 30, 2026

----------------------------------------------------------

### Step 1 (Static vs Relative)
**Guided Question: What changed compared to the default static positioning?**

Honestly, at first, I didn't think much would happen, but when I added position: relative, the sidebar just... drifted. It moved 20px down and 20px to the right, but the weirdest part was that it didn't push the "Main Content" box away. It's like the sidebar left its "ghost" in the original spot so the rest of the page still thinks it's there, while the actual box is just hovering somewhere else. When I messed with the values (like making top 50px), it just kept sliding further away from its homeeeee.

### Step 2 (Fixed)
**Guided Question: What happens when you scroll the page? Why does the footer behave differently?**

This one is actually super cool (!!!) because the footer literally refuses to move. No matter how much I scroll up or down, it’s just glued to the bottom of my screen. It’s totally different from relative because relative is based on where the element *used* to be, but fixed doesn't care about the page layout at all, it only cares about the browser window. It's like that one sticky note on your monitor that stays there even if you change the paper behind it.

### Step 3 (Absolute)
**Guided Question: What is the effect of position: absolute? How is it different from fixed?**

When I set the content to absolute, it felt like the box just broke free from the rest of the group. It jumped to exactly top: 66px and left: 200px. The big difference from fixed is that if I had enough content to scroll, the absolute box would actually move away as I scrolled up, while fixed would stay stuck to my eyes. It feels more "attached" to the page itself rather than the screen.

### Step 4 (z-index)
**Guided Question: Why does the notice appear on top? What happens if you swap the values?**

The notice is on top because its z-index is 2, while the content is only 1. It’s basically just a layering system—higher numbers mean you're "closer" to the person looking at the screen. If I swap them and give the content a 2 and the notice a 1, the notice actually disappears behind the yellow box! It’s like putting a folder on top of a paper; the one on top is the only one you can fully see.

----------------------------------------------------------

### Challenge & Reflections

**The Top-Right Challenge:**
To get the notice in the top-right of the content, I'd have to put the <div class="notice"> *inside* the <div class="content"> in the HTML. Then, I'd set the content's position to relative (so it acts as a boundary) and set the notice to position: absolute; top: 0; right: 0;. This makes the notice "stick" to the corner of its parent box instead of the whole page.

**Reflection Questions:**
* **a. Summary:** static is just the boring default. relative is for small nudges. absolute is for placing things exactly where you want them in a container, and fixed is for stuff like navbars or footers that you never want to disappear when scrolling.
* **b. Parent Dependency:** absolute is kind of a "lost child" until it finds a parent that has a position like relative or absolute. If it doesn't find one, it just uses the whole body of the page as its guide.
* **c. Sticky vs Fixed:** fixed is stuck from the very start. sticky is more like a hybrid...it acts normal until you scroll to it, and *then* it sticks to the top like it's glued there until you scroll past its section.
* **d. School Event Design:** If I were making a page for something like the "Himig Agham" concert (I LOVE OUR CONCERT!!!!), I’d use fixed positioning for a "Buy Tickets" button so people can always see it. I’d also use absolute positioning to put a "LIVE NOW" badge right on top of the event poster image to make it pop and look professional.