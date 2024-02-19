# 2.1: Formatting
```GML
if(<condition>) {
	//do stuff
}
```
# 2.2: Condition Operators
* ==
* !=
* >
* <
* >=
* <=
* &&
* ||
* ^^
	* xor one or the other, not both
* ()
	* use like math
* !
	* not
* %
	* Returns remainder
	* useful in loops where u need to do something every x times
## Getting if even rather than odd
```GML
//in create event
testNum = 0;

//in Step Event
if(mouse_check_button_pressed(mb_left)) {
	testNum++;
	if(!(testNum % 2)) show_debug_message(testNum);
}
```
# 2.3: conditional operator
## Intro: alter code to this
```GML
//in create
testNum = 0;
varState = "0";

//in step
if(mouse_check_button_pressed(mb_left)) {
    testNum++;
    if(testNum % 2) {
        varState = "odd";
    } else {
        varState = "even";
    }
    show_debug_message("{0} is {1}", testNum, varState);
}
```
* That takes too much space, conditional operators help that
* `variable = condition ? set if true : set if false;`
```GML
//delete the inside of mouse chekc and replace with
    testNum++;
    varState = testNum % 2 ? "odd" : "even";
    show_debug_message("{0} is {1}", testNum, varState);
```