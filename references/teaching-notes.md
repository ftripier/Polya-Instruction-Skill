# Teaching notes

These are original examples for this skill. Adapt them to the learner's actual
work; they are not scripts to repeat or excerpts from Pólya.

## Choosing the next question

The four checks in `SKILL.md` paraphrase Pólya's objections in Part I, §17,
pp. 22–23. His example criticizes prematurely naming Pythagoras: the student may
not see where it applies, or may receive the crucial idea without learning how
to find it. Read the section in this
[transcription of the book](https://studylib.net/doc/27587599/how-to-solve-it---polya).

Use the following original examples to distinguish the learner's next useful
operation from the instructor's knowledge of the answer.

### A method name at the wrong moment

**Learner:** “I need the diagonal of a rectangle with sides 3 and 4. I know some
triangle formulas, but I don't see a triangle here.”

**Premature:** “Can you use Pythagoras?” The missing connection is geometric;
another formula name does not help them see it.

**Better next question:** “What shapes appear if you draw the diagonal inside
the rectangle?” This invites the learner to construct the relevant representation.
Stop there and use their response.

**If they identify a right triangle:** “Which relationship you know connects its
side lengths?” If only the theorem's name or formula is missing, supply it and
explain how the sides correspond. Naming Pythagoras is now motivated; there is
no need to prolong a recall exercise.

The transferable move is to draw the target quantity and look for familiar
structure. It is not a rule to try Pythagoras whenever a length is unknown.

### An observation the learner has already made

**Learner:** “I checked that the first few sums of odd numbers are squares. I
know induction, but I'm stuck on how to go from n to n + 1.”

**Unhelpful:** “Can you check a few small cases?” It repeats completed work.
“Add 2n + 1 to n² to get (n + 1)²” gives away the step they want to construct.

**Better next question:** “What term is added when you extend the sum from n odd
numbers to n + 1?” The learner can work out the change, then connect it to the
inductive assumption. If identifying that term is the obstacle, use a concrete
n before returning to the general case.

The transferable move is to compare neighboring cases and isolate what changes.
The same problem needs a different prompt for a learner who has not yet spotted
the pattern, as in the next example.

## A learner has no starting point

**Learner:** “Help me prove that the sum of the first n odd numbers is n². I don't
know where to start. Please don't give me the proof.”

**Possible response:** “Try writing out the sums for n = 1, 2, 3, and 4. What do
you notice about how each total grows from the previous one?”

This offers an accessible action. It does not assume that the learner knows
induction or reveal the whole proof. If they already noticed that pattern, use
their observation to choose the next prompt instead of assigning the same work.

## An algebraic step loses a solution

**Learner:** “For x² = x I divided by x and got x = 1. Is that right?”

**Possible response:** “x = 1 does satisfy the equation. Dividing by x assumes
that x is nonzero. What happens if you substitute x = 0 into the original
equation?”

Validate only what is valid. Locate the lost case instead of restarting the
solution. If the learner does not understand division by zero, explain that
prerequisite directly.

## A useful next step in debugging

**Learner:** “I'm learning binary search. Mine loops forever on a two-element
list. Help me figure it out; don't rewrite it.”

If the code is absent, ask for the loop and a failing input. If it is present,
inspect it first. A useful prompt might ask the learner to trace `low`, `high`,
and `mid` through one iteration and check whether the search interval shrinks.
Do not diagnose a particular bug without the code, or patch it before the learner
has had a chance to investigate. A requested test run can supply evidence for
their investigation.

## More help is needed

**Learner:** “I still don't understand what you mean by an invariant.”

Explain the term briefly and give a small example suited to this problem. Then
offer a concrete application. Another “What stays the same?” is unlikely to help
if the concept itself is missing.

**Learner:** “I'm out of time. Please show me the full solution now.”

Give the worked solution at an appropriate level, including why the decisive
step works and a check of the result. The learner's request overrides the default
hint-by-hint pace.

## Reading in How to Solve It

G. Pólya, *How to Solve It: A New Aspect of Mathematical Method*, second edition,
Princeton University Press, 1957. Page numbers below are printed book pages;
section titles are more reliable across editions and PDF viewers.

| Location | Relevance |
| --- | --- |
| Part I, §1, “Helping the student,” p. 1 | Balance assistance with independent work. |
| Part I, §§2–5, pp. 1–4 | Questions, generality, and learning through practice. |
| Part I, §§6–14, pp. 5–19 | Four phases illustrated through teacher–student exchanges. |
| Part I, §16, “The teacher's method of questioning,” pp. 20–22 | Move from general prompts toward concrete suggestions as needed. |
| Part I, §17, “Good questions and bad questions,” pp. 22–23 | Judge how a question helps the learner think. |
| Part III, “Diagnosis,” p. 94; “Pedantry and mastery,” p. 148; “Rules of teaching,” p. 173 | Further instructor-focused reading. |

Sources: [book scan hosted by the University of Georgia](https://jwilson.coe.uga.edu/emt725/References/Polya_HowToSolveIt.pdf)
and [table of contents from AAAS Project 2061](https://www.project2061.org/publications/rsl/online/TRADEBKS/TOCS/HOW2SOLV.HTM).

The question-selection workflow, chat pacing, handling of explicit solution
requests, and tool-use guidance are design choices for a contemporary agent
instructor. They should not be attributed to Pólya as literal instructions. The
four question checks are a paraphrase of §17, not a verbatim checklist from the
book. No copy of the book is bundled.
