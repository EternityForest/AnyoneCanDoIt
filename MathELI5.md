# Math: Explain it like I'm 5

Inspired by a subreddit. All the math that someone
with no math talent knows and uses without actually understanding,
and the facts that people who actually knows math seem to think are "too obvious"
to write down.

None of the fundamentals and excercises I never learned. You
should probably go actually learn math. 


Alpha quality! Hasn't been fully reviewed!




## Base systems

### Base 10
Base 10 is when each digit has 10x the value of the last. `437`= four hundreds, three tens, and seven ones, or, more concisely, `4\*100 + 3\*10 + 7\*1 `

As a note, the multiplication by one at the end is does nothing, anything times one is just the number you started with, but in programming things are sometimes writen more verbosely to make the intent clear, although mathematicians may see it as unnecessary clutter.

The number of combinations of an N digit lock is 10\*\*N. For three digits, you
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

Hex is the same, but with 16 values, 0 through 15 and, we use ABCDEF for the extra numbers. We mark hex with 0x(I don't know why). `0xFF` = 15\*16 + 15\*1 = 255 = the max number you can fit in a byte.

Now because four bits has 16 possible combinations(2 to the 4), we can use one hex digit(having 16 possible vals) to represent four bits.
This means we can use two hex digits for 8 bits, which is a byte, which makes hexadecimal very useful for binary data.

### Base 64
This is normally represented as ASCII text, and in the usual applicaion, is a little more complicated because
64 combinations only represents 6 bits, and bytes work with 8, meaning we must stufff three bytes into 4 characters, 
and in some cases special padding rules apply to the decoders.

Nonetheless, it is the same as the other base systems.

### Non-integer bases
These exist, but I am not going to pretend to understand them.

## Arithmetic

This deals with the basic operations like addition and subtraction.  I have no reason to doubt
the teachers who say that learning this is essential for understanding the 
concepts. I will leave such discussions of education to them.

Perhaps if I somehow found time to learn it, I'd be making six figures
in a chemistry lab, rather than writing this!

But in any case, it is rather uncommon to need to calculate something
while you are away from a smart phone, so for the purposes of getting by
without actually understanding it, this is entirely a computer's job.


## Variables

Variables are placeholders, usually a number, for something you don't know yet.

Often they the "Inputs and outputs" of a formula, allowing you to state an equation that describes something general,
even if you don't know the specific numbers you will need to input until, you actually measure them.

I think they are also like the english "So and so" for an unknown person,
or "Such and such" for and unknown thing, which someone might use when making aan abstract,
general statement that isn't about any particular person, but *is* about people in general.

They are often a single letter, but can also be words or symbols.


### Programming

Variables in math are not the same as variables in
programming.   In math, X=70 is a statement that the two are equal,
in most programming languages, X=70 is a command to store the number 70
in the container called X, which can later be overwritten with something else.

They are often not really similar to inputs and outputs, but closer to scratchpads
when you can store things.    In addition, in some languages, they don't truly represent
storage locations at all, and are actually labels you can attach to objects, which can have 
multiple labels, to "be stored in different places at the same time".

Pure functional languages have a concept of variables that is much closer
to the mathematical meaning.

### Graphs

When graphing something, the Y or vertical position is usually the dependant variable,
because we are studying how it goes up and down as we move from left to right(The horizontal position is usually called Y, 
and is usually the independent variable, because it's doing it's own thing, we increase it evenly as we go across the chart to see what happens).

Often the independent variable is time, and the vertical axis represents how something changes over time.

There are all sorts of other charts that may use different meanings for each axis, this is just a very common convention.


## [Linear](https://en.wikipedia.org/wiki/Linear_function_(calculus)) and Nonlinear functions

This will come up a whole lot.  For any function that takes a number as
an input and returns another number, some will be linear, and others will not.

Linear functions make a straight line if you graph the input vs the output.
Linear functions behave similarly at any scale, the same size input step makes the same size output step, no matter what the value was.When dealing with a nonlinear function, you might find:

* Audio distrotion. Linear functions won't add new frequencies to sound.  Crunchy electric guitar like stuff is nonlinear.

* Thresholds.  Stuff won't behave the same at different power levels, file sizes, or whatever.  Even with no literal sharp cliff like threshold, in practice there may be obvious points where things act different.
* Some nonlinear functions will have huge changes for small steps past a certain point.
* Diminishing returns.  Some nonlinear functions will take more and more input for the same amount of output change.

When dealing with linear functions in things you can directly perceive, like light, it probably won't
look linear, because eyes and ears don't have a linear response.  Brightness generally has a diminishing returns type curve, it
takes more power to look twice as bright the higher you go.

There is usually no way to stack different linear functions with addition to get something nonlinear. This is related to the fact
that no combination of resistors will introduce nonlinearity(In theory, real resistors do wierd stuff with tempeature changes).


## Multiplicaton

## Linearity

A constant times X makes a linear graph.  X times X is the same as X\*\*2, which is most 
definitely not linear.

### Rectangles
Multiplying the lengths of the sides of something gives the square area.  4ft\* 8ft= 32 square feet.  1ft\* ft=1 square foot.

#### Algorithm Complexity 
This also means that any algorithm like "Do something with every possible pair of one input from the list A and one from B" will take an amount of time proportional to the length of A times the length of B, since every step in the algorithm is one of the "Square feet" in the "table" where each side has one foot per item on the list.

If A and B are the same, then the area will be A squared, and this is fairly common in programs. If you see this pattern, maybe try to do something about it, because it will get very slow.

Example: You have 100 items, and you want to display a statistic like "This is more expensive than 99% of items".  If you loop over every one, and compare it to all the others, you will do 100 * 99 comparisions.

Instead, you could pass the full list to a proper sorting algorithm(Which uses code I don't understand to sort things much faster than comparing every element to every other), and simply look at how high up everything is on the list.  The second item costs more than 1% of items and less than 98%.

### Scaling

It can also make things bigger or smaller. x *\ 0.5 is half of something, x \* 2 is twice that thing.  Because it is linear, 
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

Multiplying by 1/x  is the same as dividing by x.  Multiplying by x will "undo" dividing by x, and give you
the original number back, and vice versa, dividing can "undo" multiplication by the same number.

But division by a variable does not produce a linear plot.

12 divided by 6 is 2.  12/3 is 4.   When we have half the divisor,
we get double the output. It seems like this should result in a linear chart,
to someone (like me!). without a real understanding of math.

But if one plots 1/x on a graph, the result is not linear.  I don't actually
know why.  It is important because there is no way to implement division
by an arbitrary value with just multiplication, although you can implement division by
one specific value by multiplying.

This is important because many very small cheap chips don't
have hardware division, and multiplication is much faster, so
you may want to watch out for equations involving dividing by a number
that can change.

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

The reason this makes no sense is pretty simple.  Normally, when you divide by a number, you can multiply it by
the same number to get the original. But there is no standard real number than, when multiplied by zero,
gives something other than zero. Multiplying by zero is like an "off switch" that doesn't let anything through.

Clearly, if division by zero had a defined result, it can't be a regular number, and still work in
the way we might expect division to work.


## Exponentiation 

2\*\*5 means "Two times itself five times, or 2\*2\*2\2\*2". It is also said as
"Two raised to the power of five" or "to the fifth power" or similar.

It is sometimes also written as 2^5, but that symbol is also used for other things occasionally, in programming,
so I will use Python's notation, with two stars.

Numbers which can be written as 2\*\*something are powers of two, the first few of which are:
1, 2, 4, 8, 16, 32, 64, 128, 256, 512,1024, 2048, 4096, 8192

These numbers are extremely common when dealing with computers, and numbers that are
two to some other power of two(2\*\*8=256, 2\*\*4=16, etc) are especially common.

The number of possible combination of N binary bits is 2\*\*N.

### Squaring

X\*\*2 is Squaring, as mentioned before, and it gives you the
area of a square, if X is the length of the sides.

To go backwards, and get length from an area, one would use a square root.

x\*\*3 is cubing.  It gives you the volume of a cube given the length of it's edge.


### X\*\*1
Anything to the one, is itself. Five times itself one time, is just 5.

### X**0

Any number raised to the power of 0, is 1, except possibly zero in some cases(see below!)

I am sure there's a cool math reason for this, but it
also happens to be really convienent in programming.


### 0**0

I have no idea what is going on here.  Android calculator thinks it
is "Undefined, or 1”.  That probably means you shouldn't rely
on it to do something sane in programming languages if you don't specificaly check the spec.
 
Xonsh/Python however, just says 1, so your milage may vary on that one.

I have never seen this in real life, or thought of it before just now, and it doesn't seem to really make any sense.
But it is good to know that it 

### Non integer powers

You can raise something to the power of 1.5, just like you can raise it to 2 or 3 or any other integer! But keep in mind, the result will not be halfway between x\*\*1 and
x\*\*2.  If it were, it would not make the same nice continous curve the exponential functions make.

In reality, raising to any number is just as valid as raising to an integer, the only difference as far as I know,is that integers can be explained as "X times itself Y times", but there is probably some deeper mathematical phenomena underlying it all which explains the values in between more completely.

The oversimplified explanation however, is that the values in between follow the same curve you would expect them to, from looking at the integer powers, rather than following a "curve" made of straight lines between integer points.

## Logarithms

The log of a number x, in a given base, is the number you would need to raise the base to the power of, in order to get x.

If y=log10(x), than x=10\*\*y.

Logs are always in a base, usually logn, the natural logarithm, using
the mathematical constant e, log10, or log2.

They are distinct from square or cubic roots, in that a square root
asks "What number, when raised to the two, gives me X", wheras a base 2 logarithm
asks "What number would I have to raise 2 to, to give X".

If you're raising X to the Y, a log finds Y, but a root finds X.


### Use in implementing multiplication

A slide rule is a calculator that amounts to two rulers, that slide.

It's easy to see how you could make an adder this way, but not obvious how one
would multiply.

Logarithms have the neat property that the log of a\*b, is the same as the log of b plus the log of a.

Essentially, if one has a table of logarithms, and "antilogarithm" to convert back,
one can multiply by looking up the numbers in the table, adding, and converting back.


Obviously, nobody really does this anymore, but the property is still a very important
fundamental thing that finds use elsewhere. In fact, there are still computers
that can add much faster than they can multiply.

### Count the Zeros!

Adding a zero to a decimal integer multiplies by ten, log10(10) is 1
log10(100) is 2, etc.

1,10, 100, etc, are known as the "powers of ten" just like
1,2,4,8 are the powers of two.

### Complexity theory

Some advanced algorithms are known to only get slower with the log of the input.

People like these, because as we can see in the zero counting argument, the slowdown eventually
levels off, as it takes a lot of points added on to add a single zero to
a very large number.  Think of how much you have to add to 1000000000 to get 10000000000. 

It is a lot!


These are actually better than linear time, which means they probably don't
do something to every input, and instead skip some.  Of we did something
with every input, unless there's a large overhead, we would usually
expect twice the input data to take twice as long to handle.

More commonly, you see things that scale with N log N, or N times the logarithm of N.
Not sure why that seems to show up so much.

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

Sine waves also have something I don't understand to to with circles and trigonometry.

### Sampling

If you are taking digital samples of a signal, and you sample slower
than twice the frequency of the highest sine wave, you get aliasing,
which causes the familiar illusion where helicopter blades go backwards,
and which can make a sawblade under fluorescent light stand still.

If you always sample at the very top of the wave, it will look like you have an 
unchanging signal.

Aliasing will usually create an illusory sine wave for every input wave above the cutoff,
 at some related frequency.

### Harmonics

The familiar square, triangle, sawtooth, etc waves that repeat, but are not sine waves, are made
up of a sine at the "main" frequency, and a set of sines at multiples of it.

Creating a perfectly sharp square requires infinite waves, which is
why perfectly sharp waves aren't usually a thing in real life.

When distortion distorts a sine wave, the additional new tones are usually at multiples
of the frequency.  This is not true of aliasing, which makes sines at "reflected" points.

This is why aliasing sounds harsh and unmusical.

## Area and volume

These are measured in square units and cubic units, respectively.  A square inch is teh area of a square that
is one inch on each side, and a cubic inch is the volume of a cube that is one inch on all sides.

You can use any unit, but note that a cubic foot is not 12 cubic inches, but 12\*12\*12=1728 cubic inches, because squaring and cubing
are nonlinear.  Area and volume increase faster than you might thing when you increase the lengths of the sides.


When you extrude a 2D shape out into 3D space, like as if you pressed Play-doh throuh a shaped nozzle, the of the resulting object volume is the area, in square units, times the length you extruded it.

A cylinder is pretty much an extruded circle(math people may use a different word than "extruded"), so one can get it's volume by the length times the circle's area.


## Coordinate Systems

There are many ways to specifiy the position of something, but it is common to
to describe the position of a point in terms of XYZ coordinates,three numbers
representing a position along each of the three dimensions of space
that most people are familiar with. 

On a computer screen, 
X is quite the distance left to right, starting at the far left.

Y is the top to bottom position, starting at the top of the screen.

Z is the distance away from the viewer.


These may be different in some cases.  In 3D printing, Z is
the top to bottom depth.  But they are always 3 perpendicular 
axes.

In graph charts, X0, Y0 may be in the very center, and negative
numbers are used for points below or to the left of the center.

## Pi / π
Pi is a mathematical constant, approxiamtely 3.14159265359, which is the ratio of a circle's circumference to it's diameter. It is often represented as π.

If you measure a circle across it's area, and multiply by pi, you get the round trip distance if you walked along it back to where you started.

Pi is irrational, meaning there are no two integers you can divide to exactly produce it. It also goes on forever, you can never calculate the exact value of pi, although supercomputes know it to trillions of digits of precision.

There is no obvious repeating patttern in the digits either, it is said that all of Shakespeare's work is hidden somewhere, along with digital data of every image in every format, and any other data you can imagine.


### Areas and Volumes

Pi times the radius squared, or `pi*(r\*\*2)` gives the area of a circle, in square units. If you give the radius in millimeters, you get square millimeters, if inches, you get square inches.

The volume of a sphere is defined by `volume = (4/3) \* (pi * radius \*\* 3)`, and the surface area by`surface = 4 \* pi \* radian \*\*2`.
I'm not sure what the explanation for those is, but they are well known and easy to find online.




## Pythagorean Theorem
This tells you how long the long side of a triangle right triangle (One that has a 90 degree corner in it) is, given the other two sides. c is the long side, the other two
are a and b, and they are always defined by:
a\*\*2 + b\*\*2 =  c\*\*2

In other words, square each of the two sides, then add them, then take the
square root of the whole thing, and you'll get the missing side.

There are a whole bunch of proofs of this, which I am told are very beautiful to
those who understand them.

Note that the long side will never be one of the two sides that touches the 90 degree corner. 
We can see this because the triangle is half a rectangle, and the diagonal of a rectangle is 
longer than any of the sides.

Also note that there will only be one 90 degree corner. Since there are only three points, if you had two such corners,
they would be connected, and form a 180 degree turn, or two paralell lines, which would not meet and form a triangle,
unless you are using some bizzare non-euclidean geometry, but if you are using that in real life, you are probably a math expert already,
or a Cthulhu spawn.

I believe the correct name for the long side is actually the "hypotenuse".


### Distance between points

If you have two points, and you go "across" then "down"
to get from one to another, you get an L shape.  You can find
the lengths of the lines just by subtracting the X and Y positions.

If you add another line directly between the points, 
you get a triangle, and you can find the length of that line
the same as any other triangle.

### Distance between three points

For reasons I don't understand, you can extend this to three
dimensions.  

Take all the individual dimensions differences, X, Y, and Z, representing the
horizontal, vertical, and front-to-back position,
and square each one.  Add them all and square root them, and you get the 3D
distance.



## Geometry in mechanical design

Geometry is rather often used when building things, but in this case, 
even less knowledge of math is required now that there are programs like FreeCAD
which allow you to directly enter constraints like "These two lines must be at this angle",
and will solve everything for you in real time.

I am told this is not sufficient in real large buildings with a chance of falling over of you get 
it wrong, and real engineers do, or at least should do, some level
of manual verification, probaby largely as an additional check, solving the problem
in unrelated ways to find any errors in the reasoning.

But for the home 3D printer, this is, again, the computer's job.

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

It allows one to work backwards, and find questions given the answer.

Arithmetic will be enough to answer things like X=5*2, but
algebra allows one to work backwards, and find the value of
X in equations like "10=  X*2", which asks "What number do you
have to multiply by 2 to get 5"

It also allows you to solver problems that are defined by multiple equations.

Suppose you have 10 feet of wood to build a 16:9 frame.

X and Y are the final horizontal and vertical dimensions.

You know that X/Y=16/9,  because that's the ratio you want.

you know that X+Y is 10 feet, if we just ignore concerns about inner
outer size for now.

Now you have 2 "simultaneous equations" that can be solved to find X and Y.

Normally, people who are actually learning this stuff start
with single equations, and don't progress to simultaneous equations till later.

But when telling a computer to solve it for you, it's all trivially easy anyway. 
Again, like arithmetic, for the purposes of getting by without knowing how it works,
solving and rearranging equations is a job for totally free programs like XCas.

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


To quote Reddit's `r/BeagleInTheSnow`, who helpfully took a look at this draft:

 Life is full of changes and a great number of them can be quantified. Down to the weather outside - Imagine it's sunny in the morning, but a stormfront rolls in by afternoon and the temperature falls considerably. 
 
 when you say "boy, it sure cooled off quickly!" you've actually unlocked a key intuition of calculus! That being, calculus can describe how one attribute of a system (say, temperature) changes with respect to some other attribute (say, time).
 
 In fact, in technical terms, you've described the rate of change of temperature with respect to time: dT°/dt. The key word is "quickly" - loosely speaking, "quickly" is the rate of change of the system - this is a derivative. 
 
 In the real world, it is used to describe how physical systems change (generally over time). This can be used to model the number of predator/prey in an ecosystem, the performance of stocks, the temperature and weather, the speed of your car... among many other things.


## Prime Numbers

According to wikipedia:
  A prime number (or a prime) is a natural number greater than 1 that is not a product of two smaller natural numbers.  

Which is an odd way to describe it, I've always heard it stated as "A number that can't be evenly divided by anything except itself, and one"

Two, despite being even, is a prime.  All other even numbers are "composite", meaning not prime. Even numbers can be divided by two, so the other even numbers have themselves, one, and two as divisors, totalling three.

There are an infinite number of prime numbers.

### Is one a prime?
It really seems like it should be, and in history, has been treated as one.  However, if you treat one as prime, a lot of other theorems
don't make sense or have to be reworded, so the generally accepted definition excludes one.  

Depending on your view of the philosophy, Both the set of all primes, and the set of all primes, plus one "exist" regardless of what we call them, but choosing to exclude one for what we know as primes makes a lot of things neater and more elegant, which mathematicians love.

### Fundamental Theorem of arithmetic

From Wikipedia:

   The fundamental theorem of arithmetic states that every integer greater than 1 is either a prime number, or can be represented as the product of prime numbers and that, moreover, this representation is unique, aside from other combinations of the order of the factors.

In other words, you can make any integer by multiplying primes, but for any given number, there is only one way to do so.

### Product of two primes

This implies that if you multiply two primes, the resulting number cannot be made with any other two primes, as those two
are the unique representation.

There is no known easy way to go backwards, and find the original primes, once the numbers get large enough, although quantum computing could do so. This property is used in cryptography.

### First few primes
2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31, 37, 41, 43, 47, 53, 59, 61, 67, 71, 73, 79, 83, 89, 97, 101, 103, 107, 109, 113, 127, 131, 137, 139, 149, 151, 157, 163, 167, 173, 179, 181, 191, 193, 197, 199, 211, 223, 227, 229, 233, 239, 241, 251, 257, 263, 269, 271


## Highly composite numbers

A highly composite number is a positive integer with more divisors than any smaller positive integer.  They are essentially the "opposite"
of primes, and as such are extremely useful, but little known. The number 360, which is chosen as the number of degrees in a circle, is one such number, and it can be evenly divided by: 1, 2, 3, 4, 5, 6, 8, 9, 10, 12, 15, 18, 20, 24, 30, 36, 40, 45, 60, 72, 90, 120, 180, and 360

This is very convenient, as it gives us nice round numbers for many different angles, including very common ones like 180, 90, and 45.

### List of the first few
1, 2, 4, 6, 12, 24, 36, 48, 60, 120, 180, 240, 360, 720, 840, 1260, 1680, 2520, 5040, 7560, 10080, 15120, 20160, 25200, 27720, 45360, 50400, 55440, 83160, 110880, 166320, 221760, 277200, 332640, 498960, 554400, 665280, 720720, 1081080, 1441440

### Superior highly composite number
According to wikipedia:

   In mathematics, a superior highly composite number is a natural number which has more divisors than any other number scaled relative to some positive power of the number itself. It is a stronger restriction than that of a highly composite number, which is defined as having more divisors than any smaller positive integer.
   
But to most of us, it means "They REALLY have a lot of divisors. The first 15 superior highly composite numbers, 2, 6, 12, 60, 120, 360, 2520, 5040, 55440, 720720, 1441440, 4324320, 21621600, 367567200, 6983776800.  They get big in a real hurry, but the enduring popularity of 12(a dozen!), 60(A minute!), and 360(a circle!) may have something to do with this property.  I'm sure you can think of even more examples of these numbers in use.





### Fermat's Last Theorem

The theorem itself might not seem interesting to you, but the amount of human drama and deep passion that came from it definitely makes it
worth including in any overview of mathematics.

   In number theory, Fermat's Last Theorem (sometimes called Fermat's conjecture, especially in older texts) states that no three positive integers a, b, and c satisfy the equation a\*\*n + b\*\*n = c\*\*n for any integer value of n greater than 2

This probably has very little practical use to most, but the history is so interesting that it can be appreciated even if you
have no clue what the math means, like I sure don't.

It was proposed around 1637, and remained unsolved for hundreds of years.  Fermat himself supposedly wrote a note in the margin that he had a proof, however nobody knows for sure, and if it is true, if it was a joke or not.

It was finally proved by English mathematician Andrew Wiles around 1993, working in largely secret, possibly to avoid ridicule for trying such an ambitiuos thing.

People worked for a *long* time on this, and I think it's a wonderful example of just how deep the rabbit hole goes, and how dedicated to
their work a mathematician is.  In the end, his proof was around 100 pages long, and understood by only a handful.

I think Wile's himself expresses the feeling best:

   "Some mathematics problems look simple, and you try them for a year or so, and then you try them for a hundred years, and it turns out that they're extremely hard to solve. There's no reason why these problems shouldn't be easy, and yet they turn out to be extremely intricate. [Fermat's] Last Theorem is the most beautiful example of this."

   "I carried this problem around in my head basically the whole time. I would wake up with it first thing in the morning, I would be thinking about it all day, and I would be thinking about it when I went to sleep. Without distraction I would have the same thing going round and round in my mind."



