# CHEATSHEET for JS

## if/else broken down into pieces and used to create an if-else statement 

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


//   const bf = beast.at(0)
//   const bl= beast.at(-1)
//   console.log(bf, bl )
  
//   const df = dish.at(0)
//   const dl =  dish.at(-1)
//   console.log(df, dl)

//   const firstChar = bf == df
//   console.log(firstChar)
  
//   const lastChar = bl == dl
//   console.log(lastChar)
  
//   const conditions = firstChar ==  lastChar
//   console.log(conditions)
//   return conditions
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