### GOOFYSYS

```
Its quite a simple binary, which has multiple hurdles in the form of characters, make sure to get that final magic hash which leads you to the flag.
Flag format: cybergrabs{}
Author: Elemental X
```

##### Solution:
Literally the same process as Reverseenc0. You don’t need to care about any of the checks. Just find where the flag is printed, get the string that is moved onto the stack and convert to hex representation.

```
"string" --> "737472696e67" --> cybergrabs{737472696e67}
```

> *cybergrabs{737472696e67}*
