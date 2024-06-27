# 20.2.8-funds

## School Fundraising


You are the captain of a team of students competing in a competition to raise funds for a major charity.  The event wraps up with a major party.  You will use Arrays to track your team members and their donations raised.  



## Step 0 - 20%
1. Set up 3 parallel Arrays of 10 students:
- Their names. Make the 9th person you.  (hint, name is a reserved word, use nom or names etc.)
- The total amount each has raised to date for the charity.  
- Hard code in the values so that each person has raised a different amount of money.  Range your values between $0 and $500.
    - Make sure to have some students below the $40 minimum threshold (explained further down)
- A Boolean Array stating whether or not they have returned their permission forms to attend the big wrap up party.
  - For testing/marking purposes, set half to be true and half to be false
   - Tip: for the easiest use of boolean variables, do not use quotes or capitals. Simply say  `let forms = [false, true, true,...]`

## Step 1 
Display on the canvas all three Arrays using a single `For` Loop so that each student’s name appears with their dollar amount and true/false value beside it.

## Step 2 - Next 60%
Use separate for-loop algorithms for each of the following. Run them in `Draw()` and display the result with a clear label.  

Make sure your lists are displayed well labeled:

- **TOTAL and AVERAGE** - Calculate and display the total and average amount raised by your team. **(20%)**

- **COUNTIF** - To attend the big party, students must have raised a minimum of $40. If you have more than 2 students who have not raised the minimum amount, your team must work a weekend bottle drive.
  - **COUNTIF** the number of students who raised less than $40 and display that number.
`IF` that number is greater than 2, display “Bottle Drive NOT required”.  `ELSE`, display  “Bottle Drive is this Saturday” **(20%)**

- **HIGHEST** - display the highest amount raised and that person’s name **(20%)**
		Our highest fundraiser was Jack who raised $790;


## Step 3 - Final 20%


- **SUMIF** - It is getting to crunch time. Those who have not turned in the forms will not be able to participate.
  - Use our SUMIF algorithm to add the amounts raised but only by students whose forms are handed in. Then display this amount.    **(10%)**
		Fees raised by those with permission to attend: $250
    - Reminder: the SUMIF algorithm is the same as a total algorithm but with an IF statement inside.

- **DOOR PRIZE** - Add the functionality so that every time I click the mouse, it randomly chooses a different team member and displays their name so we can give out a door prize.  In other words, when I click the mouse one name is displayed.  It should be random so that each time I click the mouse, the name is re-randomized. It is ok if the same name is chosen twice. **(10%)**
	`[mouse is clicked] This door prize goes to:  Tim`
	`[mouse is clicked] This door prize goes to:  Thom`
	`[mouse is clicked] This door prize goes to:  Tam`
    - Hint: This does NOT need a FOR loop.  It should take at most 2 lines of code. One to generate a random number and one to display the name.
    - Hint #2:  The javascript RANDOM function returns a decimal number so you need to round down.  I recommend using `FLOOR`.  
	`floor(random(0,6))`  will generate a 0, 1, 2, 3, 4 or 5 but not a 6.

```
No starter code for this one
```
