---
layout: home
title: FPGA VGA Driver Project
tags: fpga vga verilog
categories: demo
---
Welcome to my FPGA VGA Project! In this project I designed a tropical GTA 6 inspired sunset , featuring a bright sun and palm trees, using Verilog and Vivado on a 640×480 VGA display.


## **Template VGA Design**
### **Project Set-Up**
The project began with a template in Vivado that featured rainbow colour strips vertically across the screen. I used it as a starting point to develop my own design

### **Template Code**
The original project template provided was called VGAColourStripes.v . This template generated eight colour strips across the VGA display. The code used row and col inputs to identify the position of each
pixel on the screen and if and else statements checked the column position and assigned different RGB values to each stripe to give the varying colours. The VGA interface works by scanning each pixel left to right before moving on to the next column. The VGA driver provides coordinates to the graphics module to decide what each colour pixel will be. I adapted the original conditional statements to create my GTA inspired backdrop.
<img src="https://raw.githubusercontent.com/Rrachar/FPGA-VGA-Driver-Project/main/docs/assets/images/1000050693.jpg">
### **Simulation**
Before synthesising , I used Vivado to simulate the Verilog code. The testbench applies clock and reset signals. I checked the output signal and pixel coordinates to make sure the correct RGB values were being
produced. This allowed me to identify errors before moving onto the next stage.


### **Synthesis**
After simulation I moved on to synthesis. Synthesis converts the Verilog code into a hardware representation that can be implemented on the FPGA. During the process Vivado checks the design and translates the Logic, including the background colours , the sun and the palm trees into resources that the Basys3 board can understand.
### **Demonstration**

These are the hardware components and the logic gates that are being used to create the design.
## **My VGA Design Edit**
For my design I had the idea of doing something I'm passionate about, video games, and what bigger game than GTA 6. I wanted to make something visually interesting that used different colours and simple shapes to 
create a retro sunset screen.
My design consists of three main features. Firstly I created a pink and orange colour gradient across the screen to represent the sky. I then added a yellowish / orange circle in the background to simulate the sun and lastly dotted about three blacked out silhouettes of palm trees to give that tropical climate vibe of Miami (the city the game was based on).
In terms of complexity, I felt this was very achievable since I was using basic mathematic equations and pixel coordinates.
I researched how VGA graphics can be generated using pixel coordinates and RGB colour values. This helped me understand how to create various shapes and colours.
### **Code Adaptation**
I adapted the original code by removing the if and else that displayed the vertical stripes and changed it so that the RGB values are calculated using the pixels Rows and Column coordinates. I added the Purple-pink-orange gradient by changing the RGB values on the row position of each pixel.
I then used  a simple mathematical equation to create a circle in the background which I'm using as the sun. For the Palm silhouettes I used conditional statements and different mathematical equations to control the position and shape of the trunk and leaves.
I kept the original clock, reset  and RGB register sections from the template as they were still needed to display the image on the VGA monitor.
### **Simulation**
Show how you simulated your own design. Are there any things to note? Demonstrate your understanding. Add a screenshot. Guideline: 1-2 short paragraphs.
### **Synthesis**  
After Synthesising my adapted VGA design. it was successfully converted into hardware logic from the FPGA. The synthesis results showed that the design used additional logic gates compared to the original template because i
introduced more calculations and conditional statements.
### **Demonstration**
I successfully implemented my GTA 6 retro styled sunset on the Basys3 FPGA.

## **More Markdown Basics**
This is a paragraph. Add an empty line to start a new paragraph.

Font can be emphasised as *Italic* or **Bold**.

Code can be highlighted by using `backticks`.

Hyperlinks look like this: [GitHub Help](https://help.github.com/).

A bullet list can be rendered as follows:
- vectors
- algorithms
- iterators

Images can be added by uploading them to the repository in a /docs/assets/images folder, and then rendering using HTML via githubusercontent.com as shown in the example below.

<img src="https://raw.githubusercontent.com/melgineer/fpga-vga-verilog/main/docs/assets/images/VGAPrjSrcs.png">
