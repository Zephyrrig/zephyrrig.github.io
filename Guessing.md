```mermaid
flowchart TD
    A[Start] --> B{Integer Secret}
    B --> C{Integer guess}
    C --> D["`secret = random(20)+1`"]
    D --> E["`Output 'Guess a number from 1 to 20'`"]
    E --> F[Input guess]
    F --> G[guess != secret]
    G --> |True| H{guess>20 or guess<1}
    H --> |True| I["`Output 'Please pick a number from 1 to 20'`"]
    I --> J{ }
    H --> |False| J
    J --> K[guess > secret]
    K --> |True| L[Output 'Too High']
    L --> M{ }
    K --> |False| M
    M --> N[guess < secret]
    N --> |True| O[Output 'Too Low']
    O --> P{ }
    N --> |False| P
    P --> Q[Output 'Try Again']
    Q --> R["input guess"]
    R --> G
    G --> |False| S[Output 'Congratulations, you win!']
    S --> T[End]
	
```

- B and C are establishing secret and guess as integers for the game.
- D is assigning a variable named "secret" as a random number from 1-20
- E is giving a prompt for guessing "guess"
- F is to establish the variable "guess"
- G is checking if you got it correctly, if not, you get into the H through R loop.
- H is checking if the number is beyond the bounds of the question
- L is checking if the number is too high
- N is checking if the number is too low
- Q is prompting you to try again and input a new value for "guess"
- S is the output if you get it correct and win.