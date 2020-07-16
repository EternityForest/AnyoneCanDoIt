# AnyoneCanDoIt
An open source guide to mistake-resistant engineering(Work in progress)


A lot of planning these days includes the word "carefully".

What does it mean? Well, it means you don't get distracted and do the wrong thing. Your hands don't shake and you don't forget anything.

In essence, it means "this task requires a high level of skill, possible talents that not everyone can learn, and you're the one who's gotta do it, sucker!".

As everyone who's ever broken anything knows, this is unscientific at best and terrible planning at worst.

Instead of just relying on our own ability, let's think of some ways we can stop these failures before they happen!



This is a fairly extreme set of principles. They likely will not
apply to every situation, and they are heavily focused on electronics and software (Though some are applicable elsewhere).

Nonetheless, I believe they may be useful in spotting likely issues with a plan.


### Redundancy.

There should not be anywhere in your plan where a single failure can have significant consequences.  One broken rope, one person dropping something, or one lost flashlight shouldn't affect the plan at all.

Two is one and one is none, not just with things, but with actions.  If the plan starts with "It's basically impossible, but I know one guy who can do it by hand for a good price" you might want a different plan.


### Storage and Organization

It's essentially *always* worth the money to buy a case for your phone. If you're gonna buy something that needs an extra adapter, buy one that doesn't if you can.  Use Bluetooth headphones instead of corded ones.

Get a labelmaker. Don't carry anything heavy without a dolly. Use padding to protect anything expensive. Physical objects are a common source of failure, so the accessories we use to manage them, and the upgrades that make them easier to manage, are worth it.

### Force and precision, pick one

Never design anything with the words "Firmly but carefully" in it.  Hands and tools slip under force. If force is needed, you should be able to use a hammer, or you should use a better design.

Stay away from all screws aside from Torx heads. Phillips requires pressing and turning at the same time. No more of that!

Especially avoid anything involving "carefully prying". Nobody wants that.


### Minimum Energy

Don't use dynamite. Or rat poison. Or High voltages, or big strong springs, or giant hydraulics, or anything else with real power behind it, unless you actually need it.

"Safety" should not be the goal. What you want is *harmlessness*.

You don't want a plan that *won't* hurt anyone. You want a plan that *cannot* hurt anyone, because there is no part that has the capability to do so.

If you need a training video to explain how not to hurt yourself, look at eliminating that step entirely.

### Minimum Material

You are trying to make excellent products. Not use up excellent materials.  Every ounce of matter, be it steel or gold, is a waste.

When someone says "Solid gold" they mean "I probably polluted an entire village somewhere because I didn't have any better ideas"

This applies to non-physical "Material" too, like lines of code.  Anything you have to buy, carry, maintain, etc, is a liability.

Go with things that are cheap, common, and inert.


### Don't trust Elegance

Scientists and engineers LOVE simple, short, expressions of some deeper truth, that cuts right to the essence of what it means to be a pencil or a knife or a razor or something.

They also love to wonder why consumer products aren't built like this anymore.   To everyone else, it's obvious.

Non-engineers are trying to sign a check, not marvel at your skill.  The rest of us will be bored long before we ever have a clue why you did what you did.

And more than that, simplicity usually just moves the complexity elsewhere, namely, to the user. It's another word for "manual".

Elegance is a design constraint that doesn't accomplish much.  It results in parts that perform multiple functions at different times, things that loop back on each other so that everything affects every other part, and nobody will have a clue what you're doing.

It's also generally ugly and delicate, because the aesthetic parts, the function parts, and the protective parts are one and the same.  

Many argue that it's just the price of fine craftsmanship, that an old 1800s writing desk was not meant to be set drinks on, but accepting that principle means putting the responsibility back on the people, rather than preventing failure at the design stage.


### No Guessing

You should never have to adjust something you can't immediately see the results of, while you're doing it.  Aside from aesthetics, you mostly shouldn't have anything that needs "adjusting" in the first place.

There shouldn't be too many tweakable parameters you have to get "just right" to make it work.  Those always result in something getting out of calibration over time, and the whole thing goes down for a week while you wait for the guy who knows how to fix it again.

If there is something that needs adjusting (Usually something that directly affects people, like light levels), it should be controlled in real time, with a knob or a slider. No "Reboot and change a config file" or any such nonsese.

In general, things should adjust themselves. Every adjustment the user makes is usually a failure the designer made.

This also applies to pretty much any kind of configuration or setup. Things should just work, and you shouldn't need to tweak them or use a different version for every possible situation.


### Too Many Tools 

