# Pseudocode: 
## Logic to get computer's choice:
### Requirements: 
- A function named *getComputerChoice()* should be created

    - the built-in random function should be used to generate a random choice between 3 options (rock, paper, scissors).

        - random function only works with integers, each integer should be matched with a string (0 = rock, 1 = paper, 2 = scissors)

        - The random function should return the value as strings

- The output from the function should be communicated to the user

___

### Pseudocode:

    FUNCTION getComputerChoice()

        choice <- Math.floor(Math.random()*3); 

        RETURN choice;

    FUNCTION END


*computerChoice* <- **CALL** *getComputerChoice()*

**DECLARE** *acceptance* as **BOOL**;

    (computerChoice === 0 || computerChoice === 1 || computerChoice === 2) ? acceptance =  true : acceptance  = false;

<br>

    FUNCTION intToValue (acceptance as BOOL, computerChoice as NUMBER)

        DECLARE value as STRING;

        IF (acceptance === true && computerChoice === 0)
            THEN value <- "Rock";

        ELSE IF (acceptance === true && computerChoice === 1) 
            THEN value <- "Paper";

        ELSE value <- "Scissors";

        END IF

        RETURN value;

    END FUNCTION

*finalComputerValue* <- **CALL** *intToValue* (*acceptance*, *computerChoice*);
___

## Logic to get human's choice: 
### Requirements: 

- Need a function called *humanChoice()* to receive and output the user's choice 
    - The users choice should be inputed into the console using *prompt()*
        - Need a message to inform them what to input and a space for the user to input their choice.
    - Provide 3 options for the user to input. They can input one of the follow 3 options: 
        - Rock
        - Paper
        - Scissors 
    - Need a way to capitalize every user string input to avoid any string mismatch cases. (If user inputs "rOcK"/"rOCK")


___
### Pseudocode:

    DECLARE user_input as STRING
        
    DISPLAY "Enter your choice"
    user_input <- INPUT()

    DECLARE capitalize as STRING
    capitalize <- user_input.toUpperCase()

    FUNCTION choiceChecker(capitalize) 
        
        DECLARE humanChoice as STRING

        //Using ternary operator to mimic if/else statement
        (capitalize === "ROCK") ? humanChoice = capitalize:
        (capitalize === "PAPER") ? humanChoice = capitalize:
        (capitalize === "SCISSORS") ? humanChoice = capitalize:
        humanChoice = "Invalid input message";

        RETURN humanChoice;

    END FUNCTION

    DECLARE finalHumanChoice as STRING;

    finalHumanChoice <- CALL choiceChecker(capitalize)

___
