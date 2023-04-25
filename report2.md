# Part 1

Honestly, I am quite unsure of what code I am supposed to use for the web server, due to missing most of last week of school for my national tournament in St. Louis, MO. However, for now I used the wavelet code to help with my server, but I will definitely change and improve my code after the feedback.

<img width="725" alt="Screen Shot 2023-04-24 at 11 03 55 PM" src="https://user-images.githubusercontent.com/110199983/234172157-a5a8003b-4931-4c65-9ab8-e8d6a52bd473.png">
<img width="666" alt="Screen Shot 2023-04-24 at 11 08 05 PM" src="https://user-images.githubusercontent.com/110199983/234172207-e7d93a66-2ae8-46e3-b946-1d8495f20a65.png">

* The methods handle, handleRequest, and start were called.
<img width="274" alt="Screen Shot 2023-04-24 at 11 08 20 PM" src="https://user-images.githubusercontent.com/110199983/234172218-6927d1e2-fe5b-43b8-83a8-7b26cc5d9394.png">
* I did not change any values yet because I am still unsure for the process of creating a webserver. 

---

# Part 2

* Failure inducing code: 
```
if (arr.length - i - 1 == 0) {
arr[i] = temp;
}
```
* Good code:
```
for (int i = 0; i < arr.length; i += 1) {
arr[i] = arr[arr.length - i - 1];
}
```
* Symptom: <img width="560" alt="Screen Shot 2023-04-24 at 11 24 07 PM" src="https://user-images.githubusercontent.com/110199983/234174026-341691e5-0ead-4f3c-8bb7-2d80260644fe.png">

* Before:
```
public class ArrayExamples {
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```

* After: 
```
static void reverseInPlace(int[] arr) {
    int temp = arr[0];
    for(int i = 0; i < arr.length; i += 1) {
      if (arr.length - i - 1 == 0) {
        arr[i] = temp;
      }
      
      else {
        arr[i] = arr[arr.length - i - 1];
      }
    }
  }
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    if (arr.length != 0) {
      int temp = arr[0];

      for(int i = 0; i < arr.length; i += 1) {
        if (i != arr.length - 1) {
          newArray[i] = arr[arr.length - i - 1];
        }
        
        else { 
          newArray[i] = temp;
        }
      }
    }
    return newArray;
  }
```
---

# Part 3

* I learned that websites are much more complex than what people view. I understand that we have created a extremely simple website that only show texts in its most basic form. Websites like apple, tesla, nike, and other big companies, must have so much code just for the smallest of things, which is mind blowing. As I was struggling with a simple process like this, the future holds a wide variety of knowledge that will further improve my skills as a programmer.
---
