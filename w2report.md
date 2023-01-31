# Part 1
StringServer code:
```
import java.net.URI;

class Handler implements URLHandler {
    String string = "";

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return string;
        } else {
            if (url.getPath().contains("/add-message")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    string += parameters[1] + "\n";
                    return String.format(string);
                }
            }
            return "404 Not Found!";
        }
    }
}
```
---
Examples:
>Site before any commands

![image](https://user-images.githubusercontent.com/122496316/215677281-cfbb4c86-7224-4cf1-97eb-e4633871e12e.png)

>Site with the add-message command. This calls the handleRequest method where the url is the argument (/add-message?s=hi). The string var is changed by adding "hi\n" to the end.

![image](https://user-images.githubusercontent.com/122496316/215677356-0c519374-8281-42a8-ab6c-c4df004528d4.png)

>Site with the add-message command. This calls the handleRequest method where the url is the argument (/add-message?s=my?name?is?luke). The string var is changed by adding "hi my name is luke\n" to the end.

![image](https://user-images.githubusercontent.com/122496316/215677416-b392a3a8-b628-4ba7-947f-25b4e7b3d11f.png)



# Part 2
Failure-inducing input for the reverseInPlace method:

```
@Test 
public void testReverseInPlaceFail() {
    int[] input = { 3, 2, 1 };
    ArrayExamples.reverseInPlace(input);
    assertArrayEquals(new int[]{ 1, 2, 3 }, input);
}
```
Non failure-inducing input for the reverseInPlace method:
```
@Test 
public void testReverseInPlaceValid() {
    int[] input = { 3 };
    ArrayExamples.reverseInPlace(input);
    assertArrayEquals(new int[]{ 3 }, input);
}
```
---

The sympton of the bug is that it fails to reverse the given array properly, returning the wrong array

>JUnit failing a test with given reason

![image](https://user-images.githubusercontent.com/122496316/215668482-326262b5-2eec-4ba6-9fc5-73693c7cf4c4.png)

>JUnit passing a test

![image](https://user-images.githubusercontent.com/122496316/215668576-ca7ef686-f079-4ed4-af8f-632f0957710f.png)

---

Bugged code:
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
}
```
Fixed code:
```
static void reverseInPlace(int[] arr) {
    int[] tempArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      tempArray[i] = arr[arr.length - i - 1];
    }
    arr = tempArray;
}
```
This fixes the issue as initially reverseInPlace was overriding arr with itself, so index 0 was overriden when it was copied over to the last index. 
The fixed code uses another array to hold the elements from arr as they're copied, arr then equals tempArray which successfully reversed the order of arr.
# Part 3
Overall these past two weeks of CSE15L have taugt me the nuances of debugging my code. Before I knew the general strategies and ideas on how to both 
mitigate and fix bugs in my code, but not to the nuanced level that I require for larger projects. I've learned a better paradigm on how to prepare 
and debug my projects. Additionally, I learned the vocabulary and strategies needed for discussing bugs in my code.
