# 1.0: How Do Variables work in GML
* Dont have to declare variables
	* easy overwriting
	* conscious local variable decision/memory build up
* NOT A TYPE SAFE LANGUAGE
	* Dont have to declare data types
	* Sounds nice, isn't
## JS Example:
```JS
let x = "2";

console.log(x-1);
```
Change -1 to +1

3 types of variables in GML

# 1.1: Instance variables
Formatting:
```GML
life = 20;
stamina = 2.2;
name = "jerma";
jeff = function() {//do something in here//}
```
each instance has its own version of this variable
GML has built in instance vars like X and Y;

## TEST VARS SET TO FUNCTIONS
# 1.2: local variables
formatting
`var _varName = value;`
* name typically starts with _
* only exists in brackets (destroyed when func ends)
```GML
function example() {
    var _local = 0;
    show_debug_message("var {0}", _local);
}

show_debug_message("var {0}", _local); //<<<<<<< error
```
* must be declared outside a loop
# 1.3: Global variables
formatting:
`global.varName = value;`
calling:
`global.varName`;
# 1.4: Macros
* Constant
* Global* (TEST THIS)
* Functions update every time its run
formatting:
`#macro var_name value;`
calling:
`var_name;`