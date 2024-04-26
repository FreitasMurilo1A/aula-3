let cor;
let circuloX; // horizontal
let circuloY; // vertical

function setup() {
  createCanvas(800, 800); // width x height
  background(color(180,520,10));
  cor = color(random(0,255), random(0,255), random(0,255));
  circuloX = [0,0,0];
  circuloY = [random(height), random(height), random(height)];
}

// circuloX = 0,0,0  
// circuloY = 300, 150 , 150




function draw() {
  
  fill(cor);
  
  //console.log (circuloX.length)
  
  for (let contador in circuloX) {
    // console.log (contador)
  circle(circuloX[contador], circuloY[contador], 30);  
  circuloX[contador] += random (3,3);
  circuloY[contador] += random (-6,6);
    
    if (circuloX[contador] >= width){
      circuloX[contador] = 0;
      circuloY[contador] = random(height);
    }
   
  }
 
  
  
  
  
  if (mouseIsPressed){
    cor = color(random(0,255), random(0,255), random(0,255), random(0,100));
  }
    
}
