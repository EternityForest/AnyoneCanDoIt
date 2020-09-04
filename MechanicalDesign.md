# Intro

This file contains info for people who aren't mechanical
engineers, who build things.  If your thing could kill
someone if it goes wrong, get a real mechanical engineer!


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


Some bearings are so ridgid that only two creates an overconstaint. 


Now add a third bearing in the middle.  The rod is already totally constrained from
pointing different ways, and the extra bearing is redundant.

You might have trouble even getting the rod through three fixed bearings.


Once you get it through, even if misalignment tolerate bearings are used, if the
center one is out of line with the others for any reason, you have a problem.

Again, in practice this works fine, because the assembly is either precise, or so wobbly it doesn't need to be.


### Peg in a hole

If the peg is tight, by itself this is an overconstaint, with it's characteristic need
for precision, or wobbly materials.

If the peg is loose, however, it will not constrain in all directions, as the peg only touches one side of the hole.

This means at any given time, it still has play in directions other that towards the side of the hole it's on.

If it's in the middle, it's not constrained at all.


This shows how constraints can exist or not exist at different times in the same assembly.


### Compliance and adjustability

Constraints like things held in place by springs, foam, rubber
pads, etc, don't "participate in fights" like ridgid constraints to.

If a direction of movement doesn't actually need to be precisely constrained, there are many ways to stop it from rattling
without actually constraining it, and requiring precision.

### Squeaky floors!

Subfloors can separate from floor joists over time(Possibly from warping involving some other overconstaint),
and squeak as nails slide.

clearly there is some kind of overconstraint happening, or the subfloor
would perfectly rest on the joists.  However,the subfloor is a solid board,
and the joists are meant to support it along the whole entire length,
so there are effectively infinite constraints points all competing to by the high spot
it actually rests on.

A little warp, and, you've got a gap, and a squeak can live there!


### Sealing

Trying to seal something is an example of overconstraint, as you need the whole surface of the seal to be touching.

This is why o rings are used, to take up the gaps that show up anyway if you don't get everything micrometer-perfect, or someone accidentally makes a tiny scratch.
