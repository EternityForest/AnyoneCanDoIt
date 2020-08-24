# Math: Explain it like I'm 5

Inspired by a subreddit.  You might call this "Looking at math the completely wrong way, for people who should probably just actually learn it".

Or, you could call it an experiment to write down all the math used in practice by a totally non-math person.

## Base systems

### Base 10
Base 10 is when each digit has 10x the value of the last. `111`= one hundred, one ten, and one one.

### [Base 2(Binary)](https://en.wikipedia.org/wiki/Binary_number)
Base 2 aka binary is the same thing with 2s. `1111`= one 8, one 4, one 2, and one 1

Since they look the same, in programming we mark binary literals with 0b, as in: `0b11` = 3 = 2+1

### Base 16(Hexadecimal)

Hex is the same, but with 16 values, 0 through 15 and, we use ABCDEF for the extra numbers. We mark hex with 0x(I don't know why). `0xFF` = 15*16 + 15*1 = 255 = the max number you can fit in a byte.

Now because four bits has 16 possible combinations(2 to the 4), we can use one hex digit(having 16 possible vals) to represent four bits.
This means we can use two hex digits for 8 bits, which is a byte, which makes hexadecimal very useful for binary data.

### Base 64
This is normally represented as ASCII text, and in the usual applicaion, is a little more complicated because
64 combinations only represents 6 bits, and bytes work with 8, meaning we must stufff three bytes into 4 characters, 
and in some cases special padding rules apply to the decoders.

Nonetheless, it is the same as the other base systems.

### Non-integer bases
These exist, but I am not going to pretend to understand them :P

## [Linear](https://en.wikipedia.org/wiki/Linear_function_(calculus)) and Nonlinear functions

This will come up a whole lot.  For any function that takes a number as
an input and returns another number, some will be linear, and others will not.

Linear functions make a straight line if you graph the input vs the output.
Linear functions behave similarly at any scale, the same size input step makes the same size output step, no matter what the value was.When dealing with a nonlinear function, you might find:

* Audio distrotion. Linear functions won't add new frequencies to sound.  Crunchy electric guitar like stuff is nonlinear.

* Thresholds.  Stuff won't behave the same at different power levels, file sizes, or whatever.  
* Some nonlinear functions will have huge changes for small steps past a certain point.
* Diminishing returns.  Some nonlinear functions will take more and more input for the same amount of output change.

When dealing with linear functions in things you can directly perceive, like light, it probably won't
look linear, because eyes and ears don't have a linear response.  Brightness generally has a diminishing returns type curve, it
takes more power to look twice as bright the higher you go.

There is usually no way to combine different linear functions to get something nonlinear.


## Multiplicaton

## Linearity

A constant times X makes a linear graph.  X times X is the same as X**2, which is most 
definitely not linear.

### Rectangles
Multiplying the lengths of the sides of something gives the square area.  4ft* 8ft= 32 square feet.  1ft* ft=1 square foot.

#### Algorithm Complexity 
This also means that any algorithm like "Do something with every possible pair of one input from the list A and one from B" will take an amount of time proportional to the length of A times the length of B, since every step in the algorithm is one of the "Square feet" in the "table" where each side has one foot per item on the list.

If A and B are the same, then the area will be A squared, and this is fairly common in programs. If you see this pattern, maybe try to do something about it, because it will get very slow.

Example: You have 100 items, and you want to display a statistic like "This is more expensive than 99% of items".  If you loop over every one, and compare it to all the others, you will do 100 * 99 comparisions.

Instead, you could pass the full list to a proper sorting algorithm(Which uses code I don't understand to sort things much faster than comparing every element to every other), and simply look at how high up everything is on the list.  The second item costs more than 1% of items and less than 98%.

### Scaling

It can also make things bigger or smaller. x * 0.5 is half of something, x * 2 is twice that thing.  Because it is linear, 
doing this to an audio signal will not distort.

Multiplying by zero is always zero, like a closed gate letting through 0% of what tries to come in.

### Negative numbers

Multiplying by a negative number inverts. 5 times -2 is -10. -5 times -2 is 10.  This is useful in signal processing.


## Division

### Relation to Multiplication

Multiplying by 1/x  is the same as dividing by x.

But division by a variable does not produce a linear plot.

12 divided by 6 is 2.  12/3 is 4.   When we have half the divisor,
we get half the output. It seems like this should result in a linear chart,
to someone (like me!). without a real understanding of math.

But if one plots 1/x on a graph, the result is not linear.  I don't
know why, but not knowing about it wasted my time on a programmer problem one time,
so I'm writing it down!

#### Fig. 1: Plot of 1/x, not a straight line at all.
![Not what you'd expect?](images/math/one_over_x.png)

### Negative numbers

5/-1 is -5.  I don't think I've ever seen division by a negative in real life. It is confusing.

### [Division by zero](https://en.wikipedia.org/wiki/Division_by_zero)

This is not usually a thing that can be done, except in some wierd algebra thing where you
figure out a result indirectly, maybe.


Computers will generate NaN, not a number, infinity, or just raise an error.
Whenever you are dividing by X, where X is the product of some kind of algorithms, be sure it will not ever be zero,
if you don't want your system to crash.



## First order filters
You can use this to make a simple smoothing filter.  At every step, when you get a new input `i`, set x to `x*0.7 + i * 0.3`.

You are essentially moving about a third of the way between where you are and the new input every step, smoothing the input
by slowly approaching it, filtering fast changes.

Why 0.7 and 0.3? They have to add up to 1, but any two numbers can be used, and you can change them to control the speed.

Obviously, if we have an input that's the same as the current state, nothing should change. If the total is less than one, the value would decrease, and if it was greater than one, it would increase, because x and i are the same. 

Half of 5 and half of 5 again (Because the state and input are the same) is the same as the 5, but  half of five plus a third of five is clearly less.  

To be sure they add up to 1, we might code it as `x = x*(1-s) +  i*s`, where s is our "speed".  Whatever we add to the s, gets taken away from that 1, so (1-s) and s always add up to one.

This is an example of exponential decay, as every step, the difference between input and output is reduced by the speed factor.

In real life, if our time steps are not perfectly even, we will need more complicated math to account for this fact.

### Filter [Time Constants](https://en.wikipedia.org/wiki/Time_constant)

We will also need to choose the "speed" appropriately. Typically, people have a Time Constant in mind. A time constant is the time
it takes for the difference between the input and output to decay to 1/e (about 37%) of the input, after an instant step change.

It is also the time it *would* take for the difference to decay to zero, if it kept on decaying at the same rate as right after the step change.
As it does not do that, and progressively slows down as it gets closer, the difference will never actually get to zero in theory. In real life,
it will, because numbers in computers have limited precision.

#### Linearity

These filters are apparently "linear", even though if you plot the response to a step change over time, they don't look like they are.

Nonetheless, they will not introduce new frequencies into the signal, just attenuate or enhance existing ones, annd if applied to audio,
will not add distortion.

#### Similarity to [RC filters](https://en.wikipedia.org/wiki/RC_circuit)

The common RC first order lowpass filter acts a very similar way. The time constant is determined by τ=RC.
In this formula, τ is measured in seconds, R in ohms and C in farads.

Note that the greater the difference between input and output, the faster it moves, the same as in our code, where the movement is
always a fraction of that distance.



![RC Lowpass filter](images/math/rc_lowpass.png)