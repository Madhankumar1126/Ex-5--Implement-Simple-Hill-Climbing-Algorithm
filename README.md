<h1>ExpNo 5 : Implement Simple Hill Climbing Algorithm</h1> 
<h3>Name: Madhan kumar J </h3>
<h3>Register Number: 2305001016 </h3>
<H3>Aim:</H3>
<p>Implement Simple Hill Climbing Algorithm and Generate a String by Mutating a Single Character at each iteration </p>
<h2> Theory: </h2>
<p>Hill climbing is a variant of Generate and test in which feedback from test procedure is used to help the generator decide which direction to move in search space.
Feedback is provided in terms of heuristic function
</p>


<h2>Algorithm:</h2>

</p>
<hr>
<h3>Step-1</h3> <p> Read the target string from the user.</p>
<h3>Step-2</h3> <p>Generate a random initial solution of the same length as the target.</p>
<h3>Step-3</h3> <p> Calculate the score (difference) between the current solution and the target.</p>
<h3>Step-4</h3>
<p> Repeat the following steps until the score becomes zero: a. Display the current score and solution. b. Mutate one random character in the current solution to create a new solution. c. Calculate the score of the new solution. d. If the new solution has a lower score, replace the old one.</p>
<h3>Step-5</h3> <p> When the score becomes zero, stop the process.</p>
<h3>Step-6</h3> <p>  Print the final solution as the target string.</p>

## PROGRAM
```
import random, string
def hill_climb():
    target = input("Enter the target string: ")
    sol = [random.choice(string.printable) for _ in target]
    score = lambda s: sum(abs(ord(a)-ord(b)) for a,b in zip(s, target))
    best, best_score = sol, score(sol)

    while best_score:
        print(best_score, "".join(best))
        new = best.copy()
        new[random.randrange(len(new))] = random.choice(string.printable)
        new_score = score(new)
        if new_score < best_score:
            best, best_score = new, new_score

    print("Final:", "".join(best))

hill_climb()
```

<hr>
<h2>Sample Input and Output</h2>
<h2>Sample String:</h2> Bee
<h2>Output:</h2>

<img width="306" height="692" alt="image" src="https://github.com/user-attachments/assets/c80ef84e-5d7f-4980-93ce-b2d5808df0e8" />

<p>.   .   .   .  .  .  . </p>
<p>.  .  .  .  .  .  .  .</p>
<p>.  .  .  .  .  .  .  .</p>

<img width="171" height="233" alt="image" src="https://github.com/user-attachments/assets/89430128-9479-44a6-abdc-c630ee087106" />


## RESULT:
Thus the program to Implement Simple Hill Climbing Algorithm has been executed successfully.
