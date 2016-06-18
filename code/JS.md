[![forthebadge](http://forthebadge.com/images/badges/uses-js.svg)](http://forthebadge.com)


# JavaScript


## Table of Contents

1. [Arrays](#arrays)
1. [Functions](#functions)
1. [Closers](#closers)
1. [Callbacks](#callbacks)
1. [Objects](#objects)
1. [Loops](#loops)
1. [Conditional Statements](#statements)
1. [JSON](#json)



```javascript

// capture selector
var nav = document.querySelector('.class');

// create our toggle method
var toggleNav = function() {

    // this equals the object attached to the AEL  
    if( this.classList.contains('.active') ) {
        this.classList.remove('active');
    }
    else {
        this.classList.add('active');
    }

};

// attach nav object to standard AEL 
nav.addEventListener('click', toggleNav, false);

```

-**Get/Set Attributes:**

```javascript

	$(elem).attr('id', 'name');      // set
	$(elem).attr('id');              // get

	elem.setAttribute('id', 'name')  // set
	elem.getAttribute('id')          // get

```

-**Scroll Event:**

```javascript

var wrap = $("#wrap");

wrap.on("scroll", function(e) {
    
  if (this.scrollTop > 147) {
    wrap.addClass("fix-search");
  } else {
    wrap.removeClass("fix-search");
  }
  
});

/**
 * OR
 */

var offset = window.pageYOffset ? window.pageYOffset : document.documentElement.scrollTop;

if (offset > 200) {
    toolbar.addClass('is-detached');
}
else {
    toolbar.removeClass('is-detached');
}

```

```javascript

// link: http://stackoverflow.com/questions/1723650/jquery-limit-text-by-length

$(function(){
    var $elem = $('p');              // The element or elements with the text to hide
    var $limit = 10;                 // The number of characters to show
    var $str = $elem.html();         // Getting the text
    var $strtemp = $str.substr(0,$limit);   // Get the visible part of the string
    $str = $strtemp + '<span class="hide">' + $str.substr($limit,$str.length) + '</span>';  // Recompose the string with the span tag wrapped around the hidden part of it
    $elem.html($str);                // Write the string to the DOM 
})

```


```javascript

function SpliceString(elem) {

    $('.name').each(function(index, elem) {

       var limit = $(elem).text().length;
       var reduce = '';

       reduce = limit / 2;

       var str = $(elem).text();
       var res = str.slice(0, reduce);
       console.log(res);
       
    }); 
}

```




