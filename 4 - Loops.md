# 4.1: while
* Simplest
* the one I use the least
* highest codebreaking potential
```GML
while(<expression>) {
	//do something here
}
```
continues looping while expression is true
# 4.2: repeat
* runs x number of times
* more basic implementation of for
```GML
repeat(<number of times(can be expression/variable)>){
	//do something here
}
```
# 4.3: for
* The one I use the most
```GML
for(<assignment>; <expression>; <operation>;) {
	//do something here
}
```
Common implementation & what it means
```GML
for(var i = 0; i < length; i++) {
	//var i = 0; is the assignment, assigns a local var to an initial value
	//i < length; is the expression, it runs before every loop and as long as it returns true it continues the loop
	//i++; this is the operation, it runs at the end of each loop, and increases i by 1
}
```
# 4.4: forEach
* The best way to loop through arrays (as long as you dont have to change item values)
* works best with arrays of objects because you can set object key values
syntax:
```GML
arrayVar = [item1, item2, item3...];

function doSomething(_element, _index) {
	//_element contains the value of the item this loop
	//_index contains the index of said item
}

array_foreach(arrayVar, doSomething);
```
