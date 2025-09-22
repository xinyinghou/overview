CodeTailor
----------

The primary goal is to complete the write-code problem, with the optional puzzle providing guidance and hints. 
The puzzle presents essential code snippets and logic in a scrambled order.

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


You can click the **"Get Help"** button below the problem description to access a mixed-up puzzle that will guide you through solving the write-code task. 
You can click the **"Close Help"** button to close the help view and return to the main problem.
You can click the **"See Help Again"** button to reopen the help puzzle anytime.
You can click the **"Regenerate Help"** button to regenerate a new puzzle based on your current code in the write-code editor.

Solution-only personalized adaptive puzzle
-----------------------------------------------
This provides a **solution-only personalized adaptive puzzle** based on students' current written code.
The students can interact with the puzzle and try to solve it.

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

After generating a correct solution within the puzzle, you will see a **Copy answer to clipboard** button.
You can copy the completed code to your clipboard and paste it into the write-code editor.

Click on the "Show Source" button below to see what the reStructuredText (rst) looks like for the CodeTailor code above.  

.. reveal:: codetailor1_source
   :showtitle: Show Source
   :hidetitle: Hide Source
   :modaltitle: Source for the example above

   .. code-block:: rst

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
