# Intro

This file contains info for people who aren't mechanical
engineers, who build things.  If your thing could kill
someone if it goes wrong, get a real mechanical engineer!


## Covering Up

There is one main way I know of, to build things that look decent,
without an incredible amount of skill.  Even a simple wooden box can be much harder than it looks.

The essential way of making things, if you don't have rock-steady hands,
is to separate the structure and the visible part.

Most of these methods rely on choosing an aesthetic that does not require extreme
precision.  This causes a bit of conflict, because modernist design aims to hide nothing, 
and show off your skill, precision, and spotlessness.

However, no matter the fashion, a design that hides nothing will look bad if there are any
imperfections.

Moreover, even one tiny flaw will be incredibly visible against a near perfect backdrop.



### Fabric

As a textured material with a bit of randomness, and it's own structure that tends to make curved edges, and cover
unevenness, fabric is incredibly forgiving.  the crappiest workmanship becomes invisible when covered with
even moderately thick or coarse fabric.

### Paper

Paper is also forgiving, in that it is essentially the only material
that is easy to cut precisely, and the fact that it can be printed means that designs
are not limited to what you can draw yourself.  It can be made incredibly strong
with my number of polymer finishes.

Paper mache is mistake-resistant because it can be reshaped and remolded
by trial and error for a long period, and because it's texture tends to hide things.

When mache is done with epoxy, it essentially becomes a strong composite material,
almost like the poor man's fiberglass.

Like fabric, paper can be used to cover things make of other materials,
hiding any imperfections.


### Cordage

Cord wrapping is one of the easiest ways to hide things of all,
and in addition, it provides a fair amount of padding against impact.



### Putty

Various putties and plasters, most of all hot glue because it can
be melting, share the ease of use of paper mache for the same reason.

### Wood

Bare wood does not hide mistakes.  Joints that are not perfectly square
are almost immediately evident.



## Freehand: the clumsy person's bane

Some people can do amazing things with just their hands.

For the rest of us, when we do anything, there should be a
reason and a rationale for why it will work, and that reason should not include us
directly.

Anything that can't be tweaked and adjusted freely should
be done with some sort of guide, transferring the responsibility for precision
from ourselves, to the guide itself.


## Stress Concentration

Whenever you have a sharp corner, tight bend, or transition from
bendy to flexible, that location specificaly, is where breakage will likely happen.

Often this is especially bad because the sharp corner is at the end of something
acting as a long lever.

This effect seems to be the most common way a 3D printed part can fail.

Even knots in a rope weaken it.  

### Solutions

* Keep it from moving
* use something like rubber to create a more gradual bending
* eliminate the sharp corner entirely.


## 3D printed layers

Print orientation matters.  Layers detach from each other with less force
than trying to rip the plastic in a single layer.

## Ridgidity and direction

Flat bars bend up and down (Think of a springy plank a pirate might walk),
much more than side to side.

You can bend sheet metal, but if you roll it into a pipe, 
you can't bend it nearly as easily.

However, if a pipe is crushed, it may bend like a hinge. This is very bad and seems to metal fatigue rather
fast if repeated only a few times.  This effect makes male 0.1" crimp pins some of the
most delicate connectors you can get.

Things need to have some thickness going in the same axis as the load trying not bned them.






## Method of Exact Constraints

This one is pretty important.  Almost everyone has
seen something stick, rattle, be too loose or tight, or otherwise
just not work, and a lot of the time, constraint theory has the answer.


An object has six degrees of freedom. Three ways to move back and forth,
and two ways to turn.  Since we want our stuff not to fall apart,
we attach things together in various ways, that allow various kinds of movement.


The study of these attachments, joints, hinges, etc, is constraint theory.



### Overconstaint

Whenever you have redundant constraints, you often have to be careful.

Thing of a three legged table.  Combined with the "nesting force" of gravity,
this is exactly constrained in all directions, except picking it up, or sliding it.

There is no way for it to wobble(Ok, someone probably invented a way by now, with springs or something).

Now consider the four legged table, which I am sure you have seen wobble.

A constraint has been added, yet it is less stable.

This is because redundant constraints, trying to achieve the same thing, do not agree.

Imagine we only had legs on one side of a table.  It is free to move like a hinge, and so will fall down and make a ramp.


Not what we want.  But when we add two legs, *both* of those legs are trying to prevent that movement.

If they do not agree perfectly on how, you get a wobble.

### Elasticity

