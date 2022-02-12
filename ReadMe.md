### Install Sass Compiler from vs code extension because browser cannot read Sass it only can read CSS

## Write all your css in .scss file and after that at bottom you'll see  watch scss button, just click it and it will create style.css in the same folder

####### Now link the normal css into your html file 
anything you write inside scss file will now automatically generate css inside .css file after saving

## WHAT WE CAN CREATE WITH SASS

-- create variables
benefits of creating variables is it helps you to make changes from one places for every same effects that is used as in case of primary btn we just need to change color of variable instead of going to each and every elements 

** Nesting different things
this means rather than writing header , and header button for selecting we can directly add button inside header that is instead of this 

<!-- code -->
header{
    background: lightblue;
    display: flex;
    justify-content: center;
    color: $textColor;
}
header button{
    background: $primaryBtn;
}
<!-- code ends -->

we can write this
header{
    background: lightblue;
    display: flex;
    justify-content: center;
    color: $textColor;
    button{
        background: $primaryBtn;
    }
}


** Now what if i want to add hover for button 
you can use like 
&:hover{
    background:red;
}
and same thing for after and before pseudoclasses

for these type of effects just use the "& " symbol and just use the colon " : " or " :: "