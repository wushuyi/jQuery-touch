# jQuery.touch

jQuery.touch.js Inspired by [Zepto](https://github.com/madrobby/zepto), it easy use.

###author by [wushuyi](https://github.com/wushuyi)

##Touch events
The “touch” module adds the following events, which can be used with on and off:

tap — fires when the element is tapped.

singleTap and doubleTap — this pair of events can be used to detect both single and double taps on the same element (if you don’t need double tap detection, use tap instead).

longTap — fires when an element is tapped and the finger is held down for more than 750ms.

swipe, swipeLeft, swipeRight, swipeUp, swipeDown — fires when an element is swiped (optionally in the given direction)



```javascript
<style>.delete { display: none; }</style>

<ul id=items>
  <li>List item 1 <span class=delete>DELETE</span></li>
  <li>List item 2 <span class=delete>DELETE</span></li>
</ul>

<script>
// show delete buttons on swipe
$('#items li').swipe(function(){
  $('.delete').hide()
  $('.delete', this).show()
})

// delete row on tapping delete button
$('.delete').tap(function(){
  $(this).parent('li').remove()
})
</script>
```