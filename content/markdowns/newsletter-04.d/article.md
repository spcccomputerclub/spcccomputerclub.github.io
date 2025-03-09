### Speedrunning in coding
To the average student who may know little about coding, a Computer Literacy assignment may already pose an exciting challenge, not to mention questions or tasks that are explicitly designed to hamper with the minds of even seasoned programmers. Yet would it be surprising if you were told that even these problems serve as toys or competitions to the most dedicated? That’s right, they’re battling it out for the fastest runtime – and one major factor of this benchmark is __runtime complexity__. 

## **The Big O Notation**
### Introduction
*Runtime complexity* is a way to measure how an algorithm’s time grows as the data size increases. The *Big O Notation* is essentially the most recognised way to classify runtime complexity. It usually appears as a Capital letter “O” followed by some expression involving lowercase *n* (roughly representing input size). Some examples include *O(1), O(n), O(n²)* etc. 

### Explaining Big O

Imagine you’re running a lemonade stand, and Big O is like a way to predict how much time it’ll take you to serve customers as more people show up. It’s not about exact minutes or seconds—it’s about the *pattern* of how your workload grows. 

Here’s how it works, super simple: 

 ![Big O 1](/assets/img/0005/Big%20O%201.jpg)

- __O(1) - Constant Time__: Picture this: You’ve got a megaphone. No matter how many customers line up—10 or 1,000—you just yell, “Lemonade’s ready!” once, and everyone hears. Takes the same effort every time. That’s *O(1)*—the job doesn’t get harder as the crowd grows. 

- __O(n) - Linear Time__: Now imagine you’re handing out cups one by one. If 5 people show up, you hand out 5 cups. If 50 show up, it’s 50 cups. The more customers (let’s call that number n), the more work you do—twice as many people, twice the time. That’s *O(n)*—it grows steadily with the crowd. 

- __O(n²) - Quadratic Time__: Here’s a tough one: Say you’re super friendly and insist on shaking hands with every customer and letting them shake hands with each other. For 3 people, it’s a few handshakes. For 10, it’s a ton—everyone’s shaking hands with everyone! The work explodes as more people join. That’s *O(n²)*—the effort grows way faster than the line itself. 

- __O(n log n) - Linearithmic Time__: This one’s trickier, but think of it like organizing your customers into groups super efficiently. You split them in half, serve each half, split again, and so on—like a speedy sorting trick. It’s more work than O(n), but way less than O(n²). It’s a middle ground—grows, but not crazily. 

### The Big Picture 

Big O isn’t about exact timing (like “this takes 5 seconds”). It’s about how your task scales. Small crowd? No big deal. Huge crowd? Some methods (like *O(1)*) stay easy, while others (like *O(n²)*) turn into a nightmare. Programmers use it to pick the smartest way to handle big jobs—like serving lemonade to a million thirsty folks without losing their minds! 

## Conclusion 

While these unique notations may not seem as relevant and common in our daily lives outside computer science, they are actually useful tools to evaluate a programs efficiency, and how different methods and functions can be used to enhance run speed even further; In big computations such as AI training, every second counts. So while we probably shouldn’t try expressing our speed of fleeing after the bell rings through runtime complexity (it’d probably be *O(0)*), perhaps someday more advancements will be made due to this clever mechanism! 

![Big O 5](/assets/img/0005/BigO5.png)
