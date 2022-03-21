class Button {
  constructor() {
    this.shape = 2;
    this.x = 100;
    this.y = 100;
    this.color = color(255, 0, 255);
    this.hovercolor = color(0, 255, 0);
    this.size = 50;
    this.hover = false;
    this.triggered = false;
  }

  display() {
    noStroke();
    if (this.hover == 0) {
      fill(this.hovercolor);
    } else {
      fill(this.color);
    }
    if (this.shape == 1) {
      rect(this.x, this.y, this.sixe, this.sixe);
    } else {
      circle(this.x, this.y, this.size);
    }
  }

  checkTrigger() {
    if (this.shape == 1) {
      // rectangle

      if (
        mouseX > this.x &&
        mouseY < this.x + this.size &&
        mouseY > this.y &&
        mouseY < this.y + this.size
      ) {
        this.hover = true;
      } else this.hover = false;
    } else if (this.shape == 2) {
      // circle

      if (dist(this.x, this.y, mouseX, mouseY) < this.size / 2) {
        this.hover = true;
      } else this.hover = false;
    }
    if (mouseIsPressed && this.hover) {
      this.triggered = true;
    }
  }
}

var button;
var altColor = false;

function setup() {
  createCanvas(400, 400);

  button = new Button();
  col = color(220);
}

function draw() {
  if (altColor) background(100, 0, 255);
  else background(220);

  button.checkTrigger();
  button.display();
}

function mousePressed() {
  if (button.hover) altColor = !altColor;
}
