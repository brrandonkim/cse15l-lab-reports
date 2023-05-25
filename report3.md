# Researching the Command: find

## Example 1: -name

With the help of ChatGPT, it directed me to a variation of find: `-name`

```
% find technical -name preface.txt
technical/911report/preface.txt

% find technical -name ai00134.txt
technical/government/Gen_Account_Office/ai00134.txt
```

The variation `-name` returns a file's location based on its name. We can use this to quickly get the path to a file so that we can utilize it later in our code and locate files that are deeply buried within several directories.

---

## Example 2: -type

ChatGPT helped me find the `-type` variation and helped me understand the different ways to use `-type`, such as `-type f` helps search for regular files or `-type d` searches for directories.

```
% find technical/911report -type f
technical/911report/chapter-13.4.txt
technical/911report/chapter-13.5.txt
technical/911report/chapter-13.1.txt
technical/911report/chapter-13.2.txt
technical/911report/chapter-13.3.txt
technical/911report/chapter-3.txt
technical/911report/chapter-2.txt
technical/911report/chapter-1.txt
technical/911report/chapter-5.txt
technical/911report/chapter-6.txt
technical/911report/chapter-7.txt
technical/911report/chapter-9.txt
technical/911report/chapter-8.txt
technical/911report/preface.txt
technical/911report/chapter-12.txt
technical/911report/chapter-10.txt
technical/911report/chapter-11.txt
```

When using the `-type f` command, there were too many files to list onto the page, so I decided to search for a specific directory and make it list its regular files, which was successful. You may filter and search for files depending on their kind with the bash command -type. It gives you the ability to distinguish between various file kinds, including ordinary files, directories, symbolic links, and more. When you wish to execute particular operations or apply particular actions just to a specific type of file, this is useful. I also ask ChatGPT to list ways to use `-type` differently and it gave me four different options: 
<img width="675" alt="Screen Shot 2023-05-24 at 9 09 34 PM" src="https://github.com/brrandonkim/cse15l-lab-reports/assets/110199983/72305c26-afd2-4451-a5c3-d97ccfdc4fc5">

---

## Example 3: -size

ChatGPT once again helped me find the variation `-size` and showed me what sizes of files I can search for in the technical directory.

```
% find terminal -size -1M
technical/plos/journal.pbio.0030024.txt
technical/plos/journal.pbio.0020223.txt
technical/plos/pmed.0020249.txt
technical/plos/pmed.0020275.txt
technical/plos/journal.pbio.0020019.txt
technical/plos/pmed.0020088.txt
technical/plos/journal.pbio.0020145.txt
technical/plos/pmed.0020103.txt
technical/plos/pmed.0020117.txt
technical/plos/journal.pbio.0020353.txt
technical/plos/journal.pbio.0020347.txt
technical/plos/journal.pbio.0020420.txt
technical/plos/journal.pbio.0020346.txt
technical/plos/journal.pbio.0020187.txt
technical/plos/pmed.0020116.txt
technical/plos/pmed.0020102.txt
technical/plos/journal.pbio.0020150.txt
technical/plos/pmed.0020062.txt
technical/plos/pmed.0020274.txt
technical/plos/journal.pbio.0020232.txt
technical/plos/journal.pbio.0030021.txt
technical/plos/journal.pbio.0020224.txt
technical/plos/pmed.0020048.txt
technical/plos/pmed.0020060.txt
technical/plos/pmed.0020074.txt
technical/plos/journal.pbio.0020146.txt
technical/plos/pmed.0020114.txt
technical/plos/pmed.0010028.txt
technical/plos/journal.pbio.0020350.txt
technical/plos/journal.pbio.0020190.txt
technical/plos/pmed.0010029.txt
technical/plos/pmed.0020115.txt
technical/plos/journal.pbio.0020147.txt
technical/plos/pmed.0020075.txt
technical/plos/pmed.0020061.txt
technical/plos/pmed.0020210.txt
technical/plos/pmed.0020238.txt
and so on...
```

When using the `-size` command, we must set a certain sie we are looking for, or higher/lower than the size of the file we request. In this case, I asked terminal to search for files in technical that are under 1 megabyte, and it listed every single file that was under one megabyte. This is advantageous since it enables size-based file filtering.  You may search for files by size or by size range with the -size option. Most commonly used by many people: when looking for files that fit a specific size requirement, like locating huge files, it can help discover what is using up a lot of disk space or locate little files that might require more investigation.

---

## Using ChatGPT as a tool in Lab Report 3

I typed into ChatGPT: What are a few command-line options for the bash command find?

**ChatGPT:**
```
The find command in Bash provides a wide range of command-line options to customize and refine the search criteria. Here are a few commonly used options:

-name: Matches files and directories based on their names using wildcards or regular expressions. For example, -name "*.txt" will find all files with the .txt extension.

-type: Filters files based on their type. Some commonly used values include -type f for regular files, -type d for directories, and -type l for symbolic links.

-size: Allows you to search for files based on their size. For example, -size +1M will find files larger than 1 megabyte.

-mtime and -mmin: These options allow you to search for files based on their modification time. -mtime specifies the number of days ago the file was modified, and -mmin specifies the number of minutes ago.

-user and -group: These options let you search for files owned by a specific user or group. For example, -user john will find files owned by the user "john".

-exec: Executes a command on each file found. This option is useful for performing actions on the found files, such as deleting, moving, or processing them.

-prune: Excludes certain directories from the search. It can be used to prevent the find command from descending into specific directories.

These are just a few examples of the command-line options available for the find command in Bash. The find command is quite powerful and flexible, allowing you to combine multiple options to create complex search queries based on your requirements. You can refer to the find command's documentation or use the man find command in the terminal for more detailed information about all the available options.
```

ChatGPT provided a good number of bash commands that are similar or relate to the `-find` command; with the small summarization of each code I was able to understand and use ChatGPT again to dive deeper into the full functionality of the bash commands I chose. Furthermore, I chose the commands that appeared most intriguing, applied it to the repository we had, and constructed the wider applications of these alternatives (the reasons we want to utilize them). I spent a lot of time searching for possibilities before finding ChatGPT, which gathered several of them in one location for me to pick from.
