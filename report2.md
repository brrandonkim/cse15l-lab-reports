# Part 1

<img width="663" alt="Screen Shot 2023-05-10 at 8 04 19 PM" src="https://github.com/brrandonkim/cse15l-lab-reports/assets/110199983/46187b7c-728e-4916-b8f8-81024aaee8a4">

* The methods `handle`, `handleRequest`, and `start` were called.
<img width="323" alt="Screen Shot 2023-05-10 at 5 43 11 PM" src="https://github.com/brrandonkim/cse15l-lab-reports/assets/110199983/879baec9-d636-46db-a2d8-65e677dbbcd6">

* Everything that's in the method's body are relevant. The class `Handler` uses sets of if and else statements to produce and output that either adds the message or shows the message "404 not found"

---

# Part 2

* Failure-inducing input: 
```
@Test
public void testReversedInPlaceMultiple() {
  int[] input2 = {1,3,5};
  ArrayExamples.reverseInPlace(input2);
  assertArrayEquals(new int[] {5,3,1}, input2);
}
```
* Non-failure-inducing input:
```
@Test
public void testReversedInPlaceOne() {
  int[] input1 = {5};
  ArrayExamples.reverseInPlace(input1);
  assertArrayEquals(new int[] { 5 }, input1);
}
```
* Symptom: 

<img width="560" alt="Screen Shot 2023-04-24 at 11 24 07 PM" src="https://user-images.githubusercontent.com/110199983/234174026-341691e5-0ead-4f3c-8bb7-2d80260644fe.png">


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