In real life, most non-crappy tables don't do this.  One reason is that the legs
are usually at the edges, and the table can bend slightly, to take up any gaps
causes my very slightly mismatched legs.

However, if someone were to reinforce the taple with some ultra ridgid graphene
plastic or something, they might find it wobbles *more* than it did before.


Constraint theory is so important because it serves as an antidote to the 
slightly dated and worn out idea that good design is lots of strong steel, wood,
and "solidness", which leads people to pile up heavy crap on their designs, for no reason.

You can never make something perfectly strong or rigid, and the more you try,the heavier it gets,
meaning it has more energy to break itself when someone drops it.

What you can do, is to make a little warp or misalignment irrelevant, so that
when someone drops it, things spring back to mostly the original place, and nobody notices a problem at all.

The biggest flaw with many high quality designs is that they need to be high quality.
When they degrade, or the factory messes up, they don't work at all, or things warp and peel and look bad.

### Bearings on a rod

When you have one bearing on a rod, it can rotate, or the rod
itself can even turn slightly to point in different directions, or more than slightly, if misalignment
tolerant bearings are used.

The only thing it really ridgidly constrains is moving the endpoint perpendicular to the rod,
because the rod can't go through the wall of the bearing.


With two bearings on a rod, the other ends is constrained the same way.


We have a little bit of overconstraint here.  They do have to be fairly well lined up,
if regular bearings are used.  But the rod is probably a tiny bit bendy and the bearings
probably have some play, and the world won't end if it's a nanometer off.


Some bearings are so rigid that only two creates an overconstaint. 


Now add a third bearing in the middle.  The rod is already totally constrained from
pointing different ways by the first two bearings,  and the extra bearing is redundant.

You might have trouble even getting the rod through three fixed bearings at all.

Once you do get it through, even if misalignment tolerate bearings are used, if the
center one is out of line with the others for any reason, you have a problem.

Again, in practice this works fine, because the assembly is either precise, or so wobbly it doesn't need to be, but
if this is being made by hand or in small quantities, or will be exposed to forces that might bend things and misalign things,
you might notice some issues.



### Peg in a hole

If the peg is tight, by itself this is an overconstaint, with it's characteristic need
for precision, or wobbly materials and tolerance of inaccuracy.  If things expand and contract, they get jammed or lose precision.

If the peg is loose, however, it will not really constrain in all directions, as the peg only touches one side of the hole.

This means at any given time, it still has play in directions other that towards the side of the hole it's on.

If it's in the middle, it's not constrained at all, as it still has room to move in any direction.


This shows how constraints can exist or not exist at different times in the same assembly.

Instead of a peg in a hole, one might use a peg in a corner, only touching 2 points of the corner, and held there by a spring.
Even if the peg is damaged, of still stays in one spot.

Note that this also applies pretty much any time something fits into something that constrains it from all sides.


I don't know the real techical reason this generates overconstaint, but my best guess would be
that each of the walls has its own idea of where the part should be, and one must either be ignored (a loose fit), or things have
to smash and bend, actually changing each walls "idea of where things should be" to match what's going on.


### Two holes

Often it's taken for granted that accurate pegs and holes can be made good enough,
but what about when we have TWO pegs and holes?

This is quite common when attaching wood together, but usually holes are drilled and screws are driven with everything in place, so alignment is pretty much guaranteed.

Still, this is an example of overconstraint. Both holes constrain the same axes, and were the board to expand and change the distance, A whole lot of force and bending could result.




### Compliance and adjustability

Constraints like things held in place by springs, foam, rubber
pads, etc, don't "participate in fights" like ridgid constraints to.

If a direction of movement doesn't actually need to be precisely constrained, there are many ways to stop it from rattling
without actually constraining it, and requiring precision.

### Squeaky floors!

Subfloors can separate from floor joists over time(Possibly from warping involving some other overconstaint),
and squeak as nails slide.

We the want subfloor to perfectly rest flat on the joists  However,the subfloor is a solid board,
and the joists are meant to support it along the whole entire length,
so there are effectively infinite constraints points all competing to be the "high spots"
it actually rests on.

A little warp, and, you've got a gap, and a squeak can live there!


### Sealing

Trying to seal something is often an example of overconstraint, as you need the whole surface of the seal to be touching, meaning you have a lot of different
points trying to do the same thing.

This is why o rings are used, to take up the gaps that show up anyway if you don't get everything micrometer-perfect, or someone accidentally makes a tiny scratch.


In practice, sealed parts usually work because the parts that actually do the sealin
