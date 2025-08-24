
🪄 CodeTailor Examples - Try the "Get Help" button
==================================================

Provide a Solution-only Personalized Adaptive Puzzle
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This provides a **solution-only personalized adaptive puzzle** based on students' current written code.
The students can interact with the puzzle and try to solve it.

The students can regenerate the puzzle based on their updated code anytime by clicking the "Regenerate Help" button.

:Paired Block Sets: 
    - Pairs a correct block with an incorrect block that is not needed in a correct solution.
    - Try to use students' own wrong code as distractor blocks.

    
.. activecode::  str-mixed-example-solper
    :autograde: unittest
    :parsonspersonalize: movable
    :parsonsexample: str-mixed-example-pp

    Finish a function, ``phrase(person, thing)``:
        - It has ``person`` and ``thing`` as input.
        - First verify whether ``person`` and ``thing`` are strings. If not, return ``False``.
        - If ``person`` and ``thing`` are two strings, return one string with the characters in ``person``, followed by an empty space, and then followed by ``thing``
        - Make sure the first letter in ``person`` is capitalized and all the characters in ``thing`` are lowercase.
       
        .. table::
            :name: phrase_table_solper
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
        return person + " " + thing
        # more bugs ...




    ====
    from unittest.gui import TestCaseGui

    class myTests(TestCaseGui):
        def testOne(self):
            self.assertEqual(phrase("sam", "Likes to code"), "Sam likes to code", 'phrase("sam", " Likes to code")')
            self.assertEqual(phrase("mary-anne", "likes to sing"), "Mary-anne likes to sing", 'phrase("mary-anne", " likes to sing")')
            self.assertEqual(phrase("ANNA", "likes to dance"), "Anna likes to dance", 'phrase("ANNA", " likes to dance")')
            self.assertEqual(phrase(1111, "likes programming"), False, 'phrase(1111, " likes programming")')


    myTests().main()


.. parsonsprob:: str-mixed-example-pp
    :numbered: left

    Finish a function, ``phrase(person, thing)``:
            - It has ``person`` and ``thing`` as input.
            - First verify whether ``person`` and ``thing`` are strings. If not, return ``False``.
            - If ``person`` and ``thing`` are two strings, return one string with the characters in ``person``, followed by an empty space, and then followed by ``thing``
            - Make sure the first letter in ``person`` is capitalized and all the characters in ``thing`` are lowercase.
    -----
    def phrase(person, thing): # a correct solution
    =====
        if type(person) == str and type(thing) == str:
    =====
                person = person.capitalize()
                thing = thing.lower()
                return person + " " + thing
    =====
        else:
    =====
            return False



What to do next
^^^^^^^^^^^^^^^

.. raw:: html

    <p>Click on the following link to try: <b><a id="multi_level_per_puzzle"> <font size="+1">A Block-and-Solution Personalized Adaptive Puzzle</font></a></b></p>

.. raw:: html

    <script type="text/javascript" >

      window.onload = function() {

        a = document.getElementById("multi_level_per_puzzle")
        a.href = "multi_level_per_puzzle.html"
      };

    </script>