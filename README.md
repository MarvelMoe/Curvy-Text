# Curvy-Text
## A text animation Jquery dependent  plugin

This is a combination of lettering.js and textiallate.js. I've taken their code and removed the dependcies on each other, 
removed the optional "out effect" and combined it into 1 script. There is also no dependency on animate.css; you just add
a @keyframes rule and then define a class with the animation-name and animation-duration property in your css file. 
The goal was to reduce the amount of http requests; especially if you're just animating a single element.



##  Usage
- Define @keyframes rule and animation class 
 ```
 /* The animation code */
@keyframes rule-example {
    0%   {
     opacity: 0.5;
     transform: rotateX(90deg)
     }
    100% {
     opacity: 1;
     transform: none
    }
}

/* The element to apply the animation to */
.target-element {
    animation-name: rule-example;
    animation-duration: 4s;
}

  ```
- Add jquery and curvy-text.js files
- Add the following function after scripts

     ```  $(function() {
            $('.target-element').curvy({ in : {
                    effect: 'animation-class'
                }
            });
        
 - Options(these are default settings)
 ```
      delayScale: 1.5,
      delay: 50,
      sync: false,
      reverse: false,
      shuffle: false,
      
   ##  Demo
   On a live site
   https://lalunainn.com