Avoid having two similar tools for slightly different applications if you can. They can almost always be merged, unless the task is so large that modifying them takes too much time.

Especially avoid creating a new tool to avoid learning an industry standard that you know you will have to learn anyway.

### No Mental rotation

Just throw the idea in the bin right then and there if it involves accurately imagining something rotated or flipped.  

Things like reading maps not oriented towards the real directions, manually flipping things for printing on two sides of a page, etc, should be treated with extreme care.

### No arbitrary mappings and remappings

If you're plan has something like "Oh yeah A fits into C" or "Just press Ctl-N" or "A is also called 1 in some places", you need to document every step, or avoid the whole plan.  Nobody should have to memorize nonstandard arbitrary codes.


### No Duplicated information or entry

No reporting the same information to different sets of people at different times.  No giving employees multiple ID numbers that apply in different contexts.

No manual bookkeeping that relies on someone updating one document to stay in sync with another.  This should either be automated, one person should be dedicated to this, or the whole plan should be scrapped.

The only time a user should do the same thing twice is as a confirmation. Redundancy should be part of the automated process, not something you do yourself.   

Requiring a user to reliably do the same action more times than needed is not redundancy, it is just multiplying the single points of failure, unless there is tolerance for some of them to be erroneous.

A user should not deal with both the processed and unprocessed version of information.

Avoid anything like common credit card receipts, where one has to write both the tip amount and the total, as the total can be calculated from other information and there is no need for a person to do so.

Most such cases that use the extra manual calculation step as  a confirmation can be replaced by an automatic calculation, and an explicit confirmation prompt.



### Do not be confident, and don't trust someone because they're better than you.

This is neither a football field, nor a chess club, nor a Eugenics festival.

It is not an engineer's job to worship anyone's superior body or brain.

An engineers job is to use careful analysis and the latest tech to achieve results above and beyond the limitations of the body and mind, for the good of all.

Someone who takes great pride in being smarter than you likely does not understand this.

And when it's true, it can be even worse, as they may not even notice how incomprehensible their designs are, causing everyone around them to make mistakes.

### Respect the "blue collar workers"

No matter how long your day was at the office, I am quite sure the team that had to install whatever garbage you're building was far longer.

If they tell you something, believe it.

Sometimes non-technical people have some unscientific ideas and think things are "Too cheap and plasticity" or "not powerful enough" or something, but even then, they probably have at least one legitimate complaint, and ten more they aren't even telling you.

The ones who actually use these systems in real life know a lot more than the ones who design them from behind a desk.

### Use what you have, buy what you need

While helping a friend move, someone once repeatedly tried to convince me to carry various things like couches and bookcases by hand, across level ground, with a perfectly good dolly sitting idle.

Their reasoning? "It's Faster!".

Speed and flexibility is quite often used as a rationale for doing things the hard way.

Unless you enjoy being sore at the end of the day, I see little reason to not use perfectly good existing things, rather than do more work yourself.

Everything you do can fail. Things that happened in the past and already exist are the closest thing to truly predictable we have.


### Don't throw stuff away

Throwing things away is selling them, and being paid in empty space. If you don't need the empty space, you're just wasting things.


### There is no later

Avoid any plan that involves a person remembering "When X, do Y" or "In 30 minutes, check on the pot".

Especially avoid anything that requires regular recurring maintenance.   The cheapest plastic may last 500 years, while steel used in the same place may be total rusted when left alone.

Choose plans that are independent of any human action, and especially independent of any *specific* person.


The best way to predict the future is to create it yourself. As people's future state cannot be effectively predicted, anything dealing with the future should be left to machine.

### Tests don't predict the future

Things are not guaranteed to behave as they did in testing in all cases. 

If it works in a test, but theory says it will fail, watch out.

### Avoid hidden state

Hidden state is anything that has a variable condition, such as a door that can be open or closed, but which does not make that state visible, or makes it insufficiently visible.


Appliances that get hot should have power lights.  Just as you shouldn't trust a person to do something later, you shouldn't trust a person to check on something later.

There should not be any "Do X, then check Y" steps. X should obviously and instantly fail if Y is in the wrong state.

Ideally, all things should return to a default safe state if left unattended.


### No Ordering dependancies

Avoid manual processes with steps that must be done in a particular order. This is a common type of error that can be eliminated in the design stage.


### Explicit Not Implicit

Where possible, avoid expecting anyone to manually determine unknown information, even when it is fully specific by present information.

Examples include inches to feet conversion, or manually finding the center of a marked circle to drill a hole.

### Watch for highly transported objects

An objects is unlikely to be lost if it stays in one place.  When a cheap object such as a pen or pair of scissors is used in two locations, it is likely far better to duplicate the item rather than transport it.

