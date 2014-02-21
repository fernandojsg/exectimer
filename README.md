# Description

Very simple nodejs module that can be used to track the time that diferent execution blocks took to execute in microseconds.

## Example

```javascript
 var t = require("proctimer");

 var myFunction() {
   var tick = new t.tick("myFunction");
   tick.start();
   // do some processing and end this tick
   tick.stop();
 }

 // Display the results
 console.log(t.timers.myFunction.duration()); // total duration of all ticks
 console.log(t.timers.myFunction.min()); // minimal tick duration
 console.log(t.timers.myFunction.max()); // maximal tick duration
 console.log(t.timers.myFunction.mean()); // mean tick duration
 console.log(t.timers.myFunction.median()); // median tick duration
 console.log(t.timers.myFunction.start()); // timestamp of the start of the first tick
 console.log(t.timers.myFunction.end()); // timestamp of the end of the last tick
```


[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/alexandrusavin/exectimer/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

