Project: number-display
Authors: Michael Kölling and David J. Barnes

This project is part of the material for the book

   Objects First with Java - A Practical Introduction using BlueJ
   Seventh edition
   David J. Barnes and Michael Kölling

It is discussed in chapter 3.

To use this project, create an instance of class NumberDisplay. Then inspect this 
instance and leave the inspector window open. With the inspector window open, 
call the object's methods, such as increment and setValue.


Lab report part 1 (part a = question, part b = answer)

1a.Think again about the lab-classes project that we discussed in Chapter 1 and 2. 
Imagine that we create a LabClass object and three Student objects. We then enroll 
all three students in that lab. Try to draw a class diagram and an object diagram 
for that situation. Identify and explain the differences between them.

1b.

2a.At what time(s) can a class diagram change? How is it changed?

2b.When a class is created or a new relationship between the classes or objects
is established, such as making one class inheret from another, an arrow would 
point to the class that is being extended by the class.

3a.At what time(s) can an object diagram change? How is it changed?

3b.When adding new Student objects or removing them.

4a.Write a definition of a field named tutor that can hold a reference to an 
object of type Instructor.

4b.private Instructor tutor;

6a.Create a second NumberDisplay object with a limit of 60, and give it the name 
minutes. Call its increment method and note how the method calls are represented 
in the Terminal window. Imagine that the hours and minutes objects on the object 
bench represent the two NumberDisplay objects managed by a ClockDisplay object. 
In effect, you are now performing the role of the ClockDisplay object. What 
should you do each time you call increment on minutes to decide whether it has 
rolled over and whether increment should therefore be called on the hours object?

6b.

7a.Select the Show Code Pad from the View menu. Create a NumberDisplay object with 
limit 6 in the Code Pad by typing :
NumberDisplay display = new NumberDisplay(6);
Then call its getValue and increment methods in the Code Pad, by typing 
display.getValue() and display.increment();.
Note that the call to increment will need a semicolon at the end because it is a 
statement – telling the object to do something – while the call to getValue does 
not because it is asking the object to return a value (the call is an expression).
Use the recorded method calls in the Terminal window to help you with the correct 
way of writing these method calls.


7b.

8a.A call to setValue will need to include a numerical parameter value. Call the 
setValue method on the display variable – you will need to include a semicolon at 
the end. Call it first with a value less than the limit (e.g., 3) and check the 
result with a call to getValue, which does not need a semicolon. Then call it 
with a value greater than the limit (e.g., 10) and check the result with a call 
to getValue. Did both calls to setValue result in a change to the stored value? 
Can you explain the results?

8b.

9a.In the Code Pad, create a NumberDisplay object called digit with a rollover 
limit of 10. Now call its setValue method with a value of 10. Predict what the 
result of calling getValue on it will be immediately after the call to setValue. 
Getting the correct answer to this exercise will help you to know whether you 
understand how the rollover limit works with NumberDisplay objects. If you predicted 
incorrectly, then review the previous sections and read on further to help to clarify 
your understanding.

9b.

10a.What error message you see in the Code Pad if you type the following?
NumberDisplay.getValue()
Take a careful look at this error message and try to remember it because you will 
likely encounter something similar on numerous future occasions. Note that the 
reason for the error is that the class name, NumberDisplay, had been used incorrectly 
to try to call the getValue method. Instead of the class name, we must use the 
variable name, such as display. We shall explore this error in more detail later in 
this chapter.

10b.

11a.What error message do you see in the Code Pad if you type the following?
display.setValue(int 5);
The error message is no actually very helpful at all. Can you work out what 
is incorrect about this call to setValue, and correct it? It would also be worth 
remembering this error message because it results from an easy error to make in 
the early stages of learning.

11b.

12a.Replace the “<” operator in the setValue test with “<=” so that it reads
if((replacementValue >= 0) && (replacementValue <= limit))
Now repeat exercise 9. Make sure that you understand the reason for the difference 
between the two outcomes. Replace the “<=” operator with the original “<” operator 
before continuing.

12b.

13a.What is the only valid parameter value that would no longer set the value field 
if you replaced the “>=” operator in the test with “>” so that it reads 
if((replacementValue > 0) && (replacementValue < limit)) 


13b.

14a.What are some of the invalid parameter values that would now be able to set the 
field if you replaced the && operator in the test with so that it reads ││
if((replacementValue >= 0) (replacementValue < limit))

14b.

15a.Which of the following expressions return true?
! (4 < 5)
! false
(2 > 2) ((4 == 4) && (1 < 0)) ││
(2 > 2) (4 == 4) && (1 < 0) ││
(34 != 33) && ! false
After writing your answers on paper, open the Code Pad in BlueJ and try it out.
Check your answers.

15b.

16a.Write an expression using boolean variables a and b that evaluates to true 
when a and b are either both true or both false.

16b.

17a.Write an expression using boolean variables a and b that evaluates to true 
when only one of a and b is true, and that is false if a and b are both false 
or both true. (This is also called an exclusive or.)

17b.

18a.Does the getDisplayValue method work correctly in all circumstances? What 
assumptions are made within it? What happens if you create a number display 
with limit 1000, for instance? Try this out: create a NumberDisplay object and 
call its setValue method with a three-digit value. What is returned from a 
call to getDisplayValue? Is it a two-digit String?

18b.

19a.Is there any difference in the result of writing
return value + "";
rather than
return "" + value;
in the getDisplayValue method?

19b.

20a.Predict, and then test, the result of these two expressions:
9 + 3 + “cat”
and
“cat” + 3 + 9
Did they surprise you? Explain why the results are what they are

20b.
