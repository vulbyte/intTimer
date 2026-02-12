# intTimer

this is a pretty simple class, i just use it in a bunch of places so i thought it would be best to make a reference for it as it's pretty stable from my experience so far.

the whole timer has an okay amount of comments so it's probably easier to skim the class itself then read this, but for anyone who's new here's the tldr of how to use the timer:

## tutorial

say you have a function like this you want to print every say 7 seconds:

```js   
function RestateLoveOfTacos(){
    console.log("i love tacos! 🌮");
}
```

what you do is you bind the function to the timer after declaring it like so:
```js 
/* with your declarations */
import {IntTimer} from /location/to/file/intTimer.mjs
timer = new IntTimer({
    timeoutDuration: 7
});

/* a bunch of code probably */ 

timer.AddTimeoutListener(RestateLoveOfTacos);
/*                                         ↑
note the lack of "()", ____________________」
this is a common issue people do as a mistake.
*/
```

## faq

why not use .js instead of .mjs?
> all browsers have supported emca6 aka .mjs files since 2014ish, the last major browser to not support emca6 was internet explorer. and if i ever wish to use emca6 features to expand this class in the future i would rather force compatibility now than later.

isn't this inefficent compared to X method?
> yeh there's defo better and faster methods, but this method imo is very extensible and easy to reason about, so this is one of the few times where imo the DX is signifigantly better to the point of eating the inefficiencies.
