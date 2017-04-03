1) Write a JavaScript function that reverse a number.
```
function revNum(num)
{
  return parseInt(num.toString().split("").reverse().join(""));
}
console.log(revNum(123));
```
- Here, the input is number instead of a string. so first, we have used toString() method to convert into a string.
- In javascript, string object doesn't have a reverse method so first we need to convert it into an array we can use split function to do that.
- Now we can reverse the array and use join to join it back to string
- convert it into a number using parseInt()
2) Write a JavaScript function that checks whether a passed string is palindrome or not? 
```
function palindrome(inputString)
{
   var revString=inputString.split("").reverse().join("");
    
    if(inputString === revString)
      {
        return true;
      }
    else
      {
        return false;
      }
}

console.log(palindrome("JaJ"));
```
- always use strict === while comparing otherwise it will ignore the datatype

3)  Write a JavaScript function that generates all combinations of a string


4) Write a JavaScript function that returns a passed string with letters in alphabetical order.
5) Write a JavaScript function that accepts a string as a parameter and converts the first letter of each word of the string in upper case.
```
function firstLetter(inputString)
{
 var arrayWord=inputString.split(" ");
 var newWordArray=arrayWord.map(function(each){
   return each.charAt(0).toUpperCase() + each.slice(1); 
  });
  return newWordArray.join(" ");
}
console.log(firstLetter("the quick brown fox"));
```

6) Write a JavaScript function that accepts a string as a parameter and find the longest word within the string.

```
function longestWord(words)
{
  var wordArray=words.split(" ").sort();
  return wordArray[0];
}

console.log(longestWord('Web Development Tutorial'));

```

- we can directly sort the array using sort() method.


7) Write a JavaScript function that accepts a string as a parameter and counts the number of vowels within the string.

```
function vovels(words)
{
  var vovels=['a','e','i','o','u'];
  var charArray=words.split("");
  var vovelsArray=[];
  charArray.forEach(function(each){
    
    if(vovels.includes(each.toLowerCase()))
      {
        vovelsArray.push(each);
      }
     
  })
  return vovelsArray.length;
}

console.log(vovels('The quick brown fox'));

```
- we can use array.includes(string) method to check whether the char is in the array or not.


8) Write a JavaScript function that accepts a number as a parameter and check the number is prime or not.

- first of remember that 1 is not a prime number, 2 is a prime number. If the number is a factorial of any number except 1 and itself then it is considered nonprime number.

```

function primeCheck(num)
{
  if(num === 1)
    {
      return "It is not a prime number"
    }
  else if (num == 2)
    {
      return "It is a prime number"
    }
  else
    {
      for(var i=2;i<num;i++)
        {
          if(num % i === 0)
            {
              return "The Number is not a prime number"
            }
        }
      return "It is a prime number"
    }
}

console.log(primeCheck(7));

```
9) Write a JavaScript function which accepts an argument and returns the type. 

```
function objtype(obj)
{
 return typeof(obj);
}

objtype("abc");

```
10) Write a JavaScript function which returns the n rows by n columns identity matrix.

```
My Solution:

function matrix(num)
{
  var array=[]
  for(var i=0;i<num ;i++)
    {
      for(var j=0;j<num;j++)
        {
          if(i!== j)
            {
             array[j]=0; 
            }
          array[i]=1;
        }
      console.log(array.join(""));
    }
}
matrix(4)

Better solution:

function matrix(num)
{
  var m=new Array(num);
  for(var i=0;i<num;i++)
    {
      m[i]= new Array(num).fill(0);
      m[i][i] = 1;
    }
  
  console.log(m);
}
matrix(4)

```
- to define array size in while defining use new Array(size) method (e.g var j= new Array(3)) 
- array.fill(0) method will fill the array with 0


