# Cricket-Highlight
Project Overview

This project is a simple implementation of an automated cricket highlight generator.  
In real matches, a full cricket game lasts around 3 to 4 hours, but highlights are usually only 30–60 minutes. This project tries to solve that problem by identifying important moments from ball-by-ball match data.
The system uses a rule-based approach to filter key events like sixes, fours, wickets, and player milestones.

Problem Statement
Watching a full cricket match is time-consuming. Viewers prefer short highlights that capture the most important moments.
So, the problem is:
How to automatically convert a full-length cricket match into short highlights?

 Objective
To identify important moments from a cricket match  
To reduce full match data into short highlight sequences  
To simulate how highlight systems work in real broadcasts  

 Approach / Methodology
Step 1: Data Representation
Each ball in the match is stored with:
- Over number (e.g., 18.2)
- Event (SIX, FOUR, WICKET, etc.)
- Runs scored
- Batsman name

Step 2: Event Identification
Only important events are considered:
- SIX  
- FOUR  
- WICKET  
- Milestones (Half-century, Century)

Step 3: Scoring System
Each event is given a score based on importance:

| Event |   Score    |
|-------|------------|
| WICKET| High       |
| SIX   | Medium-High|
| FOUR  | Medium     |

Additional conditions:
- Events in death overs (16–20) get higher priority  
- Milestones also get extra importance  

Step 4: Sorting
- Events are sorted based on score 
- Top events are selected  

Step 5: Highlight Generation
- Selected events are sorted back in match order  
- Final output shows a timeline of highlights  

Sample Output
Match Highlights:
1.2 - FOUR
1.3 - SIX
3.1 - WICKET
16.1 - SIX
18.1 - SIX
20.1 - SIX

Conclusion
This project demonstrates a basic approach to generating cricket highlights using simple rules and data processing. It gives an idea of how large match data can be reduced into meaningful short summaries.
