1) Test if jQuery is loaded.

```
<script>
    $(document).ready(function(){
      console.log("ready");
    });
  </script>

```

2) Scroll to the top of the page
    $(document).ready(function(){
      $('button').on("click",function(){
        $('html, body').animate({scrollTop:0},'slow')
      
      })
    });

