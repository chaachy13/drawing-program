color ink, black=#000000;
float drawingSurfaceX, drawingSurfaceY, drawingSurfaceWidth, drawingSurfaceHeight;
//float drawingDiameter;
Boolean draw=false;

void setup() {
  size(500, 600);
  quitButtonSetup();
  drawingSurfaceX = width*0;
  drawingSurfaceY = height*0;
  drawingSurfaceWidth = width*3/4;
  drawingSurfaceHeight = height*4/5;
  //
  ink = black; // example to change ink
  //drawingDiameter = width*1/100;
  //
  rect(drawingSurfaceX, drawingSurfaceY, drawingSurfaceWidth, drawingSurfaceHeight);
}

void draw() {
  quitButtonDraw();

  if (draw == true) {
    fill(ink);
    line(mouseX, mouseY, pmouseX, pmouseY);
  }
}

void mousePressed() {
  quitButtonMouseClicked();
  if ( mouseX>drawingSurfaceX && mouseX<drawingSurfaceX+drawingSurfaceWidth && mouseY>drawingSurfaceY && mouseY<drawingSurfaceY+drawingSurfaceHeight ) {
    println("drawing surface");
    if (draw == false) {
      draw = true;
    } else {
      draw = false;
    }
  }
}
void setup() {
  size(640, 360);
  background(102);
}

void draw() {
  stroke(255);
  if (mousePressed == true) {
    line(mouseX, mouseY, pmouseX, pmouseY);
  }
}
String title= "X";
PFont quitButtonFont;
color purple = #2C08FF; //Ink
color purpleQuitButton = #FFDBFB;
color yellowQuitButton = #FEFFDB;

void quitButtonRect() {
  rect(width*19/20, height*0, width*1/20, height*1/20);
}
void quitButtonSetup() {
  quitButtonFont = createFont ("Harrington", 55); //Must also Tools / Create Font / Find Font / Do Not Press "OK"
  quitButtonRect(); //Quit Button
}

void quitButtonDraw() {
  //HoverOver
  if (mouseX >= width*19/20  && mouseX <= width && mouseY >= height*0 && mouseY <= height*1/20) {
    fill(yellowQuitButton);
    quitButtonRect();
  } else {
    fill(purpleQuitButton);
    quitButtonRect();
  }

  //Text in Quit Button
  fill(purple); //Ink, hexidecimal copied from Color Selector
  textAlign (CENTER, CENTER); //Align X&Y, see Processing.org / Reference
  //Values: [LEFT | CENTER | RIGHT] & [TOP | CENTER | BOTTOM | BASELINE]
  textFont(quitButtonFont, 20); //Change the number until it fits, largest font size
  text(title, width*19/20, height*0, width*1/20, height*1/20);
  fill(255); //Reset to white for rest of the program
}

void quitButtonMouseClicked() {
  if (mouseX >= width*19/20  && mouseX <= width && mouseY >= height*0 && mouseY <= height*1/20) {
    exit();
  }
}
