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


### another main and most beautiful thing with sass is that is you can work by creating component 
rules to create file like component is 
underscore-filename.scss
(_header.scss) -> create file for all header css effects and to use it import like in react does
<code>@import './header';</code> // importing, we dont need the extension .scss it will recognize automatically


## FUNCTIONS " MIXINS" MIXINS IS LIKE FUNCTIONS IN JS

<p>syntax</p>
<code>
@mixin functionName {
    <!-- add your effect here what you want to put  -->
    <!-- i'm puttin' display flex all property inside functions, header.scss -->
}
<p>To use it </p>
<code>
@include flexCenter(); // @include functionName();
</code>

</code>

## ADD CUSTOM PARAMETERS BY ADDING PARENTHESIS WITH FUNCTION

<P>syntax </P>
<code>
@mixin functionName(add_parameter){
<!-- adding parameter is just creating variable so to create variable use dololar sign ($) with variable name -->
}
</code>

<span>Overall</span>
<code>
@mixin flexCenter($direction){
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    flex-direction: $direction; // now just use direction where you want to use and put value i.e $direction: column;
}

</code>

<p>
and now you can use it differently for every places
<code>
@mixin flexCenter($direction, $background){
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    flex-direction: $direction;
    background: $background;
}

<!-- to use it -->
@include flexCenter(column,red); //inside header, and can change for button 
</code>
 </p>