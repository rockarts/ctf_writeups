This is the code for the Stairway to Hell challenge for the Hacktober CTF. I really liked seeing a CTF with some programming challenges, I hope to see more in the future.

For this challenge we had to generate a staircase. Here is the code in Kotlin:


```kotlin
fun main() {
    var start = 665

    //Build the steps.
    for (i in 1..30) {
        //Print the numbers. Starting with 666
        for(i in 1..i) {
            start++
            print("${start} ")

        }
        //Go to next step. 
        println()
    }
}

```

Submitting the correct answer proved to be challenging. We had to remove newlines which got rid of the steps. 
You then had to submit multiple times until your answer was accepted. Even when I got the flag I got the "Stop wasting my time." message. 
After I answered I tried helping multiple people in the slack channel with the correct format and telling them to resubmit. 

```bash
$ nc env2.hacktober.io 5001 < stairway.txt
DEADFACE gatekeeper: You haven't convinced me yet. Start with 666 and build a staircase of 30 steps. Strip out newlines and keep spaces between numbers. Send me all 30 steps and I'll know you're the real deal.

Stop wasting my time.
Connection Closed.

flag{plung3_to_the_4by55}
```
