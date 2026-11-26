
# AI Collaboration Log

This log records significant AI interactions for the AIAS Level 3 requirement. It feeds the
300–500 word AI Collaboration Statement at the end of the notebook.

**Tool:** Claude (Anthropic), model Claude Opus 5.5, used through claude.ai.

| Date | Task | What the AI produced | What I checked, changed or decided |
|---|---|---|---|
| 08-Nov-2026 | Stakeholders and success criteria | Pointed out potential users and stakeholders; wrote technical and practical criteria to help me choose points | Chose the points to write on |
| 10-Nov-2026 | Understanding the data | Explained the meanings of a few values I couldn't make sense of | Caught that I'd misread "0-9y" as an age group when it's driving experience |
| 10-Nov-2026 | Exploration questions | Helped with questions I could ask, e.g. "Which groups seem to have a higher rate than average" | Only used numbers that came from running the code myself |
| 10-Nov-2026 | Histograms and diagrams | Helped write the histograms and charts and gave pointers on what to look for | Claude pointed out my reason for using the median didn't fit, because the columns with missing values aren't skewed. I checked the numbers and rewrote it |
| 12-Nov-2026 | Q4 and Q5: past accidents and driving experience | Recommendations on what to add to my code (median with dotted lines) | I wrote the code and used its suggestion for the median line |
| 12-Nov-2026 | Q4 interpretation | Pointed out I had read numbers off the chart instead of the table, and that my reason was wrong (a rate already accounts for group size); explained the likely reason (new drivers all have 0 accidents) and gave example wording | Wrote the first draft myself and reworded the example |
| 12-Nov-2026 | Q5 and dropping PAST_ACCIDENTS | Gave the weaknesses of dropping it; checked SPEEDING_VIOLATIONS and DUIS | Used the same method as my Q2 gender check. Decided to drop PAST_ACCIDENTS because drivers with accidents claim less even with the same experience. Kept SPEEDING_VIOLATIONS and DUIS as they don't show the same pattern |
|17-Nov-2026| Data Qaulity Report | Recomendations on What i should check| AI produced that i should check for missing values and pointed back to my Report earlier | I wrote and adapted my Code to the recomendations that AI gave me  |
|17-Nov-2026| Data Quality report - Duplicates | AI produced some of the Code to check if the values in the dataset are duplicate values| I overlooked on the code it gave me and used it to check it and used the Result it gave me  | 
|17-Nov-2026| Data Qaulity report - Outliers and unusual values | I asked AI to explain what it is and what i could mention AI Produced 'Check weather values are strange to be in a model  check 1. Very high counts, 2. Rounded values, 3. Postal code , 4. New drivers have zero of everything'| I decided to go ahead with these checks|
|17-Nov 2026|Outliers and unusual values| AI produced that i should check the 2 patterns that was found earlier which was new drivers and postal codes in Q1| I Decided to check these patterns|
|17-Nov - 2026| Outlier and unusual values Code | Ai suggested I check the IQR way to which will give me the Potential Outliers | I then choose to Apply these to give my Qaulity report a more accurate Reponse |
|19-Nov-2026| Data preperation-Priority issues | Ai Suggested i should check the Postal Code issue and target imbalanced | I decided to use these and move Forward with my Data preperation |
|19-Nov-2026| Data preperation | Claude explained that the scikit-learn decision tree only works with numbers, so I turned the text columns into numbers. For ordered groups like age and income, I numbered them from 0 (lowest) upwards to keep their order | I applied the suggestion and used it |
| 19-Nov-2026 | Data Preperation 3.6 and 3.7 | Explained Integration and Feature construction and the preparation log columns; gave a better reason for not making a combined offence column (a DUI is more serious than a speeding fine, and the tree can use both columns on its own) | Decided not to create any new columns. Reworded 3.6 and the preparation log in my own words, and changed "1 column" to the number of values affected |
| 19-Nov-2026 | Data Preperation |Assisted me with code for selection, encoding, train/test split, and filling missing values, plus explanations| I used its help but did the work myself: ran all cells, verified the outputs, fixed errors, and made sure I understood everything.|
| 26-Nov-2026 | Checking my notebook against the brief, lectures and labs | Downloaded my Data Analytics lectures, labs, tutorials, brief and report template from Canvas and compared Phases 1-3 with them | I asked for the check and reviewed the list of problems it found |
| 26-Nov-2026 | Fixing Phases 1-3 | Edited my notebook directly: removed crashing and duplicate cells, corrected numbers that did not match the output (MARRIED/CHILDREN were the wrong way round, income, Q2, Q5), fixed the Phase 3 headings, added the validation cell, saved the prepared data and updated the preparation log | Reviewing every change in VS Code and re-running the notebook before I commit |
| 26-Nov-2026 | Adding what the lectures and labs teach | Added box plots, a correlation heatmap and a scatter plot (Lecture 2, Lab 1), a missing-values bar chart (Lab 3), the positive class and a split check (Lab 5), with first-draft interpretations | Will reword the interpretations in my own words. Kept the training-only median because the brief overrides Lab 3 on this |
| 26-Nov-2026 | GENDER decision | Pointed out that Lab 5 drops sensitive columns and only uses them to check fairness, and that my paper cites Test-Achats | I decided to keep GENDER as an input because Q2 shows men claim more at the same experience; the model is for understanding risk, not pricing, and I will check fairness by gender in Evaluation |
