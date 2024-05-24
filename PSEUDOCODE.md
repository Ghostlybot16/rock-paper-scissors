# Pseudocode: 
## Logic to get computer's choice:
### Requirements: 
- A function named getComputerChoice should be created

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