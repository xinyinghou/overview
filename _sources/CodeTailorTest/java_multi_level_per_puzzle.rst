
🪄 CodeTailor Examples - Try the "Get Help" button
===================================================

Provide a Block-and-Solution Personalized Adaptive Puzzle 
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

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


.. activecode::  has22-example-multiper-java
    :language: java
    :autograde: unittest
    :parsonspersonalize: partial

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



Thanks for trying CodeTailor! 🎉
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^