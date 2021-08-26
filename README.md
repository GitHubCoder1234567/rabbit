# rabbit
var garden,rabbit;
var gardenImg,rabbitImg;
var apples,applesImg;
var leaves,leavesImg;
function preload(){
  gardenImg = loadImage("garden.png");
  rabbitImg = loadImage("rabbit.png");
  applesImg = loadImage("apple.png");
  leavesImg = loadImage("orangeLeaf.png");
}

function setup(){
  
  createCanvas(400,400);
  
// Moving background
garden=createSprite(200,200);
garden.addImage(gardenImg);

//creating boy running
rabbit = createSprite(180,340,30,30);
rabbit.scale =0.09;
rabbit.addImage(rabbitImg);


apple=createSprite(100, 250, 25, 25);
apple.addImage(applesImg);
apple.scale=0.08;
}



function draw() {
  background(0);
  
  edges= createEdgeSprites();
  rabbit.collide(edges);

  drawSprites();
}

function createApples(){
apple=createSprite(random(50, 350),40,10,10);
}
var apples=Math.round(random(1,2));
if(frameCount % 80 ==0){
  if(apples == 1){
    apple=createSprite(random(50, 350),40,10,10);

  }
else{
  leaves=createSprite(random(50, 400,),40, 10, 10);

}
}



function createLeaf(){
  leaves=createSprite(random(50, 400,),40, 10, 10);
}