Transported objects create an element of both variable state and a dynamic time region while it is in transit.

”Kits" for accomplishing an activity are valuable enough to warrant even large amounts of duplication.

### Atomic Time regions

An atomic time region is the period between beginning an activity and completing it, when the activity cannot be abandon during the region.

A section of fast moving traffic is one such example.  There is neither a way to exit at an arbitrary point, nor any inherent stability that would return things to a safe state were the driver to stop paying attention.

Another example is the time between taking an item out of a pocket to use it, and returning it, during which it can be lost.

These regions should be minimized, and things should be designed such that things can be paused or stopped at arbitrary points without consequence.


### Captive Objects


Things not meant to separate should not be able to easily, or should at least be able to stick together by themselves.

None of this "Hold these three parts in place while you Insert rod X" busisness.

Valuable items such as keys and wallets can be tethred to the inside of pockets using carabineers and grommets.   Pens can be affixed to clipboards.

Where periodic separation is required, a slipped knot, highwayman's hitch, or mechanical device should be used, but only one that requires definitive action to separate. 

A tether that can become undone simply through tension is not secure, and magnetic attachment should not be used for things exposed to arbitrary unknown force, such as portable or handheld objects.


### Watch for Reversibility

Any step that cannot easily be reversed should be avoided or given extreme caution, and an acceptable decision that can be undone may be preferable to an excellent decision that cannot.

As situations change, fixed elements add extra challenge to keep up with, but fixed elements can often be avoided through planning and engineering.

In particular, never do something in hardware that can be done digitally, unless it is safety critical and studies have shown hardware failsafes to be needed.

Don't write things in stone or make your mark that lasts forever.   Almost nothing people do is perfect, so be sure that your plans can be erased without a trace when something better comes along.

### Project to Process transitions

Projects are easy.  They have a beginning, an end, and the only goal is to finish them without seriously wrecking something.

Processes are hard.  When someone starts saying it's the journey, not the destination, suddenly you now have more than one goal, in fact, you have hundreds, because every action
must be done not only successfully, but neatly and gracefully, with a smile and good posture.


The easiest way to avoid these, is to do things in advance so that they can be done as a project, rather than live under pressure as part of a process.


### The Dreaded Chopstick

Absolutely reject any design that involves bending some part in, wedging it at an odd angle, and possibly pushing something out of the way with  chopstick.

Hands and tools should never go where eyes cannot, nor should there be any step where the act of closing a box can easily affect the (Now non-inspectable) contents 

### Eschew the Screw, careful how you connect

Screw-based connectors are often incredibly inconvenient to work with in-place, although they may seem very convenient for use in the lab.

When using terminal blocks, avoid non-detachable versions, and air hose quick connects are usually worth it.

Generally, connection points are very common failure modes.   All connectors should have a large strain relief if you want them to last, unlike a the popular slim white style USB connectors that imitate "luxury" brands.

Keychain carabineers and clips are similar danger points, as is the wrong knot in a rope.

Remember, connection can fail by coming undone, staying stuck, putting force on something else that breaks, and in sealed devices, by leaking.

Electrical contacts have all sorts of additional failure modes.

Pay attention to connection points!

### Relative Motion?

When two things must stay fixed relative to each other, they should not have a long elaborate series of connections and objects in between them.

### No Remapping By Swapping

A relatively common problem is something like this.  You have a box with four coloured pipes going out, and four blank ones going in.


You need to figure out which pipe to drop each colored ball in to make it come out the right pipe.

If there is already a listing of which pipes to use, but it is incorrect, people will often try to fix it by swapping incorrect ones.  When more than two are wrong, this seems to rarely work.

Instead, make a map of every input and the corresponding output (Giving them all labels that have nothing to do with what specific balls you put in!), and trace outputs back to inputs on the map.


### Look for potential problems


A lot of people will analyze a plan or situation by looking for active problems. The things that are wrong with the plan itself, that are guaranteed to cause problems.

This is important, but more equally important is to look for points where a mistake is likely, or where the consequences are large.


A wet floor is not an immediate problem until someone slips on it.  It would be easy for someone who is used to assuming perfect competence to conclude that people should see it and not slip.


Removing contributing factors is often easier then directly avoiding problems for several reasons.

One is that you cannot always be sure of the future, or what additional circumstances will complicate your plan to avoid the mistake.

Another is that, like the wet floor, "Being careful" must often be done continually, in this case each and every time, whereas removing the contributing factor often only needs to be done one time(as in mopping the water), and will persistently make things safer until something causes the factor to return.

