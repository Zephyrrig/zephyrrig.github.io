```mermaid
flowchart TD
	A[Main] --> B{Integer Secret}
	B --> C{Integer guess}
	C --> D[secret = random(20)+1
	D --> E[Output "Guess a number from 1 to 20"
	E --> F[Input guess]
	F --> G[guess !=secret]
	G --> H{guess>20 or guess<1}
	
Start([Start]) --> End([End])
```

