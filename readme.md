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



