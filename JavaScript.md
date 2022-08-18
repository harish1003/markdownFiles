# JAVASCRIPT
*javascript is the dynamic programming language that is used to build web applications and in also game development. It allows us to implement the dynami features on the web page which cannot achieved by the css/html alone.*

> <script>..</script> javascript code is written in between this tags
* ALL files are stored in the same folder { example on how to use css and javascript in the html context }


    >  HTML FILE 
    <!DOCTYPE html>
    <html>
    <head>
    <link rel="stylesheet" href="cssfile.css">
    <h1 id="head1"> It will change when you click try button </h1>
    <h1 id="head2"> Font size will change</h1>
    </head>
    <body>
    <hr/>
    <div id="div3"> I will be visible only when you click the button</div>
    <button type="button"
        onclick="myFunc()"> Try to see how javascript changes the html content </button>
    <button type="button"
        onclick="changeFont()"> Click to change Font Size </button>
    <button type="button"
        onclick="toggle()"> Click to toggle the view </button>
    <script src="javascript.js"> </script>
    </body>
    </html>
    
    >cssFile.css
    #div3{ background-color : powderblue;}
    h1{ background-color : red;}
    body{ background-color: powderblue;}
    
    >javascript.js
      function myFunc(){
         document.getElementById("head1").innerHTML = "Demo tutorial For JavaScript";
        }
        
        function changeFont(){
         document.getElementById("head2").style.fontSize="35px"
         document.getElementById("head2").style.backgroundColor="red"
        }

        function toggle(){
           var x = document.getElementById("div3");
           if(x.style.display === 'none'){
            x.style.display = 'block'
           }
           else {
            x.style.display = 'none'
            }
        }
* 
     
