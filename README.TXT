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

1b.Photo of said diagram

2a.At what time(s) can a class diagram change? How is it changed?

2b.When a class is created or a new relationship between the classes or objects
is established, such as making one class inheret from another, an arrow would 
point to the class that is being extended by the class.

3a.At what time(s) can an object diagram change? How is it changed?

3b.When adding new Student objects or removing them.

4a.Write a definition of a field named tutor that can hold a reference to an 
object of type Instructor.

4b.private Instructor tutor;

5a.Open the number-display project. Select Show Terminal from the View menu 
and select Record method calls, as you did with the figures project in chapter 
1. This will allow you to see the result of your interactions with objects, 
which will be useful when we look in detail at the full clock-display project. 
Now create a NumberDisplay object and give it the name hours, rather than using 
the default name offered by BlueJ. Use a rollover limit of 24. Open an inspector
window for this object. With the inspector open, call the object’s increment method. 
Note what is shown in the Terminal window. Repeatedly call the increment method 
until the value in the inspector rolls over to zero. (If you are feeling impatient, 
you could always create a NumberDisplay object with a lower limit!)

6a.Create a second NumberDisplay object with a limit of 60, and give it the name 
minutes. Call its increment method and note how the method calls are represented 
in the Terminal window. Imagine that the hours and minutes objects on the object 
bench represent the two NumberDisplay objects managed by a ClockDisplay object. 
In effect, you are now performing the role of the ClockDisplay object. What 
should you do each time you call increment on minutes to decide whether it has 
rolled over and whether increment should therefore be called on the hours object?

6b.Only when the value stored in the minutes numberDisplay rolls over, then it should
increment the hours numberDisplay by 1.

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

8a.A call to setValue will need to include a numerical parameter value. Call the 
setValue method on the display variable – you will need to include a semicolon at 
the end. Call it first with a value less than the limit (e.g., 3) and check the 
result with a call to getValue, which does not need a semicolon. Then call it 
with a value greater than the limit (e.g., 10) and check the result with a call 
to getValue. Did both calls to setValue result in a change to the stored value? 
Can you explain the results?

8b.No, only the value under the limit changed the stored value. I believe it is due
to the limit established when initiallizing the object. It could not accept the
higher value because it wasnt a legitimate value to store in this case.

9a.In the Code Pad, create a NumberDisplay object called digit with a rollover 
limit of 10. Now call its setValue method with a value of 10. Predict what the 
result of calling getValue on it will be immediately after the call to setValue. 
Getting the correct answer to this exercise will help you to know whether you 
understand how the rollover limit works with NumberDisplay objects. If you predicted 
incorrectly, then review the previous sections and read on further to help to clarify 
your understanding.

9b.It will be 0, since it rolls back once hitting the limit. 
NumberDisplay digit = new NumberDisplay(10);

10a.What error message you see in the Code Pad if you type the following?
NumberDisplay.getValue()
Take a careful look at this error message and try to remember it because you will 
likely encounter something similar on numerous future occasions. Note that the 
reason for the error is that the class name, NumberDisplay, had been used incorrectly 
to try to call the getValue method. Instead of the class name, we must use the 
variable name, such as display. We shall explore this error in more detail later in 
this chapter.

10b.There is also the fact that there isnt a semi-colon at the end I believe.

11a.What error message do you see in the Code Pad if you type the following?
display.setValue(int 5);
The error message is not actually very helpful at all. Can you work out what 
is incorrect about this call to setValue, and correct it? It would also be worth 
remembering this error message because it results from an easy error to make in 
the early stages of learning.

11b.display.setValue(5); The other spelling of the call is wrong since we are
not trying to initialize the parameter for a class. By writng "int", we are 
asking the program to specify a data type for a parameter when in actuality,
we simply wish to call upon a method.

12a.Replace the “<” operator in the setValue test with “<=” so that it reads
if((replacementValue >= 0) && (replacementValue <= limit))
Now repeat exercise 9. Make sure that you understand the reason for the difference 
between the two outcomes. Replace the “<=” operator with the original “<” operator 
before continuing.

12b.If Im guessing correctly, it should now display the limit, so 10, since we 
included into the accepted values we can display in the stored location. That
assumption was correct.

13a.What is the only valid parameter value that would no longer set the value field 
if you replaced the “>=” operator in the test with “>” so that it reads 
if((replacementValue > 0) && (replacementValue < limit)) 

13b. It is 0, since we exclude the value from being displayed, even though it is
technically correct to display 0 on it.

14a.What are some of the invalid parameter values that would now be able to set the 
field if you replaced the && operator in the test with so that it reads ││
if((replacementValue >= 0) (replacementValue < limit))

14b.It can be anything up following 10, even if 10 is our limit. We remove the extra
condition of having the replacement value being within the confines of our limit, so
now, we can put whatever value, that isnt in the negatives, in the display. 

15a.Which of the following expressions return true?
1.! (4 < 5)
2.! false
3.(2 > 2) || ((4 == 4) && (1 < 0))
4.(2 > 2) || (4 == 4) && (1 < 0) 
5.(34 != 33) && ! false
After writing your answers on paper, open the Code Pad in BlueJ and try it out.
Check your answers.

15b.In Java, the ! operator is known as the logical NOT operator. It is used to invert 
the value of a boolean expression. If the expression is true, applying the ! operator 
will make it false, and vice versa. And ││ is known as the Logical OR operator,
meaning it returns true if one of the statements is true, statement 1 ││ statement 2.
So,
1.False
2.True
3.False
4.False
5.True
All are correct.

16a.Write an expression using boolean variables a and b that evaluates to true 
when a and b are either both true or both false.

16b. a && b || !a && !b (other ways : a == b)

17a.Write an expression using boolean variables a and b that evaluates to true 
when only one of a and b is true, and that is false if a and b are both false 
or both true. (This is also called an exclusive or.)

17b. a^b

return true;

18a.Does the getDisplayValue method work correctly in all circumstances? What 
assumptions are made within it? What happens if you create a number display 
with limit 1000, for instance? Try this out: create a NumberDisplay object and 
call its setValue method with a three-digit value. What is returned from a 
call to getDisplayValue? Is it a two-digit String?

18b.It seems to be the case, the string displayed a three digit number. Though,
I think thats only the case if your inputted value is a positive integer number
within the confines of the initialized limit. It assumes that the number displayed
positive and corresponds to the windown within the limit. No, it is not a two-digit
String.

19a.Is there any difference in the result of writing
return value + "";
rather than
return "" + value;
in the getDisplayValue method?

19b.No, there doesnt seem to be any change.

20a.Predict, and then test, the result of these two expressions:
9 + 3 + “cat”
and
“cat” + 3 + 9
Did they surprise you? Explain why the results are what they are.

20b.For the first one, it will return : 12cat
For the 2nd one, it will return cat39.
I think...I was correct!The reason I know this is because in game programming,
we were told that if you start an additive operation with a Sring, the other things
added will become part of said strings and act as as though it is a concatination of
of strings rather than an addition with numbers. This is why it was cat39, since the
String came first and 12cat, becasue it was treated as an addition before seeing the
String that needed to be concatinated.
