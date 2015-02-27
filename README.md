#jquery.smartclick
smartclick is to solve one issue from jquery click event, which is return Event object doesn't pass back the target element where it binds from click event.

##Why I build it
When event is caught by click event listener, the default expection is the element I binded at. However, jQuery doesn't do that for me. And they just expect ```this``` could do replace the current element, however, most of time I use this to represent current Object/module. So I build smartclick to return expected element from 

##Installation
```shell 
bower install jquery.smartclick
```

you may want to auto update your bower.json with 
```shell 
bower install jquery.smartclick --save-dev
``` 

##How to use
1. Include jQuery if you haven't:

	```html
	<script src="http://ajax.googleapis.com/ajax/libs/jquery/2.0.0/jquery.min.js"></script>
	```

2. Include plugin's code:

	```html
	<script src="dist/jquery.boilerplate.min.js"></script>
	```

##Example
+ html tree elements:

```html
<div class="className">
    <div class="className2">
        <div class="className3"></div>
    </div>
</div>
```

+ bind the elements you want to bind and get what you expected

```javascript
$(".className").smartclick({
    onClick: function(target, event) {
        // target is the target element you bind from
        // event is Event object from jquery.click
    }
});
````

##Credit
Template used: [jQuery biolerplate](https://github.com/jquery-boilerplate/jquery-boilerplate)

##License
MIT
