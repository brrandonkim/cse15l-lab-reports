## Original Post


I am using my personal Macbook Pro 14" with the new Silicon Chip, running MacOS, and using VSCode to program and edit.


**My Output:**

<img width="410" alt="Screen Shot 2023-06-05 at 11 21 45 PM" src="https://github.com/brrandonkim/cse15l-lab-reports/assets/110199983/595a6475-2bf8-4776-95d8-777f4d81651b">


**ReversibleChecker.java:**

<img width="396" alt="Screen Shot 2023-06-05 at 11 22 44 PM" src="https://github.com/brrandonkim/cse15l-lab-reports/assets/110199983/8705394e-a07c-44bf-b826-d7113238eafc">

---

**Script.sh:**

<img width="279" alt="Screen Shot 2023-06-05 at 11 22 55 PM" src="https://github.com/brrandonkim/cse15l-lab-reports/assets/110199983/7c950cf6-32a6-44f6-993a-1de2367da1ef">

---


My `Script.sh` is supposed to run `ReversibleChecker.java` and when I input a string that is the same word when reverse, the code should echo "The string is reversible". However, I did not input any string and yet it still passes the test when it should not. The code should actually output: "The string is not reversible" or not have either output. I can't seem to figure out the issue because my VSCode does not point out any errors, please help me out.

**TA's Response:**

The problem you stated is somewhat the answer to your problem. You need to include a variation in `ReversibleChecker.java` that gives an output when there is no string inputted by the user.

---

**Reformed ReverisbileChecker.java:**

<img width="461" alt="Screen Shot 2023-06-05 at 11 35 36 PM" src="https://github.com/brrandonkim/cse15l-lab-reports/assets/110199983/468a1587-43dd-4801-b8b9-4603420b3598">

Thank you for calling out my silly error. After pointing me in the direction of the error I said, I was able to add a layer of code that would give me an output of "empty input." when the user does not enter anything.

<img width="394" alt="Screen Shot 2023-06-05 at 11 38 08 PM" src="https://github.com/brrandonkim/cse15l-lab-reports/assets/110199983/09154ea2-fff6-48e6-929d-1d5c08b2e18b">

---

**Setup Info:**

<img width="124" alt="Screen Shot 2023-06-05 at 11 23 57 PM" src="https://github.com/brrandonkim/cse15l-lab-reports/assets/110199983/d43204d7-efe0-4fc1-8641-229a2fda34e9">

Before ReversibleChecker.java was edited:

```
import java.util.Scanner;

public class ReversibleChecker {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter a string: ");
        String input = scanner.nextLine();

        String reversed = reverseString(input);

        if (input.equalsIgnoreCase(reversed)) {
            System.out.println("The string is reversible.");
        } else {
            System.out.println("The string is not reversible.");
        }

        scanner.close();
    }

    private static String reverseString(String input) {
        StringBuilder reversed = new StringBuilder();
        for (int i = input.length() - 1; i >= 0; i--) {
            reversed.append(input.charAt(i));
        }
        return reversed.toString();
    }
}
```

To trigger the bug, I compiled the code using `javac ReversibleChecker.java` then used `chmod +x Script.sh` and finally `./Script.sh` which introduces a bug by not providing any input when prompted for a string.

In order to fix this issue, I had to modify the Java program to handle empty input correctly and return the proper result; by adding this after `String input = scanner.nextLine();"

```
if (input.isEmpty()) {
            System.out.println("Empty input. Please provide a valid string.");
        }
```

---

**Reflection**

I learned that `vim` was an extremely useful command line that helped me edit files remotely. Also it allows you to do all actions from the terminal. They have integrated instructions on how to use it, which I have not seen for any of the other commands, which intrigues me differently than the other command lines. It took me a little while to get used to, but once you get used to it, you pick up on how to use it quickly and effectively.
