## Reference-Free Prompt for ICE-Score in Code Summarization Task

```
You will be given the code summary for a code snippet.
Your task is to rate the summary only on one metric.
Please make sure you read and understand these instructions carefully.
Please keep this document open while reviewing, and refer to it as needed.

### Evaluation Criteria:
Content Adequacy (0-4) The Content Adequacy is measured by assessing the extent to which the summary lacks information needed to understand the code.

- A score of 0 (lacking all information) means that the code summarization is totally incorrect and meaningless.
- A score of 4 (perfectly contains all information) means that the code summarization is perfectly correct and perfectly contains all necessary information.

### Evaluation Steps:
1. Read the code carefully and understand the functionalities of the implementation.
2. Read the code summary and compare it to the code. Check if the code summary covers the functionalities of the code.
3. Assign a score for Content Adequacy on a scale of 0 to 4, where 0 is the lowest and 4 is the highest, based on the Evaluation Criteria.

---

Code Snippet:

{{CODE}}

Summary for Evaluation:

{{GeneratedSummary}}

Evaluation Form: 
Content Adequacy (scores ONLY):

```

## Reference-Enhanced Prompt for ICE-Score in Code Summarization Task

```
You will be given the code summary for a code snippet.
Your task is to rate the summary only on one metric.
Please make sure you read and understand these instructions carefully.
Please keep this document open while reviewing, and refer to it as needed.

### Evaluation Criteria:
Content Adequacy (0-4) The Content Adequacy is measured by assessing the extent to which the summary lacks information needed to understand the code.

- A score of 0** (lacking all information) means that the code summarization is totally incorrect and meaningless.
- A score of 4 (perfectly contains all information) means that the code summarization is perfectly correct and perfectly contains all necessary information.

### Evaluation Steps:
1. Read the code carefully and understand the functionalities of the implementation.
2. Read the code summary and compare it to the reference summary. Check if the code summary covers the functionalities of the code.
3. Assign a score for Content Adequacy on a scale of 0 to 4, where 0 is the lowest and 4 is the highest, based on the Evaluation Criteria.

---

Code Snippet:

{CODE}}

Reference Summary:

{{REFERENCE}}

Summary for Evaluation:

{{GeneratedSummary}}

Evaluation Form:  
Content Adequacy (scores ONLY):

```


## Reference-Free Prompt for ICE-Score in APR Task
```
You will be given the code patch for fixing a bug.
Your task is to rate the patch only on one metric.
Please make sure you read and understand these instructions carefully.
Please keep this document open while reviewing, and refer to it as needed.

### Evaluation Criteria:
 Functional Correctness (0-4): To what extent does the patch correctly fix the bug?
  - 0: Completely incorrect or irrelevant regarding addressing the bug.
  - 4: Completely correctly fix the bug, cover all edge conditions.

### Evaluation Steps:
1. Read the bug carefully and identify the issues.
2. Read the code patch and compare it to the bug. Check if the patch indeed fixes the bug.
3. Assign a score for functional correctness on a scale of 0 to 4, where 0 is the lowest and 4 is the highest, based on the Evaluation Criteria.


Problem:

{{PROBLEM}}

Patch:

{{OUTPUT}}

Evaluation Form:
functional correctness (scores ONLY):

```

## Reference-Enhanced Prompt for ICE-Score in APR Task
```
You will be given the code patch for fixing a bug.
Your task is to rate the patch only on one metric.
Please make sure you read and understand these instructions carefully.
Please keep this document open while reviewing, and refer to it as needed.

Evaluation Criteria:
 Functional Correctness (0-4): To what extent does the patch correctly fix the bug?
  - 0: Completely incorrect or irrelevant regarding addressing the bug.
  - 4: Completely correctly fix the bug, cover all edge conditions.


Evaluation Steps:
1. Read the bug carefully and identify the issues.
2. Read the code patch and compare it to the reference patch. Check if the patch indeed fixes the bug, and if it is as good as the reference patch.
3. Assign a score for functional correctness on a scale of 0 to 4, where 0 is the lowest and 4 is the highest, based on the Evaluation Criteria.

Problem:

{{PROBLEM}}

Reference Patch:

{{REFERENCE}}

Patch:

{{OUTPUT}}

Evaluation Form:
functional correctness (scores ONLY):
```
