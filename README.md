# Little Women Exercise

<p align="center">
  <img src='https://static01.nyt.com/images/2020/01/03/books/review/24littlewomen1/24littlewomen1-videoSixteenByNineJumbo1600-v2.jpg' width='500'>
</p>

This is a lightly modified version of CosiMichele's original exercise: https://github.com/CosiMichele/LittleWomen-Exercise

Hello folks! If you got here that means you have survived the December 9th-10th Carpentries workshop at the University of Arizona!

Learning Shell, R and Git can be extremely confusing, and quite overwhelming, therefore be proud of yourself!

## Tying It All Together

This repository's goal is to bring together the materials covered this past couple of days, by using Bash, Git and R. We are going to use the novel Little Women (`LittleWomen.txt`) from yesterday's `shell-lesson-data` folder in order to reinforce your computational learning experience.

The 4 main protagonists of the book - Meg, Jo, Beth, and Amy - are here to help us figuring out what is within the secret zip file in this repository! Meg, Jo, Beth and Amy have the key to finding out what is behind `secret.zip`. 

Following, you're going to find instructions which you can follow at your own pace.

## Repository Contents

In this repository, you'll find the following structure:

```
.
├── README.md                   <- This file
└── secret.zip                <- Compressed file
```
The `zip` file should be decompressed in order to finish the exercise 🙂. 

The file `secret.zip` is protected by 4 numbers separated by dots (formatted: `xxx.xxxx.xxx.xxx`).

## Instructions

1. Import this repository to your GitHub account.
2. Clone the imported repository to your machine.
3. Navigate to the example folder from yesterday and find `LittleWomen.txt` (located in `shell-lesson-data/exercise-data/writing/LittleWomen.txt`) and copy it to the newly cloned repository.
4. Decompressing `secret.zip`:
     - Using the command line*, find how many times Meg, Jo, Beth and Amy get mentioned. The answer will be the password to opening the file.

### *Command line help

we might have not covered how to do this in yesterday's lecture, but here's a hint: use `grep`, `wc` and redirection (the "pipe", `|`).

- `grep` is a incredibly strong tool that allows users to pick a string (e.g., word or part of a word) from a file. Using the `man` or `--help` option find out what the capabilites of `grep` are. Watch out for case sensitivity! We want to pick up "Meg", so careful of the capital letter :).
- `|` take the output of `grep` and send it directly to the next command!
- `wc` will count the words piped from `grep`.

**Hints!**

You can find the above number with a single command line :).

<details>
  <summary> grep hint </summary>
  
  `-o` and `-w` are the only 2 flags you may want to use for this.

  - `-o`: The -o option tells grep to only output the matched parts of the text
  - `-w`: This option tells grep to match only whole words. It ensures that "Meg" is treated as a standalone word and not part of another word.

</details>

<details>
  <summary> wc hint </summary>
  
  use `-l` with `wc`! (such as `wc -l`): This command counts the number of lines in the input it receives. Since we used `grep` with the `-o` option, each line will correspond to an occurrence of the word you are looking for.

</details>

**Don't feel like you're alone, we are here to help! Best of luck!!**

---

## Answers

<details>
  <summary> Click me if things get too complicated and you still want to get to the end (don't spoil yourself!) </summary>
  
  `secret.zip` decompress with `683.459.1355.645`. The format of your command is: `grep -o -w "{character_name}" LittleWomen.txt | wc -l`, where {character_name} should be replaced with Meg, Beth, Jo and Amy.

</details>
