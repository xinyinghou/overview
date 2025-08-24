
🪄 CodeTailor Examples - Try the "Get Help" button
===================================================

Provide a Solution-only Personalized Adaptive Puzzle
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This provides a **solution-only personalized adaptive puzzle** based on students' current written code.

The students can regenerate the puzzle based on their updated code anytime by clicking the "Regenerate Help" button.

:Paired Block Sets: 
    - Pairs a correct block with an incorrect block that is not needed in a correct solution.
    - Try to use students' own wrong code as distractor blocks.

    
.. activecode::  has22-example-solper-java
    :language: java
    :autograde: unittest
    :parsonspersonalize: movable

    Create a method ``has22(nums)`` that takes an array of integers, ``nums`` and returns ``true`` if there are at least two items in the list that are adjacent and both equal to 2, otherwise return false.

    .. table::
        :name: phrase_table_solcode
        :align: left
        :width: 50

        +-------------------------------------+-------------------------------+
        | Example Input                       | Expected Output               |
        +=====================================+===============================+
        | ``has22({1, 2, 2})``                | ``true``                      |
        +-------------------------------------+-------------------------------+
        | ``has22({1, 2, 1, 2})``             | ``false``                     |
        +-------------------------------------+-------------------------------+
        | ``has22({2, 1, 2})``                | ``false``                     |
        +-------------------------------------+-------------------------------+



    ~~~~
    import java.util.Scanner;
    import java.util.Arrays;

    public class Has22 {
        public static boolean has22(int nums) {
            for (int i = 0; i < nums.length - 1; i++) {






    ====
    import static org.junit.Assert.*;
    import org.junit.Test;

    class TestHelper {
        public static void runAllTests() throws Exception {
            if (!Has22.has22(new int[]{1, 2, 2, 3})) {
                throw new Exception("Test 1 failed");
            }
            if (Has22.has22(new int[]{2, 3, 2})) {
                throw new Exception("Test 2 failed");
            }
            if (Has22.has22(new int[]{1, 3, 4, 5})) {
                throw new Exception("Test 3 failed");
            }
        }
    }


    public class RunestoneTests {
        @Test
        public void testPhrase() throws Exception {
            try {
                TestHelper.runAllTests();
                System.out.println("✅ All tests passed!");
                System.out.println("Test 1: phrase(\"Sam\", \"Likes to code\") -> Sam likes to code");
                System.out.println("Test 2: phrase(123, \"code\") -> null");
                System.out.println("Test 3: phrase(\"JANE\", \"Loves JAVA\") -> Jane loves java");
            } catch (Exception e) {
                System.out.println("❌ " + e.getMessage());
                fail(e.getMessage());
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