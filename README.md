What if an AI code reviewer could retain memory of your team's preferences?
While AI code reviewers are great at analyzing a Pull Request,many struggle to learn from the wider team or developers' past decisions as each PR is treated as a new codebase.
Our team of 6 has been experimenting with an alternative approach.
We imagine an AI code reviewer that learns from team, developer, and precedent memory to provide more contextual and personal feedback.

->3 Types of Memories

1. Team Memory - What the team as a whole wants the AI to remember
• Coding standards
• Architecture decisions
• Security concerns
• Project specific conventions
• Exceptions approved by the team

2. Developer Memory - What patterns or concerns does each developer have?
Instead of a generic reviewer, the AI can recognize patterns or oversights of individual developers
For instance, if a developer often misses edge cases in async functions, then the reviewer would focus more on those
The AI can also remember how a developer improves over time

3. Precedent Memory - What have past reviewers learned that can be applied to future PRs
This is probably the most exciting part.
Imagine an AI reviews a PR and flags some code, but a senior engineer responds explaining why that code is acceptable because of X.
Typically, that learning would be lost as the PR is merged and forgotten.
Our system stores that as precedent data so that future reviewers can apply that context when the same scenario appears.

->The Loop:

PR ➔ Context Detection ➔ Retrieve Memories ➔ Review Code ➔ Accept/Flag ➔ Update Memories

->Our prototype features:
1. Interactive PR/Code Reviewer
2. Team Memory Dashboard
3. Developer Insights Page
4. Decision and Precedent Log
5. AI Review Comments
6. Accept / False Positive / Team Decision Feedback
7. Real-time Memory Updates

->Prototype:  https://ledgerprototype.vercel.app/

The objective of our project is not to replace human code reviewers, but to augment and support them by improving the consistency and context of an AI reviewer.
As the team uses the system, the AI reviewer can provide feedback geared specifically to that team.
This project combines the talents of our team of 6 who have interests ranging from AI, to software engineering, to developer tools, and even to the concept of memory itself.
