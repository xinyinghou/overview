
🪄  Examples - Try the "Get Help" button
=====================================================

Provide a Common-Solution-based Adaptive Puzzle 
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
This type provides a common solution-based adaptive puzzle to all students. 

No distractor blocks are provided. The students can interact with the puzzle and try to solve it.

.. activecode::  str-mixed-example-cp
    :autograde: unittest
    :nocodelens:
    :commonparsons:

    Finish a function, ``phrase(person, thing)``:
        - It has ``person`` and ``thing`` as input.
        - First verify whether ``person`` and ``thing`` are strings. If not, return ``False``.
        - If ``person`` and ``thing`` are two strings, return one string with the characters in ``person``, followed by an empty space, and then followed by ``thing``
        - Make sure the first letter in ``person`` is capitalized and all the characters in ``thing`` are lowercase.
       
        .. table::
            :name: phrase_table_cp
            :align: left
            :width: 50

            +-------------------------------------+---------------------------------------+
            | Example Input                       | Expected Output                       |
            +=====================================+=======================================+
            |``phrase("Sam", "Likes to code")``   | ``"Sam likes to code"``               |
            +-------------------------------------+---------------------------------------+
            |``phrase("ANN", "Likes to CODE")``   | ``"Ann likes to code"``               |
            +-------------------------------------+---------------------------------------+
            |``phrase(1, "Python")``              | ``False``                             |
            +-------------------------------------+---------------------------------------+

    ~~~~
    # Here is a student's buggy code
    # click the "Get Help" button above to see what it provides.

    def phrase(person, thing):
        if type(person) == str or type(thing) == str: # bug 1 
            person = person.capitalize # bug 2
            thing = thing.lower()
        else:





    ====
    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):
        def testOne(self):
            self.assertEqual(phrase("sam", "Likes to code"), "Sam likes to code", 'phrase("sam", " Likes to code")')
            self.assertEqual(phrase("mary-anne", "likes to sing"), "Mary-anne likes to sing", 'phrase("mary-anne", " likes to sing")')
            self.assertEqual(phrase("ANNA", "likes to dance"), "Anna likes to dance", 'phrase("ANNA", " likes to dance")')
            self.assertEqual(phrase(1111, "likes programming"), False, 'phrase(1111, " likes programming")')



    myTests().main()

What to do next
^^^^^^^^^^^^^^^

.. raw:: html

    <p>Click on the following link to try: <b><a id="solution_per_puzzle"> <font size="+1">An Only-solution Personalized Adaptive Puzzle</font></a></b></p>

.. raw:: html

    <script type="text/javascript" >

      window.onload = function() {

        a = document.getElementById("solution_per_puzzle")
        a.href = "solution_per_puzzle.html"
      };

    </script>