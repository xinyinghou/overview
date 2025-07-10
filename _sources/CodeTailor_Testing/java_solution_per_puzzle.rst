
🪄 CodeTailor Examples - Try the "Get Help" button
===================================================

Provide an Only-solution Personalized Adaptive Puzzle with a common solution (example solution)-based one as the safeguard
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This type provides an **only-solution personalized adaptive puzzle** based on students' current written code.

No distractor blocks are provided. The students can interact with the puzzle and try to solve it.

The students can regerenate the puzzle based on their updated code anytime by clicking the "Regerenate Help" button.

.. activecode::  str-mixed-example-solper-java
    :language: java
    :autograde: unittest
    :nocodelens:
    :solperpuzzle:

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
    // Here is a student's buggy code
    public class PhraseBuilder {
        public static String phrase(Object person, Object thing) {
            if (!(person instanceof String) || !(thing instanceof String)) {
                return "False";
            }

            String personStr = ((String) person).toUpperCase();
            String thingStr = ((String) thing); 

            return personStr + thingStr;
        }
    }




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



What to do next
^^^^^^^^^^^^^^^

.. raw:: html

    <p>Click on the following link to try: <b><a id="java_multi_level_per_puzzle"> <font size="+1">A Java Block-and-Solution Personalized Adaptive Puzzle</font></a></b></p>

.. raw:: html

    <script type="text/javascript" >

      window.onload = function() {

        a = document.getElementById("java_multi_level_per_puzzle")
        a.href = "java_multi_level_per_puzzle.html"
      };

    </script>