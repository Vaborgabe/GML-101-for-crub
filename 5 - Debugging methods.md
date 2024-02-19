# 5.1: show_debug message
basic syntax
`show_debug_message("message");`
advanced usage:
* in the string you can use "{#}" followed by variables to insert variables into the string easily
* make sure to remember in programming, you start counting at 0
example:
```GML
var1 = "value 1";
var2 = "value 2";
show_debug_message("var1 is {0}, var2 is {1}", var1, var2);
```
# 5.2 debug get callstack
* Gets array to show you where the function was called from, a.k.a. the callstack
* most of it will be a script/event name, then a : (colon), then the line number
* best way to display a callstack is to assign a local variable to the function, then loop through and print each result
`debug_get_callstack(depth (optional));`