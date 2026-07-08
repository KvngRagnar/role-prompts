# Objective: Use role-based prompts for personalized feedback.

    Ask the model to act as a coding mentor.

## Provide a simple piece of code (e.g., a Python function with a bug).


    CODE PROVIDED

        def check_palindrome(string):
            first_checker = 0  # starting point for forward iteration
            last_checker = len(string) -1 # starting point for backward iteration

            while first_checker < last_checker:  # so the pointers to not check already comfirmed characters
                if string[first_checker] != string[last_checker]:
                    return False
                else:
                    first_checker += 1  #iterate 1 place forward
                    last_checker -= 1   #iterate 1 place backward
            return True


## Prompt the model: "Act as a mentor reviewing this code. Provide corrections and explain improvements."

    Model Response

        First, well done for implementing the two-pointer technique — that shows you understand how to compare characters from both ends efficiently. The logic is correct and the function will properly identify basic palindromes.


        That said, there are a few improvements you can make:

            Handle case sensitivity
            Right now, "Racecar" would return False because uppercase and lowercase letters are treated differently. You can normalize the string using .lower().

            Handle spaces and special characters
            A phrase like "nurses run" would return False because of the space. You may want to remove spaces (and possibly punctuation) before checking.

            Remove unnecessary else block
            The else statement is not required because if the if condition is false, the loop automatically continues. Removing it improves readability.

            Minor comment corrections
            There are small spelling errors in comments (e.g., “comfirmed” → “confirmed”). Clean comments improve professionalism.

    The mentor pointed out that the function works correctly for basic palindrome checks but suggested improvements for readability and edge cases, also that the function does not handle uppercase letters, spaces, or special characters, which could cause incorrect results for inputs like "Racecar" or "nurses run".

    It also recommended normalizing the string using .lower() and possibly removing spaces before performing the comparison, and that I should simplify the logic using Python slicing (string == string[::-1]) for cleaner code.
    The tone of the response was supportive, constructive, and focused on helping me grow as a devoloper rather than just pointing out mistakes.


## Review the response and check if the role influences feedback style.

    The mentor role clearly influenced the feedback style. Instead of simply saying what was wrong, the response explained why improvements were needed and suggested better practices. The tone felt encouraging and educational rather than critical. It focused not only on fixing issues but also on teaching cleaner and more Pythonic approaches. This shows that role-based prompting changes the way feedback is delivered making it more supportive, detailed, and improvement-oriented.