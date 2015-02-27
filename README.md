jquery.smartclick
==================
smartclick is to solve one issue from jquery click event, which is return Event object doesn't pass back the target element where it binds from click event.

Why I build it
================
When event is caught by click event listener, the default expection is the element I binded at. However, jQuery doesn't do that for me. And they just expect ```this``` could do replace the current element, however, most of time I use this to represent current Object/module. So I build smartclick to return expected element from 

Installation
================
```bower install jquery.smartclick```

How to use
===============
+ html tree elements:
>
```html
<div class="className">
    <div class="className2">
        <div class="className3"></div>
    </div>
</div>
```

+ bind the elements you want to bind and get what you expected
>
```javascript
$(".className").smartclick({
    onClick: function(target, event) {
        // target is the target element you bind from
        // event is Event object from jquery.click
    }
});
````
