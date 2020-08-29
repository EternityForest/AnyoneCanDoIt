# Math: Explain it like I'm 5

Inspired by a subreddit. All the math that someone
with no math talent knows and uses without actually understanding,
and the facts that people who actually knows math seem to think are "too obvious"
to write down.

None of the fundamentals and excercises I never learned. You
should probably go actually learn math. 


Alpha quality! Hasn't been reviewed!




## Base systems

### Base 10
Base 10 is when each digit has 10x the value of the last. `111`= one hundred, one ten, and one one.



The number of combinations of an N digit lock is 10**N. For three digits, you
start with ten choices for the first.

For every possible choice, there are ten more choices, giving 100 total.

For each of those 100, there are now 10 choices for the final number, giving 1000 total.

Note that a real three digit number only goes up to 999, although there are a thousand possibilities, 
because zero is the first possibility.

This fact causes massive numbers of errors in programming, when people get confused by it.  They are generally known as a type of off-by-one error.

### [Base 2(Binary)](https://en.wikipedia.org/wiki/Binary_number)
Base 2 aka binary is the same thing with 2s. `1111`= one 8, one 4, one 2, and one 1

Since they look the same, in programming we mark binary literals with 0b, as in: `0b11` = 3 = 2+1

The number of possible combinations of N bits, is always 2 to the N.

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

## Percents

Percents are pretty much multiplication. 10 percent of
50 is the same as 10 times 0.10.

Note that there are 100 percent steps, and 100 steps
of 0.01 between 0 and 1, which is why this works.

This also means that percentages are reversible, because multiplication is.

10 percent of 50 is 5.  50 percent of 10 is also 5. Many times
the reversed version is easier to mentally calculate, if for some unlikely reason you don't
have your phone.

As an aside, some math people will insist this is very
obvious, but like most of the stuff in this file, I only know because
of some random Facebook meme.


## Division

### Relation to Multiplication

Multiplying by 1/x  is the same as dividing by x.

But division by a variable does not produce a linear plot.

12 divided by 6 is 2.  12/3 is 4.   When we have half the divisor,
we get double the output. It seems like this should result in a linear chart,
to someone (like me!). without a real understanding of math.

But if one plots 1/x on a graph, the result is not linear.  I don't actually
know why, but not knowing about it wasted my time on a programming problem one time,
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


## Exponentiation 

2**5 means "Two times itself five times, or 2*2*2*2*2". It is also said as
"Two raised to the power of five" or "to the fifth power" or similar.

Numbers which can be written as 2**something are powers of two, the first few of which are:
1, 2, 4, 8, 16, 32, 64, 128, 256, 512,1024, 2048, 4096, 8192

These numbers are extremely common when dealing with computers, and numbers that are
two to some other power of two(2**8=256, 2**4=16, etc) are especially common.

The number of possible combination of N bits is 2**N.

### Squaring

X**2 is Squaring, as mentioned before, and it gives you the
area of a square, if X is the length of the sides.

To go backwards, and get length from an area, one would use a square root.

x**3 is cubing.  It gives you the volume of a cube given the length of it's edge.



### X**0

Any positive real number raised to the power of 0, is 1. 
Any negative real number raised to the power of 0, is -1

I am sure there's a cool math reason for this, but it
also happens to be really convienent in programming.


### 0**0

I have no idea what is going on here.  Android calculator thinks it
is "Undefined, or 1”.  That probably means you shouldn't rely
oon it to do something sane in 
 programming languages if you don't specificaly check the spec.

I have never seen this in real life, or thought of it before just now.

## Sine waves

sin(x), when graphed, makes a sine wave. Those waves 
are a pure frequency, but only if infinitely long.

Any finite wave has the "Clicks and pops" of the starting and ending, but in
practice, some waves are thought of as pure tones.

Any repeating periodic sound or RF pattern or any other wave you can plot on a graph,
can be made of different stacked sine waves
of different frequencies, powers, and offsets.

Figuring out what waves go into something is what a Fourier Transform does.

Inverse Fourier Transforms can calculate a waveform given the "ingredient" sine waves.

Most kinds of nonlinear functions (Like vaccum tube distortion!) will add new frequencies not in the input.
This will sound audibily distorted, and interfere with the operation of various circuits that might be interpreting it.


### Sampling

If you are taking digital samples of a signal, and you sample slower
than twice the frequency of the highest sine wave, you get aliasing,
which causes the familiar illusion where helicopter blades go backwards,
and which can make a sawblade under fluorescent light stand still.

If you always sample at the very top of the wave, it will look like you have an 
unchanging signal.

Aliasing will usually create an illusory sine wave for every input wave above the cutoff,
 at some related  frequency.

### Harmonics

The familiar square, triangle, sawtooth, etc waves that repeat, but are not sine waves, are made
up of a sine at the "main" frequency, and a set of sines at multiples of it.

Creating a perfectly sharp square requires infinite waves, which is
why perfectly sharp waves aren't usually a thing in real life.

When distortion distorts a sine wave, the additional new tones are usually at multiples
of the frequency.  This is not true of aliasing, which makes sines at "reflected" points.

This is why aliasing sounds harsh and unmusical.

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

## Algebra

As typically encountered, algebra is the fact that you 
can move parts of equations around to make new equations,
which are guaranteed to be true if the original is true.

Suppose you have 10 feet of wood to build a 16:9 frame.

X and Y are the final horizontal and vertical dimensions.

You know that X/Y=16/9,  because that's the ratio you want.

you know that X+Y is 10 feet, if we just ignore concerns about inner
outer size for now.

Now you have 2 simultaneous equation that can be solved to find X and Y.

Normally, people who are actually learning this stuff start
with single equations, and don't progress to simultaneous equations till later.

But when telling a computer to solve it for you, it's all trivially easy anyway.

And also, I can't think of any practical examples with
just one equation.


I am told that learning to actually do this by hand opens
up a whole new way of thinking, and you may want to actually learn it.


### Solutions?

Some equations may have multiple solutions. Depending
on context, it may mean you have multiple options, or,
that the information you want cannot be found from
the input.

Given the average brightness of an image, there's no algebra
to return the original picture, it is simply lost.


In some cases, there may be conflicts between different
equations, and one might want to instead find the answer
with the least total amount of error, or, on some cases,
the least *squares* of the errors.

This usually happens when there are more equations than
unknown variables you are looking for, and is called an overdetermined system.

This conflict is similar to the same kind of thing in
an overconstrained machine design.

## Calculus

This deals with the study of continuous things that
don't seem to have an answer otherwise. Actually learning this
is said to expand your mind even more, and to be a very fulfilling experience.

I can't actually say I have ever used anything like it I'm real lifez
but the people who knows it, use it *all the time*, on projects that could not 
happen without it.
