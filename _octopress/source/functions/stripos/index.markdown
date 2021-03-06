---
layout: page
title: "JavaScript stripos function"
comments: true
sharing: true
footer: true
alias:
- /functions/view/stripos:536
- /functions/view/stripos
- /functions/view/536
- /functions/stripos:536
- /functions/536
---
<!-- Generated by Rakefile:build -->
A JavaScript equivalent of PHP's stripos

{% codeblock strings/stripos.js lang:js https://raw.github.com/kvz/phpjs/master/functions/strings/stripos.js raw on github %}
function stripos (f_haystack, f_needle, f_offset) {
  // From: http://phpjs.org/functions
  // +     original by: Martijn Wieringa
  // +      revised by: Onno Marsman
  // *         example 1: stripos('ABC', 'a');
  // *         returns 1: 0
  var haystack = (f_haystack + '').toLowerCase();
  var needle = (f_needle + '').toLowerCase();
  var index = 0;

  if ((index = haystack.indexOf(needle, f_offset)) !== -1) {
    return index;
  }
  return false;
}
{% endcodeblock %}

 - [Raw function on GitHub](https://github.com/kvz/phpjs/blob/master/functions/strings/stripos.js)

Please note that php.js uses JavaScript objects as substitutes for PHP arrays, they are 
the closest match to this hashtable-like data structure. 

Please also note that php.js offers community built functions and goes by the 
[McDonald's Theory](https://medium.com/what-i-learned-building/9216e1c9da7d). We'll put online 
functions that are far from perfect, in the hopes to spark better contributions. 
Do you have one? Then please just: 

 - [Edit on GitHub](https://github.com/kvz/phpjs/edit/master/functions/strings/stripos.js)

### Example 1
This code
{% codeblock lang:js example %}
stripos('ABC', 'a');
{% endcodeblock %}

Should return
{% codeblock lang:js returns %}
0
{% endcodeblock %}


### Other PHP functions in the strings extension
{% render_partial _includes/custom/strings.html %}
