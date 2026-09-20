# An annotated modelling dialogue

This is an original fictional conversation inspired by the teaching in
*How to Solve It*, Part I, §20, “A rate problem,” pp. 29–32. It uses a different
problem and is not a transcription or a record of a real tutoring session.
Source: [text of the book](https://studylib.net/doc/27587599/how-to-solve-it---polya).

Read it when a learner is struggling to formulate a problem, identify what
varies, or connect an intermediate relationship to the requested result. The
instructor notes explain the interventions; they are not spoken in the dialogue.
In a real session, ask the next useful question and wait for the actual response.

## Problem and starting knowledge

**Problem:** A point light is mounted 4.5 m above level ground. A person of height
1.8 m walks directly away from the lamp post at 1.2 m/s. How fast is the far tip
of their shadow moving away from the post when the person is 6 m from it?

Use the idealized geometry in which the person is an upright vertical segment
of fixed height. The light ray through their head meets the ground at the shadow
tip. The lamp, person, and shadow are in one vertical plane.

The learner knows similar triangles, algebra, and differentiation with respect
to time. They know that a derivative represents an instantaneous rate, but have
trouble identifying which function and derivative a word problem requires.
Explain any missing prerequisite in a real session rather than assuming this
example's starting knowledge.

## 1. Identify the point and quantity being tracked

**Learner:** The person is moving at 1.2 m/s. Is that also the answer for the
shadow? I don't know what else to calculate.

**Instructor:** Which point is the stated speed about, and which point does
the question ask you to track?

**Learner:** The stated speed is the person's. The question asks about the far
end of the shadow, measured from the post. Those might move differently.

**Instructor:** How could you represent that end's position as time changes?

**Learner:** Let z(t) be its distance from the post, measured along the ground.

**Instructor:** What expression represents how fast that distance is increasing
at a particular moment?

**Learner:** dz/dt. If x(t) is the person's distance from the post, the given
speed is dx/dt = 1.2 m/s, but we want dz/dt.

**Instructor note:** Reformulation connects the physical request to a concept
the learner already knows. The distinction between the two moving points is
necessary before choosing a derivative. A request to differentiate immediately
would leave that modelling decision unresolved.

## 2. Distinguish an instantaneous value from a constant

**Learner:** We know x = 6. Could I replace x with 6 everywhere before I start?

**Instructor:** Does that equality describe the person's position for all time,
or only at the moment we are considering?

**Learner:** Only at that moment. I should write x(t₀) = 6. The function x(t)
still changes, so its derivative there is 1.2, not zero.

**Instructor:** Keep the changing distances as functions while we find their
relationship. Let's also call the two fixed heights H and h, and the person's
speed v, so we can see how they enter the result. Which heights stay fixed as
the person walks?

**Learner:** H = 4.5 m for the light and h = 1.8 m for the person. Those are
fixed. x(t) and z(t) change, and dx/dt = v = 1.2 m/s.

**Instructor note:** The dangerous substitution is freezing a moving quantity
before using a relationship over time. Keeping H and h symbolic is a separate
choice that makes the structure easier to inspect. Substituting their numerical
values early would also be valid. This is not a rule to forbid numbers.

## 3. Introduce an unknown that makes the geometry usable

**Instructor:** What relationship can you see among the distances and heights
in the picture?

**Learner:** There are two right triangles: the big one from the light to the
shadow tip, and the small one from the person's head to that tip. But I don't
know the length of the shadow, so I can't put numbers into the small triangle.

**Instructor:** Can you name that unknown length and describe how it connects
the two ground distances you already named?

**Learner:** Let s(t) be the distance from the person's feet to the tip. Then
z = x + s. The small triangle has height h and base s; the big one has height H
and base z.

**Instructor:** What makes those two triangles similar?

**Learner:** Both have a right angle where the vertical meets the ground, and
they share the angle at the shadow tip. So their corresponding sides are in
proportion: h/s = H/z.

**Instructor note:** Not knowing s numerically does not prevent using it in an
equation. The extra quantity is useful because the geometry supplies another
relationship. The learner also justifies the model through the specified
geometry instead of treating simultaneous changes as sufficient evidence for
a particular formula. Here x > 0, s > 0, and H > h > 0, so the ratios are defined.

## 4. Turn the intermediate relationships into a useful model

**Learner:** Now I have z = x + s and h/s = H/z, but also this extra unknown s.
It feels as though I've made the problem bigger.

**Instructor:** Your target is dz/dt and your given rate is dx/dt. Which pair
of positions would it help to relate directly?

**Learner:** z and x. I could remove s by writing s = z − x. Then

```text
h/(z − x) = H/z
hz = H(z − x)
(H − h)z = Hx
z = [H/(H − h)]x.
```

**Instructor note:** The instructor reconnects the intermediate work to the
original target. The learner chooses the elimination and performs the algebra.
The two equations determine s and z from x; the additional symbol has enabled
a relationship rather than supplied missing physical data by guesswork.

## 5. Choose the operation that connects the model to the target

**Instructor:** You have a relationship between positions. What would turn it
into the relationship between rates that you need?

**Learner:** Differentiate with respect to time. H and h are fixed, so their
ratio is a constant:

```text
dz/dt = [H/(H − h)] dx/dt = [H/(H − h)]v.
```

**Instructor:** Evaluate that expression using the given heights and speed.

**Learner:** The factor is 4.5/(4.5 − 1.8) = 4.5/2.7 = 5/3. Multiplying by
1.2 m/s gives **2 m/s away from the post** for the shadow tip.

**Instructor note:** The operation is motivated by the difference between the
relationship established and the relationship requested. Numerical evaluation
comes after that bridge has been built. The height ratio is dimensionless, so
the result retains the units of the person's speed.

## 6. Check the meaning of the answer

**Learner:** But we never used the 6 m. Have we missed something?

**Instructor:** Does the rate expression depend on the person's current
distance from the post?

**Learner:** No. With fixed heights and this walking speed, the tip moves at
2 m/s wherever the person is along this path. At x = 6 m, the position formula
gives z = 10 m and s = 4 m, but I don't need those positions to find the speed.

**Instructor:** That accounts for the specified instant. The fixed ratio of
positions makes the ratio of speeds fixed in this model.

**Learner:** Is the shadow itself growing at 2 m/s too?

**Instructor:** What relationship distinguishes the shadow's length from the
tip's position measured from the post?

**Learner:** s = z − x. So ds/dt = dz/dt − dx/dt = 2 − 1.2 = 0.8 m/s.
The tip is moving at 2 m/s from the post, while the shadow is lengthening at
0.8 m/s. They are different rates.

**Instructor note:** This check addresses the learner's own concerns about an
unused datum and the interpretation of the answer. The value at the named
instant is consistent with the model, even though the requested rate does not
depend on it. Matching units alone would not distinguish the two speeds;
returning to the definitions of s and z does.

## 7. Look back at the formulation

**Learner:** I thought the hard part would be differentiating, but once we had
z in terms of x, that was easy. How should I recognize what to do next time?

**Instructor:** What did you need to settle before differentiation was useful?

**Learner:** Which position's rate I wanted, which position's rate was given,
and how the positions were connected. Naming the unknown shadow length let me
write the similar-triangle relation. Then I could eliminate it. Also, x = 6
described one moment; it didn't make x constant.

**Instructor:** Those distinctions helped you build the model. In another
problem, look for relationships justified by its definitions or constraints,
then choose an operation that connects what you have to what you need.

**Instructor note:** The reflection identifies reusable decisions. The lesson
does not require every word problem to introduce an extra symbol or use similar
triangles. Introducing s was useful here because it allowed two geometric
relationships to be written and combined.

## Using the example without turning it into a script

- If the learner has already defined the target and quantities correctly,
  start with their obstacle rather than replaying the reformulation.
- If they find a direct relationship between z and x, develop it; naming s is
  optional when the model can be built without it.
- If they substitute 4.5 and 1.8 immediately, accept the equivalent numerical
  relationship. Preserve the distinction between fixed heights and changing
  positions.
- If they prefer to calculate the positions at x = 6 first, use that for
  orientation, then recover a relationship valid as the person moves before
  reasoning about rates.
- If a proposed model needs an assumption not supplied by the problem, make
  that assumption explicit or identify the missing information. Adding a symbol
  does not by itself make an underdetermined problem solvable.

The dialogue illustrates instruction. It is not a report of a live interaction
or a behavioral evaluation of the skill.
