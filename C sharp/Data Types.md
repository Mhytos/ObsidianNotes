---
integer: |-
  Full number (int32)
  initialised by "int", followed by declaration 
  int age = 19;
  ---
  int age;
  age = 19;
  (same thing)
long: |-
  long number (int64)
  initialised by "long" and a "L" at the end of the number
  long earthAge = 90000000L;
double: |-
  decimal number 
  initialised by "double", followed by declaration
  decimal point makes number decimal, to be sure we can add a "D" at the end (Like with "long")
  double decimal = 55.2;
  ---
  double decimal = 55.2D;
float: |-
  precision number 
  same thing as with int and long
  if there is a decimal point in the number, it registers as a double
  so as before, we have to add a "F" at the end
  float precision = 5.0000001F;
decimal: |-
  decimal for stuff like money
  same thing as before, it gets registered as a double because of the decimal point
  we have to follow up the number by a "M"
  decimal money = 14.99M;
string: "i mean, its a fucking string\rstring name =\"Aba\"\r!we have to use \"\" and must not use '' cause reasons\r\r

  can be empty"
char: "only allows one single character. Here we use '' and not \"\"\r

  char letter = 'a'\r\r

  cannot be empty"
---
primitive types are only holding one value (number, char, true/false)

complex data types are holding a list of different characters (string (list of chars), array, ...)