
//things that need to be fixed:
//reading 10 registers as a 1 as it is two characters and reads the first
//main game loop reads cards twice (need to iterate by 2 without breaking it (i / i+1))

let notNull = false;
let unShuffled = ["Y1","Y2","Y3","Y4","Y5","Y6","Y7","Y8","Y9","Y10","R1","R2","R3","R4","R5","R6","R7","R8","R9","R10","B1","B2","B3","B4","B5","B6","B7","B8","B9","B10"];
let randomIndex;
//Red beats black
//Yellow beats red
//Black beats yellow


//Shuffling 
let deck = [null,null,null,null,null,null,null,null,null,null,null,null,null,null,null,null,null,null,null,null,null,null,null,null,null,null,null,null,null,null];

for (i = 0; i < 30; i++){

  while (notNull == false){
//Checks an random index for unshuffled, checks if it hasnt already been used (set to null) then keeps searching till it finds one and set it to the next index of deck
    randomIndex = Math.floor(Math.random() * 30);
    if (unShuffled[randomIndex] !== null){
      notNull = true;
    }  
  }

    deck[i] = unShuffled[randomIndex];
    unShuffled[randomIndex] = null;
    notNull = false;

}
console.log("deck");
for (i = 0; i < deck.length; i++){
console.log(deck[i]);
}
//End of shuffling

//"Gameplay"

let p1Cards = [];
let p2Cards = [];

//Returning true = player 1 wins false = player 2
function compareCards(p1, p2) {
//Compare on color
if (p1[0]== "R" && p2[0]=="B"){
  return true;
}
else if(p1[0]== "Y" && p2[0]=="R"){
  return true;
}
else if(p1[0]== "B" && p2[0]=="Y"){
  return true;
}

//Same color (numbers)
else if((p1[0]== "B" && p2[0]=="B") || (p1[0]== "R" && p2[0]=="R") || (p1[0]== "Y" && p2[0]=="Y")){
  if(p1[1] > p2[1]){
    return true;
  }
  else{
    console.log("lower");
    return false;
  }
}
else{
    console.log("else");
    return false;
  }
}

//End of compareCards

let player1Won;

for (i = 0; i < 29; i++){

console.log("twf sgtwtw ");
console.log(deck[i]);
console.log(deck[i+1]);
  
  player1Won = compareCards(deck[i],deck[i+1]);
  console.log(player1Won);
  
  if(player1Won == true){
    p1Cards[p1Cards.length - 1] = deck[i];
    p1Cards[p1Cards.length] = deck[i+1];
  }
  
  else{
    p2Cards[p2Cards.length - 1] = deck[i];
    p2Cards[p2Cards.length] = deck[i+1]; 
  }
}

console.log("player 1");
for (i = 0; i < p1Cards.length; i++){
console.log(p1Cards[i]);
}

console.log("player 2");
for (i = 0; i < p2Cards.length; i++){
console.log(p2Cards[i]);
}
