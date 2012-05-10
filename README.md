HoverIntent for mootools
===========

This is a port of jQuery HoverIntent http://cherne.net/brian/resources/jquery.hoverIntent.html

hoverIntent is a plug-in that attempts to determine the user's intent... like a crystal ball, only with mouse movement! It works like (and was derived from) jQuery's built-in hover. However, instead of immediately calling the onMouseOver function, it waits until the user's mouse slows down enough before making the call.
Why? To delay or prevent the accidental firing of animations or ajax calls. Simple timeouts work for small areas, but if your target area is large it may execute regardless of intent.

![Screenshot](http://w492283.open.ge.tt/1/files/5V4WYVH/0/blob/x675?noinc=1)

How to use
----------

    <script type="text/javascript">
        window.addEvent("domready", function() {
            $$('#featured li').each(function(li){
                li.hoverIntent(
                    over: makeTall, // function = onMouseOver callback (REQUIRED)    
                    timeout: 500, // number = milliseconds delay before onMouseOut    
                    out: makeShort // function = onMouseOut callback (REQUIRED)  
                );
            })
        });
    </script>

    <ul id="featured"> 
        <li></li>
        <li></li>
        <li></li>
        <li></li>
    </ul>