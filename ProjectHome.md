AS3 Wrapper Class for creating BitmapDatas greater than 2880px

With the Class you're able to bypass the 2880px limit for BitmapData and the 8191px limit for DisplayObjects

```
import com.formatlos.as3.lib.display.BitmapDataUnlimited;
import com.formatlos.as3.lib.display.events.BitmapDataUnlimitedEvent;
 
var bdu:BitmapDataUnlimited = new BitmapDataUnlimited();
bdu.addEventListener(BitmapDataUnlimitedEvent.COMPLETE, onBmpReady);
bdu.create(5000, 5000, true);
 
var hugeBmp : BitmapData;
 
function onBmpReady(event : BitmapDataUnlimitedEvent) : void
{
	hugeBmp = bdu.bitmapData;
	trace("BitmapData: w=" + hugeBmp.width + " h=" + hugeBmp.height);
}
```