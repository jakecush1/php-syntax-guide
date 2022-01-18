#PHP syntax guide
```
--Comments:
PHP can comment out code a few different wanys, either using:

// double forward slash comments our a line<br>
// # hashtag comments out a line as well<br>
/*<br>
slash start will comment out multiple lines<br>
*/<br>
```
#PHP Variables:<br>
Variable declaration begins with a $ and like all other PHP the 
line must end in a ;<br>
```
  $varInt = 54;<br>
  $varStr = "hello world";<br>
  $_vartest = "hi;<br>
vars can only contain a-z, A-Z, 0-9 and _, numbers letters and underscores<br>
Vars are case sensitive, $var1 is different than $VAR1<br>
```
#PHP Echo / Print:<br>
Echo and Pring are both functions in PHP to display data on the screen<br>
echo has no return vaue and print has a return value of 1<br>
echo can take multiple parameters and print can only take 1<br>
```
  echo("echo can" . "have more than". "one parameter<br>");<br>
  echo($num1 + $num2);<br>
  print("234");<br>
  print "Study PHP at " . $txt2 . "<br>";<br>
  print $x + $y;<br>

```
#PHP Data Types:<br>
PHP contains all the data types as other coding languages
 there exists:<br>
 You can use var_dump($var) to check whic type of data the variable has<br>
   ```
   -String
    $varStr = "hello this is a string";
    
   -Integer
    $varInt = 54;
    
   -Float (floating point numbers - also called double)
    $varFloat = 11.23;
    
   -Boolean
    $varBoolean = true;
    $varBoolean2 = false;
    
   -Array
    $varArray = ["guitar","piano","drums","bass","saxophone"];
    $numbArray = [1,2,3,4,5];
    
   -Object
   -there are two main aspects when creating object:classes and objects
   -a class is a template made for creating objects
   -you can use the __contruct() function to automatically create objects
   
  class House {
    public $color;
    public $madeOf;
    public $cost;
    public function __contruct($color, $madeOf, $cost) {
      $this->color = $color;
      $this->madeOf = $madeOf;
      $this->cost = $cost;
    }
    public function message() {
      return "My house is " . $this->color . " and is made of " . 
      $madeOf . " and costs " . $cost;
    }
 }
  
$myHouse = new House("blue", "bricks", "1million");
echo $myHouse -> message();
```
#NULL
   Null means that the variable has no data type assigned to it```
   $nullVar = NULL;
   ```
#Resource
    
#PHP Strings
Strings have multiple built in functions to manipulate or check different 
parts of strings```
$myStr = "hello there everyone, this is a string";

strlen() counts the length of the string
echo strlen($myStr) //outputs 38

str_word_count() - Count Words in a String
echo str_word_count($myStr) //outputs 6

strrev() - Reverse a String

strpos() - Search For a Text Within a String
strpos($myStr, everyone) //outputs 12 because the word everyone has 12 characters before it

str_replace() - Replace Text Within a String  
str_replace("hello", "goodbye", "hello world") //outputs goodbye world
```
#PHP Numbers
There exits a few different types of numbers in PHP
asides fro using var_dump() you can check number types w various resources(functions)
```
-integers -> int
  $x = 5985;
  var_dump(is_int($x));  //returns true
  
-decimals -> float
  $x = 10.365;
  var_dump(is_float($x)); //returns true
  
-Not a number -> NaN
  $x = acos(8);
  var_dump($x);

-infinity
  $x = 1.9e411;
  var_dump($x);
  
-numerical strings
  $x = 5985;
  var_dump(is_numeric($x)); //returns true
  $x = "5985";
  var_dump(is_numeric($x)); //returns true
  ```
PHP Casting Strings and Floats to Integers
  it can be useful to be able to change floats or strings to to ints
  we can do this using (int)```
  $float = 11.34;
  $string = "2321";
  echo (int)$float; //returns 11
  echo (int)$string; //returns 2321
```

#PHP Constants
Constants are like variables, in that they hold a value, different
in that they cannot be changed, and are automatically global across the entire script
A valid constant name starts with a letter or underscore (no $ sign before the constant name).
the syntax is as followed, default for case-insensitive is false```
   -define(name, value, case-insensitive)
   
   define("name", "jake");
   define("address", "724 hoover", true)
   echo NAME;  //returns NAME
   echo name;  //returns jake
   echo ADREss; //returns 724 hoover
  
  ```
