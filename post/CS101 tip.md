---
title: "CS101 TA Experience"
date: 2023-08-30 17:32:00 +0900
draft: false
summary: "Teaching and Learning"
---
# Teaching
## 1. Frequent mistakes
- WK1
  - not putting `:` (colon) after for loop
  - no indentation
  - misspelling `range`
- Other weeks
  - not putting `:` (colon) after if/while loop
  - using `else` with `while`
  - IndentationError

## 2. Frequent tips
- WK1
  - use `_` instead of `i`
  - group indent by tabbing the block
  - write the rest of the function name automatically by pressing tab
  - delete repeating parts and fill for loop instead
  - copy-reuse the first four lines loading library (`cs1robots`) and world data (`load_world`, `create_world`, etc.)
- Other weeks
  - copy the code from other task and modify a very little bit
  - `print` statement to debug
  - `ctrl + /` to comment out a line
  - `while True` and `break`
  - `tab` and `shift + tab` to indent and unindent
  - Block indent by scrolling through multiple lines
  - `ctrl + h` to replace


## 3. Easy refactoring
- repetition -> for loop
{{< highlight python >}}
for i in range(5):
    # Your code here (repeated action)
{{< / highlight >}}

- repetition -> function
{{< highlight python >}}
def my_function():
    # Your code here (repeated action)
{{< / highlight >}}

- action `ABABA` -> halt in the middle of the last loop of `for`
{{< highlight python >}}
for i in range(3):
    # Your code here (repeated action)
    if i == 2:
        break
    # Rest of the code
{{< / highlight >}}

# Learning
- How to teach
  - How to explain the concept
  - How to give hints
  - How to give feedback
  - How to motivate
  - How to be calm