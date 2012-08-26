Php-Pre-Printed-Forms
=====================

Printing on pre printed forms with php fpdf and jquery/jquery-ui

This is just proof of concept code that i put together with the help of code samples from various developer fourums. 
The code is very inefficient and only serves to illustrate the concept. 
I have only tested this on Firefox and IE on windows. 

To run this code you will need jquery, jquery-ui and fpdf to be available and you must change their paths and versions in the code files as required. 


Overview : 

* Every monitor has a DPI(dots per inch) setting that can be derived easily in a browser by rendering a 1x1 inch div and fetching its actual pixel values. 
* Using this pixel to inch ratio as the base, a grid is drawn on the screen to serve as the canvas. 
    (1/8 th of an inch in this case but it can be changed to 1/16 or 1/32 of an inch for higher accuracy)
* Draggable & Resizable divs are added to the grid and can be positioned in the exact x,y position by measuring the coordinates on the pre printed form and dragging the div to the corresponding position on the screen. 
* Once the positioning is complete the pixel positions as well as the other parameters like page size and orientation can be saved to a multi dimensional array and passed to php to create the pdf using fpdf. 
* Using fpdf it is possible to position the text in the exact position on the page by converting the pixel values of the div's back to inches using the ratio derived in the first step.
















