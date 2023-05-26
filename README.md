# CHEATSHEET for JS

## if/else conditions 
> broken down into pieces and used to create an if-else statement 

### Problem 1
All of the animals are having a feast! Each animal is bringing one dish. There is just one rule: the dish must start and end with the same letters as the animal's name. For example, the great blue heron is bringing garlic naan and the chickadee is bringing chocolate cake.

Write a function feast that takes the animal's name and dish as arguments and returns true or false to indicate whether the beast is allowed to bring the dish to the feast.

Assume that beast and dish are always lowercase strings, and that each has at least two letters. beast and dish may contain hyphens and spaces, but these will not appear at the beginning or end of the string. They will not contain numerals.

#### Solution/Explanation
```js
// hardcoded version
// bf - beast firstletter
// dl - dish lastletter
// df - dish firstletter
// bl - beast lastletter
// used placeholder.at() method to get the position of characters

const bf = beast.at(0)
const bl= beast.at(-1)
console.log(bf, bl )

const df = dish.at(0)
const dl =  dish.at(-1)
console.log(df, dl)

const firstChar = bf == df
console.log(firstChar)

const lastChar = bl == dl
console.log(lastChar)

const conditions = firstChar ==  lastChar
console.log(conditions)
return conditions
```

#### Solution/Function
```js
function feast(beast, dish) {
  
  if (beast.at(0) == dish.at(0) && beast.at(-1) == dish.at(-1) ){
    return true
  } else {
    return false
  }
}
```

### Problem 2
The male gametes or sperm cells in humans and other mammals are heterogametic and contain one of two types of sex chromosomes. They are either X or Y. The female gametes or eggs however, contain only the X sex chromosome and are homogametic.

The sperm cell determines the sex of an individual in this case. If a sperm cell containing an X chromosome fertilizes an egg, the resulting zygote will be XX or female. If the sperm cell contains a Y chromosome, then the resulting zygote will be XY or male.

Determine if the sex of the offspring will be male or female based on the X or Y chromosome present in the male's sperm.

If the sperm contains the X chromosome, return "Congratulations! You're going to have a daughter."; If the sperm contains the Y chromosome, return "Congratulations! You're going to have a son.";

#### Solution/Explanation
```js
function chromosomeCheck(sperm) {
     if(sperm == 'XX') {
       return ('Congratulations! You\'re going to have a daughter.')
     }  else {
       return ('Congratulations! You\'re going to have a son.')
     }
      
}
```

###Best Practice
```js
function chromosomeCheck(sperm) {
  return `Congratulations! You're going to have a ${sperm === 'XY' ? 'son' : 'daughter'}.`
}
```