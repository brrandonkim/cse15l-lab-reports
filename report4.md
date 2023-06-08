## Step 4

<img width="375" alt="Screen Shot 2023-06-07 at 10 21 44 PM" src="https://github.com/brrandonkim/cse15l-lab-reports/assets/110199983/0ec5e70d-3fc9-4c17-ae6c-68b75132e134">

**Keys:** `<ctrl-v> <enter> <"my password"> <enter>`

From my computer, I had the login command copied onto my clipboard and used the pasted command, `ctrl-v`, to quickly have the command on terminal and hit `enter` to prompt me to my password. Then I typed in my personal password and hit `enter` to log into my ieng6 account.

## Step 5

<img width="420" alt="Screen Shot 2023-06-07 at 10 29 00 PM" src="https://github.com/brrandonkim/cse15l-lab-reports/assets/110199983/abeedeb9-b77e-4ea7-a53d-edf8b20e94f2">

**Keys:** `<ctrl-c> <ctrl-v> <enter>`

Under Lab Tasks in the class website, I copied the link and the git clone command, using the copying command, `ctrl-c`, and pasting it into terminal, finally hitting `enter` to clone the lab files into my ieng6 account.

## Step 6

<img width="448" alt="Screen Shot 2023-06-07 at 10 30 45 PM" src="https://github.com/brrandonkim/cse15l-lab-reports/assets/110199983/81282c90-ce85-4878-a215-4bc7bff04da5">

**Keys:** `<l> <s> <enter> <c> <d> <space> <l> <a> <b> <7> <enter> <b> <a> <s> <h> <space> <t> <e> <s> <t> <.> <s> <h> <enter>`

In order to see what files I had in my freshly cloned account, I used the command, `ls` to locate "lab7". Then I used the command, `cd` (typed in `cd lab7`) to change my directory into where I needed to go. Lastly, I ran `test.sh` (typed in `bash test.sh`), in order to see the amount of failed tests.

## Step 7

<img width="439" alt="Screen Shot 2023-06-07 at 10 35 47 PM" src="https://github.com/brrandonkim/cse15l-lab-reports/assets/110199983/2b628fb7-beab-4820-a515-74c22e08835c">

**Keys:** `<v> <i> <m> <space> <L> <i> <s> <t> <E> <x> <a> <m> <p> <l> <e> <s> <.> <j> <a> <v> <a> <enter> <down arrow>x33 <right arrow>x2 <a> <delete> <2> <esc> <:> <w> <q>`

<img width="431" alt="Screen Shot 2023-06-07 at 10 44 16 PM" src="https://github.com/brrandonkim/cse15l-lab-reports/assets/110199983/a3c81d32-4f94-4e17-b40a-5635cbe23589">

To change `index1` to `index2` in `ListExamples.java`, I used the `vim` command (typed in `vim ListExamples.java`), hit `enter` and was presented with the code. Then I moved the cursor in terminal by using the down arrow key 33 times and the right arrow key twice. Then I used the append command `a`, which allows me to delete and add texts to the file, and deleted the 1 on `index1` and changed it to `index2` by using the keys `<delete> <2>`. Lastly, I had to save my changes, so I hit `esc` and used the command `:wq` to save and exit out of the `vim` editor.

## Step 8
<img width="307" alt="Screen Shot 2023-06-07 at 10 45 34 PM" src="https://github.com/brrandonkim/cse15l-lab-reports/assets/110199983/6e5e5402-3ebf-4dc7-bbc8-f8836b124c3c">

**Keys:** `<b> <a> <s> <h> <space> <t> <e> <s> <t> <.> <s> <h> <enter>`

To check if my new changes pass the tests, I ran `test.sh` (typed in `bash test.sh`) using the `bash` command, hit `enter` and surely enough my changes passed both tests without failures.

## Step 9

<img width="416" alt="Screen Shot 2023-06-07 at 10 46 53 PM" src="https://github.com/brrandonkim/cse15l-lab-reports/assets/110199983/8abde857-ac6f-473b-b579-8ccdc81dd9e9">

**Keys:** `<g> <i> <t> <space> <c> <o> <m> <m> <i> <t> <space> <L> <i> <s> <t> <E> <x> <a> <m> <p> <l> <e> <s> <.> <j> <a> <v> <a> <space> <-> <m> <space> <"> <f> <i> <x> <e> <d> <space> <t> <e> <s> <t> <s> <"> <enter>`

To commit my changes to my repository, I used the command `git commit` (typed in `git commit ListExamples.java -m "fixed tests"`) causing it to have the commit message `"fixed tests"` and saved into my personal github.

