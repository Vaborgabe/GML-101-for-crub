Just scratching the surface
# 3.1: 1D Arrays
Assignment:
`varName = ["first", "second", "third"]`
reading:
* Arrays start counting at 0 rather than 1
```GML
varName[0]; //will be equal to first
varName[1]; //will be equal to second
```
# 3.2: Dynamic Array Definition
## Case 1: Known Length
creating:
`varName = array_create(length, value (optional));`
adding:
```GML
var _index = 0;
repeat(length) {
	varname[index] = value;
	_index++;
}
```
example - counting by 5 to 25:
```GML
testArray = array_create(5);

if(mouse_check_button_pressed(mb_left)) {
	var _index = 0;
    repeat(5) {
        testArray[_index] = (_index+1)*5;
        _index++;
    }
    show_debug_message(testArray);
}
```
* array_create is perfect for making an array of x length where every value starts the same
## Case 2: unknown length
creating:
`varName = [];`
adding:
`array_push(varName, val...);`
example - counting by 5:
```GML
testArray = [];

if(mouse_check_button_pressed(mb_left)) {
	var _index = 0;
    repeat(5) {
        _index++;
        array_push(testArray, _index*5);
    }
    show_debug_message(testArray);
}
```

# 3.3 Multi-Dimensional Arrays
* Good for storing data like coordinates and other data points that work hand in hand
* all 1D array functions and rules apply
Assignment:
```GML
varName = [
	["0-0", "0-1"],
	["1-0", "1-1"],
	...
];
```
Reading:
```GML
varName[0][0]; //"0-0"
varName[0][1]; //"0-1"
varName[1][0]; //"1-0"
```
# 3.4: More array functions
https://manual.gamemaker.io/monthly/en/index.htm?#t=GameMaker_Language%2FGML_Reference%2FVariable_Functions%2FArray_Functions.htm
