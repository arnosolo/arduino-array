### Array Class for Arduino

Somehow Arduino doesn't support cpp stand lib, so here we are.

Implemented functions:

- `push`
- `pop`
- `forEach`

```cpp
#include <Arduino.h>
#include "Array.h"

void printStr(String str) {
  Serial.println(str);
};

void setup()
{
  Serial.begin(9600);

  Array<String> arr1 = Array<String>();
  arr1.push("demo forEach 0");
  arr1.push("demo forEach 1");
  arr1.forEach(printStr); // should print 2 msg

  Array<String> arr2 = Array<String>();
  arr2.push("hi");
  arr1 = arr2;
  Serial.println(arr1[0]); // hi
  
}

void loop()
{
}

```

