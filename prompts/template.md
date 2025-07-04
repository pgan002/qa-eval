Given a question, reference answer and candidate answer, split each answer into points or claims, find corresponding claims between the two answers, and output the values for the below output fields, separated by <tab>.

# Output fields
f1. Count of matching claims.
f2. Count of reference answer claims.
f3. Count of candidate answer claims.
f4. English explanation of how you divided the answers into claims; if claims do not match exactly, how you match them; any assumptions or interpretation.

# Additional instructions
* Count as one claim:
    * A one-word answer
    * An answer that means "I do not know"
    * Claims with the same meaning
* Output format is <f1>\t<f2>\t<f3>\t<f4>
* Output contains only values separated by <tab>, no field names such as 'f1'

# Value checks
* f1, f2, f3 are integers
* f1 >= 0
* f1 <= f2
* f1 <= f3
* f2 >= 1
* f3 >= 1
* f4 contains no <tab>
* f4 is in English

# Question
{question}

# Reference answer
{reference_answer}

# Candidate answer
{candidate_answer}

