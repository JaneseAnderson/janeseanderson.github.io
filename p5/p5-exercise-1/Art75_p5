let carX = 50;
let vroom;
let carSpeed = 3;
let carAcc = .1;

function setup() {
  createCanvas(500, 500);
  vroom = new p5.Oscillator('square');
  vroom.start();
}

function draw() {
  background(50, 25, 105, 3);

  rect(0, height - 20, 20, 20);

  vroom.freq(40 + mouseX);

  if (frameCount > 120) {


    if (carX >= 500) {
      carX = -50;
      carSpeed = 3;
    } else {
      carSpeed += carAcc;
      carX += carSpeed;
    }
  }

  noStroke();
  fill(255, 50, 50);
  triangle(carX, 50, carX + 60, 80, carX, 80);

  fill(0);
  ellipse(carX, 80, 20, 20);
  ellipse(carX + 50, 80, 20, 20);
}

function mousePressed() {
  vroom.start();
}
function mouseReleased() {
  vroom.stop();
}