#PHP Operators
  PHP divide the following operators into groups 
  ```
    -Arithmetic operators
      addition +
      subtration -
      multiplication *
      division /
      modulus (remainder after division) %
      exponent **
      
    -Assignment operators
      x = y; //assigns the value of y to x
      x+=y; //same as x=x+y
      x*=y; //same as x=x*y
      x/=y; //same as x=x/y
      x%=y; /same as x=x%y
      
    -Comparison operators - return true or false
      == equal to 
      === equal to and same type
      != , <> not equal to
      !== not identical
      >= greater than or equal to
      <= less than or equal to
      $x<=>$y returns -1 if x is less than y, returns 0 if equal and 1 if x is greater than y
      
    -Increment/Decrement operators
      ++$x //increments by 1 then returns $x
      --$x //decreses by 1 then returns $x
      $x++ //returns x then increments by 1
      #x-- //returns x then decreses by 1
      
    -Logical operators
      and , && // returns true if both sides are true
      or, || //returns true if one or the other side is true
      xor,  // returns true if one or the other is true but noth both
      !$x  //true if $x is not true
      
    -String operators
      . //concatenation
      $txt.=$txt2 // $txt = $txt . $txt2
      
    -Array operators
      + // union of two arrays 
        $newArr = [0,1]+[2,3] //makes [0,1,2,3]
      == //returns true if equal
      === //true if identical
      != //true if not equal
      !== // true if not identical      
```
#PHP If & Else & Elseif
  if statement - executes some code if one condition is true
  if...else statement - executes some code if a condition is true and another code if that condition is false
  if...elseif...else statement - executes different codes for more than two conditions
  ```
    $myNum = 5;
    if ($myNum > 6){
      echo "cool";
    }
    elseif ($myNum == 6){
     echo "righteuos"
    }
    else{
      echo "finally"
    }
    //since if was false it goes on to elseif, if elseif is false it resorts to else
    ```

#PHP Functions

  PHP comes with over 1000 built in functions, some weve already talked 
  about include vardump(), echo(), strlen()
  You can also create you own functions and make them do whatever you want
  ```
  function sumNumbers($num1, $num2){  //$num1 and $num2 are parameters
  $sum = $num1 + $num2;
  echo $sum;
  }
    //to make the function run you must then call the function
    
  sumNumbers(3,5); //function will return 8
  ```
  
#PHP Arrays<br>
  arrays are single variables holding multiple pieces of data
  they can be created a couple of ways<br>
  ```
 -Indexed arrays index each value in the order they are entered - 0,1,2,3<br>
  $myArray = [1,2,3,4];<br>
  $newArray = array("hello",14,"buddy");<br>
  var_dump($myArray);<br>
  var_dump($newArray);<br>
  echo $mArray[0]; //returns 1<br>
  
 -Associative Array are array with indexs as other custom names
  $age = array("Peter"=>"35", "Ben"=>"37", "Joe"=>"43");
  // or can be entered like:
  $age['Peter'] = "35";
  $age['Ben'] = "37";
  $age['Joe'] = "43"; 
  var_dump($age); //prints the array
  echo $age['Joe']; //will return 43
  
  -Multi dimensional arrays also exist where they have two keys
  
  -sorting arrays can be very useful using these built in functions:
  
    sort() - sort arrays in ascending order
    rsort() - sort arrays in descending order
    asort() - sort associative arrays in ascending order, according to the value
    ksort() - sort associative arrays in ascending order, according to the key
    arsort() - sort associative arrays in descending order, according to the value
    krsort() - sort associative arrays in descending order, according to the key

      $myArray = [2,6,79,43,1,3,4];
      var_dump($myArray); //prints the unsorted array
      $sorted = sort($myArray); //sorts the array by values in ascending order
      echo ($myArray); //prints the sorted array

  ```
#PHP Loop
PHP can run loops like other scripting languages
    while - loops through a block of code as long as the specified condition is true 
     ```
     $x = 1;
      while($x <= 5) {
        echo "The number is: $x <br>";
        $x++;
      } 
      ```
    do...while - loops through a block of code once, and then repeats the loop as long as the specified condition is true
    ```
      $x = 1;
      do {
        echo "The number is: $x <br>";
        $x++;
      } while ($x <= 5);```
      
    for - loops through a block of code a specified number of times
     ```
     for (init counter; test counter; increment counter) {
      code to be executed for each iteration;
      } 
    
    for ($x = 0; $x <= 10; $x++) {
      echo "The number is: $x <br>";
    } 
    ```
    foreach - loops through a block of code for each element in an array
      The foreach loop works only on arrays, and is used to loop through each key/value pair in an array.
      ```
      $colors = array("red", "green", "blue", "yellow"); 
      foreach ($colors as $value) {
        echo "$value <br>";
      }
      ```
      
      