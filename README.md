# Ternary-Operations

Imagine you're playing a game and you need to decide what reward to give a player based on their score.  Ternary operations are a shortcut way to write these decisions in code, kind of like an "if-else" statement on steroids.

Here's how it works:

* You write a **condition** that checks something, like if the player's score is high enough.
* You put a question mark after the condition.
* Then you write the **reward** for if the condition is true (like a special weapon).
* You put a colon after the reward.
* Finally, you write the **reward** for if the condition is false (like some health points).

The whole thing gets squished into one line of code!  Here's an example:

```
reward = score > 1000 ? "Legendary Sword" : "Health Potion"
```

This code checks if the `score` is greater than 1000. If it is, the player gets the "Legendary Sword".  If not, they get a "Health Potion". 

Here's another example:

```
hasKey = answer == "secret" ? True : False  
```

This code checks if the `answer` matches the secret word "secret". If it does, `hasKey` becomes True (meaning the player has the key). If not, it becomes False.

Ternary operations are handy for short decisions, but they can get confusing if you nest them (put one inside another) too much.  So keep them simple and clear, and your code will be easier to read for you and others.  


**Movie Rating:**

Imagine you're coding a movie recommendation app. You want to display a message based on the viewer's age:

* Ternary Operator:

```
message = age >= 13 ? "Enjoy the movie!" : "This movie is rated PG-13";
```

* Explanation:  
  - This checks if `age` is greater than or equal to 13.
  - If yes (true), the message is "Enjoy the movie!".
  - If no (false), the message is "This movie is rated PG-13".

2. **Free Shipping:**

Let's say your code calculates the total order amount. You want to offer free shipping if the order is above $50:

* Ternary Operator:

```
shippingCost = totalAmount > 50 ? "Free Shipping" : "$5 Shipping";
```

* Explanation:  
  - This checks if `totalAmount` is greater than 50.
  - If yes (true), shipping is "Free Shipping".
  - If no (false), shipping is "$5 Shipping".

3. **Dress Code:**

You're working on a party invitation program. You want to display a dress code message based on the time of day:

* Ternary Operator:

```
dressCode = hour < 18 ? "Dress casual" : "Dressy attire";
```

* Explanation:  
  - This checks if `hour` is less than 18 (6PM).
  - If yes (true), dress code is "Dress casual".
  - If no (false), dress code is "Dressy attire" (assuming it's after 6PM).

Remember, these are just a few examples. Ternary operations can be used for any short decision you need to make in your code!


**Ternary Operator Breakdown:**

The ternary operator, also known as the conditional operator, acts as a shortcut for writing if-else statements in a single line. Here's the syntax:

```
condition ? expression_if_true : expression_if_false
```

**Breaking it down:**

1. **condition**: This is any expression that evaluates to true or false. Remember, truthy values include `true`, non-zero numbers, strings, and objects. Falsy values are `false`, `0`, `null`, and `undefined`.
2. **?**: The question mark separates the condition from the outcome based on its truth value.
3. **expression_if_true**: This expression is executed if the `condition` is true.
4. **:**: The colon separates the true expression from the false expression.
5. **expression_if_false**: This expression is executed if the `condition` is false.

**Examples:**

1. **Age check:**

```
age >= 18 ? "You can vote" : "You cannot vote"
```

Here, if `age` is 18 or greater (truthy condition), `"You can vote"` is assigned. Otherwise, `"You cannot vote"` is assigned.

2. **Assigning a default value:**

```
let name = prompt("Enter your name: ") || "Guest";
// Ternary equivalent
let name = prompt("Enter your name: ") ? prompt("Enter your name: ") : "Guest";
```

Both achieve the same outcome. If the user enters a name (truthy value), it's stored. Otherwise, "Guest" is assigned as the default.

3. **Setting minimum value:**

```
let temperature = 10;
let minTemp = temperature < 0 ? 0 : temperature;
```

This ensures `minTemp` always holds a non-negative value. If `temperature` is less than 0 (truthy), `minTemp` is set to 0. Otherwise, the original `temperature` is assigned.

**Nesting Ternary Operators:**

You can nest ternary operators for more complex logic, but be cautious as it can decrease readability. Here's an example:

```
let grade = 85;
let letterGrade = grade >= 90 ? "A" : (grade >= 80 ? "B" : "C");
```

This assigns a letter grade based on the `grade` value. While it achieves the goal in one line, using a regular if-else structure might be clearer for complex logic.

**Key Points:**

* Ternary operators have lower precedence than most other operators. Use parentheses for proper evaluation order if needed. 
* While concise for simple if-else scenarios, consider readability for complex logic. Regular if-else statements might be better in those cases.
