
🪄 CodeTailor Examples - Try the "Get Help" button
===================================================

Provide a Block-and-Solution Personalized Adaptive Puzzle with a common solution-based one as the safeguard
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This type provides a **block-and-solution personalized adaptive puzzle** based on students' current written code.

The students can interact with the puzzle and try to solve it.

The students can regerenate the puzzle based on their updated code anytime by clicking the "Regerenate Help" button.

:Movable Blocks:
    Move the correct blocks from the left box to the right box and put them into the correct order.

:Static Blocks: 
    - The Static blocks are the blocks that are already in position in the answer box. You can not move them.
    - You can hover over the static blocks to see how many blocks are needed above and below them.

:Paired Block Sets: 
    - Pairs with a correct block and an incorrect block that is not needed in a correct solution.
    - Use students' own wrong code as distractor blocks.
    - The incorrect blocks may contain syntactic or semantic errors.
    - The correct code is randomly shown above or below the incorrect block.


.. activecode::  str-mixed-example-multiper-java
    :language: java
    :autograde: unittest
    :nocodelens:
    :multiperpuzzle:

    Complete the method ``phrase(Object person, Object thing)``.  First verify whether ``person`` and ``thing`` are instances of ``String``. If not, return ``null``.  
    If ``person`` and ``thing`` are both strings, return one string with a ``person`` of your choosing followed by a ``thing`` that person likes to do.  
    Make sure that ``person`` is capitalized (first letter uppercase, the rest lowercase), and ``thing`` is entirely lowercase.  
    For example, if the ``person`` is ``"Sam"`` and ``thing`` is ``"Likes to code"``, the returned string should be ``"Sam likes to code"``.  
    Make sure that ``person`` is capitalized and ``thing`` is lowercase.

    .. table::
        :name: phrase_table_solcode
        :align: left
        :width: 50

        +---------------------------------------------------+-------------------------------+
        | Example Input                                     | Expected Output               |
        +===================================================+===============================+
        | ``phrase("Sam", "Likes to code")``                | ``"Sam likes to code"``       |
        +---------------------------------------------------+-------------------------------+
        | ``phrase("ANN", "Likes to CODE")``                | ``"Ann likes to code"``       |
        +---------------------------------------------------+-------------------------------+
        | ``phrase(1, "Python")``                           | ``null``                      |
        +---------------------------------------------------+-------------------------------+


    ~~~~
    import java.util.Optional;

    public class PhraseBuilder {
        public static String phrase(Object person, Object thing) {
            return Optional.ofNullable(person)
                    .filter(p -> p instanceof String)
                    .map(p -> ((String) p).toLowerCase())
                    .map(p -> Character.toUpperCase(p.charAt(0)) + p.substring(1))
                    .flatMap(p -> Optional.ofNullable(thing)




    ====
    import static org.junit.Assert.*;
    import org.junit.Test;

    public class RunestoneTests {

        @Test
        public void testPhrase() {
            // Test cases: {person, thing, expectedOutput}
            Object[][] testCases = {
                {"Sam", "Likes to code", "Sam likes to code"},
                {"ANN", "Likes to CODE", "Ann likes to code"},
                {1, "Python", null},
                {"jack", 42, null},
                {null, "hello", null},
                {"BOB", "RUNS FAST", "Bob runs fast"}
            };

            StringBuilder feedback = new StringBuilder();
            StringBuilder passedCases = new StringBuilder();
            StringBuilder failedCases = new StringBuilder();
            boolean allPassed = true;

            for (Object[] testCase : testCases) {
                Object person = testCase[0];
                Object thing = testCase[1];
                String expected = (String) testCase[2];
                String result = PhraseBuilder.phrase(person, thing);

                if ((expected == null && result == null) || (expected != null && expected.equals(result))) {
                    passedCases.append("✅ Passed: phrase(")
                            .append(person)
                            .append(", ")
                            .append(thing)
                            .append(") -> Expected: ")
                            .append(expected)
                            .append("\n");
                } else {
                    allPassed = false;
                    failedCases.append("❌ Failed: phrase(")
                            .append(person)
                            .append(", ")
                            .append(thing)
                            .append(") -> Expected: ")
                            .append(expected)
                            .append(", Got: ")
                            .append(result)
                            .append("\n");
                }
            }

            if (!allPassed) {
                feedback.append("Some test cases failed.\n\n")
                        .append("=== Passed Test Cases ===\n")
                        .append(passedCases)
                        .append("\n=== Failed Test Cases ===\n")
                        .append(failedCases);
                System.out.println(feedback.toString());
                fail("One or more test cases failed.");
            } else {
                System.out.println("Passed! Your function works as expected.\n" + passedCases);
            }
        }
    }


Thanks for trying CodeTailor! 🎉
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^