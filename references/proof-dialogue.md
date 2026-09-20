# An annotated proof dialogue

This is an original fictional conversation illustrating the teaching approach
of *How to Solve It*, Part I, §19, “A problem to prove,” pp. 25–28. It uses a
different theorem and is not a transcription of Pólya's dialogue. Source:
[text of the book](https://studylib.net/doc/27587599/how-to-solve-it---polya).

Read it when you need an example of sustaining instruction through changing
subgoals. The instructor notes explain the teaching choices; they are not spoken
to the learner. In a real session, send only the next useful intervention and
wait. Do not recite this conversation or invent the learner's side of it.

## Problem and starting knowledge

**Problem:** Let ABCD be a convex quadrilateral, with its vertices named in order
around the boundary. Let E, F, G, and H be the midpoints of AB, BC, CD, and DA,
respectively. Prove that EFGH is a parallelogram.

The learner knows the definitions of midpoint and parallelogram, and that two
distinct lines parallel to the same line are parallel to each other. They have
also learned the triangle midpoint theorem: the segment joining the midpoints
of two sides of a triangle is parallel to its third side. They are unsure how
to select and apply such facts in a proof.

These prerequisites are part of this example's setup. With a real learner, use
evidence of their knowledge. Explain a missing theorem when needed rather than
trying to elicit something they have never learned.

## 1. Separate a drawing from the hypotheses

**Learner:** I drew ABCD as a rectangle and joined the midpoints. The inner shape
looks like a diamond. Could I show it is a rhombus and use that every rhombus is
a parallelogram?

**Instructor:** What properties did you give ABCD in your drawing that the
problem does not require?

**Learner:** Right angles and parallel opposite sides. Neither is given. My
drawing is only a special case. I'll draw an irregular convex quadrilateral.
The inner shape still looks like a parallelogram, but I can't justify it.

**Instructor note:** The learner has an observation and a proposed route, but
their evidence comes from a special case. The question checks that evidence
without declaring a visual guess to be a proof. It also leaves the learner to
notice the extra assumptions. A rhombus is indeed a parallelogram; the unsupported
step is expecting the inner figure always to be a rhombus.

## 2. Turn the conclusion into workable subgoals

**Instructor:** What would you need to establish to use the definition of a
parallelogram?

**Learner:** Both pairs of opposite sides must be parallel. So I need EF parallel
to GH, and FG parallel to EH.

**Instructor:** Which result you know might help establish one of those
parallelisms?

**Learner:** There is a theorem about joining midpoints in a triangle. That line
is parallel to the third side. We have midpoints here, but no triangles.

**Instructor note:** The learner chooses a theorem whose conclusion matches a
subgoal. The instructor has not named the theorem or prescribed a construction.
The midpoint conditions give the question a visible motivation and make the
connection accessible to this learner.

## 3. Make the chosen theorem usable

**Instructor:** What could you add to the figure to make that theorem usable?

**Learner:** I'm not sure. I can draw lots of lines, but I don't know where to
put one.

**Instructor:** E and F lie on AB and BC. What segment would complete a triangle
containing those two sides?

**Learner:** AC. If I join A to C, I get triangle ABC. E and F are the midpoints
of two of its sides, so EF is parallel to AC.

**Instructor note:** The general construction question did not produce an
action. The narrower question focuses on two sides already relevant to the
learner's theorem. It still leaves the construction and its use to the learner.
The instructor waits for that use rather than supplying all the consequences
of drawing AC.

## 4. Return from a new fact to the current goal

**Instructor:** You have proved EF is parallel to AC. How could that help you
establish EF parallel to GH?

**Learner:** If GH were also parallel to AC, that would do it. But I don't know
that yet.

**Instructor:** Which midpoint conditions have you not used?

**Learner:** G is the midpoint of CD and H is the midpoint of DA. Those are two
sides of triangle CDA! AC completed that triangle too. So GH is parallel to AC
by the same theorem. Then EF and GH are parallel. That makes EFGH a parallelogram.

**Instructor:** You have one pair of opposite sides parallel. What is still
needed from the definition you chose?

**Learner:** The other pair. I still need FG parallel to EH. I stopped too soon.

**Instructor note:** The learner first distinguishes a desired intermediate
claim from an established fact. Returning to the unused conditions helps them
prove it. Later, the instructor catches a premature conclusion precisely: the
first parallelism is sound, but it is only one part of the proposed proof.
Neither the useful construction nor the whole approach needs to be discarded.

## 5. Let the learner reuse the method

**Instructor:** What part of your first construction could you adapt to this
remaining pair?

**Learner:** For FG I have midpoints of BC and CD, so I should complete triangle
BCD by drawing BD. Then FG is parallel to BD. For EH, the midpoints are on BA
and AD, so triangle BAD gives EH parallel to BD. That proves FG parallel to EH.
Now both pairs are parallel.

**Instructor note:** The prompt becomes less specific because the learner has a
working method. The instructor does not name BD, introduce both triangles for
them, or make them answer separate questions about steps they can now combine.
This is evidence of transfer within the problem: the learner identifies the
structural similarity and selects the second construction.

## 6. Assemble and check the proof

**Instructor:** Write the argument as a proof, starting from the given midpoint
conditions and making clear why each pair of sides is parallel.

**Learner:** Let ABCD be any convex quadrilateral, with E, F, G, and H the
midpoints specified in the problem. Draw its diagonals AC and BD.

- In triangle ABC, E and F are the midpoints of AB and BC. By the triangle
  midpoint theorem, EF is parallel to AC.
- In triangle ADC, H and G are the midpoints of AD and DC. By the same theorem,
  HG is parallel to AC. Thus EF is parallel to HG.
- In triangle BCD, F and G are the midpoints of BC and CD. The theorem gives
  FG parallel to BD.
- In triangle BAD, E and H are the midpoints of BA and AD. The theorem gives
  EH parallel to BD. Thus FG is parallel to EH.

Both pairs of opposite sides of EFGH are parallel, so EFGH is a parallelogram.

**Instructor:** That proves the claim. The two diagonal constructions establish
both required parallelisms without assuming ABCD is a rectangle.

**Learner:** Does this really cover every convex quadrilateral? I only worked
with the one I drew.

**Instructor:** Which step depends on a measured length or angle from that
particular drawing?

**Learner:** None. Each use of the theorem only needs the specified midpoints.
The argument works for an arbitrary convex quadrilateral, not just the picture.

**Instructor note:** The learner supplies a complete forward argument after
discovering it through subgoals. The final question addresses an expressed doubt
about generality. It is not an extra exercise imposed after success. The proof
establishes a parallelogram, without claiming that the stronger rhombus guess
was true.

## 7. Look back at what suggested the construction

**Learner:** Can we go over how I was supposed to think of drawing diagonals?
I can follow the proof now, but that still feels like the hard part.

**Instructor:** You were trying to prove parallelism and remembered a theorem
whose conclusion gives parallel lines. That theorem needs a triangle with two
known midpoints. Completing that triangle suggested AC. What suggested BD?

**Learner:** The same question applied to the other pair of midpoints. I wasn't
just adding random lines: I was supplying what a useful theorem needed.

**Instructor:** That is the move you can reuse: look for a known result that
would establish your current goal, then inspect what is missing before you can
apply it.

**Instructor note:** The learner requested reflection, so the instructor makes
the origin of the construction explicit. They explain the connection that was
initially difficult, then invite the learner to account for the analogous step
they made with less help. The lesson is a way to select constructions, not an
instruction to draw diagonals in every geometry problem.

## Adapting this example

The instructional pattern is to clarify the target, let a relevant known result
suggest a subgoal, supply more concrete help at a demonstrated stall, and reduce
help when the learner can proceed. It does not prescribe this sequence for
every proof.

- If the learner already constructed the diagonals, begin with their argument;
  do not replay the discovery questions.
- If they propose coordinates or another valid proof, help develop that route.
  This example's geometry proof is not the only acceptable solution.
- If the learner needs the midpoint theorem explained, provide that support
  directly. A prerequisite gap is different from a failure to see where to apply
  a known result.
- If they request the complete solution, use a worked proof at the appropriate
  level rather than continuing to withhold steps.

This dialogue is an illustrative teaching reference, not evidence from a real
tutoring session or a behavioral evaluation of the skill.
