# Mid course exam questions

This is a example question from a digital exam. The original exam consists of 3 assignment in which you have to write a short python program.

You're only evaluated based on the _correctness_ of your solutions, code design is not important. So, you don't have to worry about comments or style guides.

**The level of these questions are based on what you've learned so far (Level 1 - 3). The actual exam will also contain questions on more advanced subjects.**

You can test your code using checkpy. First download the tests for the exam:

    checkpy -d /spcourse/exam-tests

Run checkpy:

    checkpy sp101_exam_questions

# Rules

- Create one file for all your solutions called `sp101_exam_questions.py`. This is the file you'll hand in at the end of your exam.
- You're not allowed to use `numpy` or any other external Python module.
- This is a closed book exam. You're not allowed to use any online materials.
- The only recourses you're allowed to have open during the exam are: 1) this exam webpage, 2) the Pulsar editor, and 3) the terminal.
- You cannot get any help with programming during the exam.

### Assignment 1: Twoish


Write a function called `twoish(n)`. The functions approximates the number two by calculating the sequence $$1 + \frac{1}{2} + \frac{1}{4} + \frac{1}{8} + \frac{1}{16} + \ldots$$ repeated $$n$$ times. So we compute the sum for $$\frac{1}{x}$$ where $x$ starts at 1 and is doubled at every iteration.

Example usage:

    almost_two = twoish(10)
    print(almost_two)
    less_two = twoish(2)
    print(less_two)

Expected output:

    1.998046875
    1.5

### Assignment 2: Hamming

Hamming distance is a metric used to compare texts. Normally you compare texts per letter, but we're going to compare them per word. You look at the individual words of both texts. You compare the first word of each texts. If they're the same, you count 1 point. If they're different you count 0. You do the same for the second word of each string, then the third, etc. The hamming distance is simply all points added up.

Write a function called `hamming_distance(text1, text2)` that compares two texts this way. Bear in mind some edge cases:

- If two texts have a different amount of words, you limit the comparison to the shortest of the two lengths.
- The function should not be case sensitive and not sensitive to punctuation.

Example usage:

    pretty_text = hamming_distance("Norwegian Wood", "Norwegian Fjord")
    print(pretty_text)
    pretty_text = hamming_distance("I love deadlines. I love the whooshing noise they make as they go by.",
                                   "I LOVE pizza. I love the round shape they have.")
    print(pretty_text)

 Expected output:

    1
    6

Tips:

- You can split a text into a list of words using the `text.split()` method.
- You can remove punctuation and space with the `text.strip(' .,!?;:')` method.
