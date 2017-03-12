# W3 Resource Exercises notes

One Paragraph of project description goes here

## Javascript

1) Write a JavaScript program to display the current day and time in the following format.
```
function timeconvert(time)
      {
       if(time <= 12)
       {
         return time+" AM";
       }
        else
       {
         
         return (time-12)+" PM"; 
       }
      }
    var today= new Date();
    var day=['Sunday','Monday','Tuesday','Wednesday','Thursday','Friday','Saturday']
    var time=timeconvert(today.getHours())+":"+today.getMinutes()+":"+today.getSeconds();
    document.write("Today is "+day[today.getDay()]);
    document.write("Current time is:"+time);

```
* Calling the javascript Date() method directly without making a new object, the current date will be returned in string format.
* we can create a new object using var date = new Date(). further, we can call different methods such as getHours(), getMinutes() and getSeconds().

2) Write a JavaScript program to print the contents of the current window.

```
   <script type="text/javascript">
     window.onload = function()
     {
       var button=document.querySelector('button');
        button.addEventListener('click',function(){
          window.print();
        })
     };
  </script>

```
* to load the javascript after the html page has been loaded, we have to use window.onload function.
* window.print() is used to print the current window of a website screen.

3) Write a JavaScript program to print the contents of the current window.

```
   <script type="text/javascript">
     window.onload = function()
     {
        var today=new Date();
        var date= today.getDate();
         if(date <10)
           {
             date='0'+date;
           }
        var month = today.getMonth();
         if( month < 10)
           {
             month='0'+month;
           }
        var year=today.getFullYear();
        document.write(month+'-'+date+'-'+year);
       document.write(month+'/'+date+'/'+year);
       document.write(date+'/'+month+'/'+year);
         
     };
  </script>
```
* getDate(), getMonth() and getFullYear() returns the required fild however, important thing to note that, in javascript month starts with 0.
* Important thing to note here is getFullYear will return the value of the year in 4 digit, but not getYear().

4)  Write a JavaScript program to find the area of a triangle where lengths of the three of its sides are 5, 6, 7..

```
   <script type="text/javascript">
     window.onload = function()
     {
      var a=5,b=6,c=7;
      var p= (a+b+c)/2;
      var area= Math.sqrt(p*((p-a)*(p-b) *(p-c)));
      document.write(area);
     };
  </script>
```
* squrt() function is used to find square root.

5)  Write a JavaScript program to rotate the string 'w3resource' in right direction by periodically removing one letter from the end of the string and attaching it to the front.

```
<script type="text/javascript">
     window.onload = function()
     {
       function animate()
       {
         var text=document.querySelector('h1').textContent;
         document.querySelector('h1').textContent=text.charAt(text.length-1)+text.slice(0,text.length-1);
       }
       setInterval(function() {animate()},500);
      
     };
  </script>
```
* textContent called on the queryselecotor will return the text contents.
* Slice method is used to cut the string. 

6) Write a JavaScript program to determine whether a given year is a leap year in the Gregorian calendar

```
<script type="text/javascript">
<script type="text/javascript">
       window.onload = function()
       {
       document.querySelector('button').addEventListener('click',function(){
       var value=  document.querySelector('input').value;
       if( isNaN(value) == true)
         {
            alert("Not a Number!")
         }
      else
         {
            if((value/4) % 2 == 0)
              {
                if((value/100) % 2 ==0 )
                  {
                    if((value/400) % 2 ==0)
                      {
                        console.log("It is a leap year!")
                      }
                    else
                      {
                        console.log("Nope!")
                      }
                  }
                else
                  {
                    console.log("It is a leap year");
                  }
              }
           else
             {
               console.log("Nope!");
             }
         }
      
       })
       }
  </script>
  </script>
```
* If the number is divided by 2 then it is a even number. Here % function will return 0 if the number can be devided by 2
* isNAN(value) will check whether the given value is a number or not;


7) Write a JavaScript program to find 1st January is being a Sunday between 2014 and 2050.

```
window.onload = function()
       {
         for(var i=2014 ; i<=2050; i++)
          {
          var findday = new Date('Janruary 01, '+i)
          if(findday.getDay() == 0)
            {
              console.log(findday.toDateString());
            }
          }
       }
```
* The date function will take parameters in multiple string/int formate check MDN/W3 site.
* The toDateString() method return the date in string format.

8) Write a JavaScript program to find 1st January is being a Sunday between 2014 and 2050.

```
  <script type="text/javascript">
       window.onload = function()
       {
         var randnum= Math.floor((Math.random() * 10)+1) ;
         console.log(randnum);
          var num=prompt("Enter a Number between 0 to 10");
         if(randnum === num)
           {
             alert("You got it!");
           }
         else
           {
             alert("Opss! is was"+randnum);
           }
       }
  </script>

```
* Here Math.random number will generate random numbers between 0 to 1(exclusive).
* Floor function will round off the number to its nearst integer.
* ceil will round off floating number to nearst interger.

9)  Write a JavaScript program to calculate days left until next Christmas.

```
  <script>
  window.onload = function()
  {
    var dayinmillsec= 24 * 60 * 60 *1000;
    var today=new Date();
    var next=new Date('26 December, 2017');
    console.log(Math.round((next - today) / dayinmillsec));
  }
  </script>

```
* If we directly take the difference between two dates, it will return the difference in number of milliseconds;
* If we divide the total diffence by the 1 day milliseconds we will get the total days.
* 24 *60 *60 * 1000 (milliseconds) -> 1 day
   Diffencebetweentwodates (milliseconds) -> ?

10)  Write a JavaScript program to calculate multiplication and division of two numbers (input from user).

```
 <script>
  window.onload = function()
  {
    var buttons=document.querySelectorAll('button');
    var ans=document.getElementById('ans');
    buttons[0].addEventListener('click',function(){
    var num=document.querySelectorAll('input');
    ans.textContent = "The result is:"+parseInt(num[0].value) * parseInt(num[1].value);
    });
    buttons[1].addEventListener('click',function(){
    var num=document.querySelectorAll('input');
    ans.textContent = "The result is:"+parseInt(num[0].value) / parseInt(num[1].value);
    }); 
  }
  </script>

```
11) Write a JavaScript program to get the website URL (loading page).
```
 <script>
  window.onload = function()
  {
alert(document.URL);
  }
  </script>

```
*A Document object represents the HTML document that is displayed in that window. The Document object has various properties that refer to other objects which allow access to and modification of document content.


 




