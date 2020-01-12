# DV8 and RefBot

## Goal

We want to find whether the problematic (a) file clusters or (b) individual files identified by RefBot overlap with those identified by DV8. How do they differ? How are they similar?

## DV8

The tools included in DV8 are primarily concerned with architecture, or rather, the relationships between files and not just files themselves. 

1. *Decoupling Level (DL) and Propagation Cost (PC)* - These are project-wide metrics. They are given as percentages.
2. *Architecture Anti-Patterns* - A set of design flaws that can be detected algorithmically and have been shown to incur large maintenance costs. Each flaw is a set of files.
3. *Architecture Roots* - A root is a set of files. While a system can have any number of flaws, roots attempt to capture the most problematic files in a minimum amount of file sets. "Five roots can typically cover 50% to 90% of all the error-prone files ina system."

## RefBot

RefBot is a guided refactoring tool. Intuitively, it should start refactoring with the most problematic (change-prone or error-prone) file sets. Does this overlap with the files identified by DV8? Below are the aspects in a RefBot report.

1. *Quality Attributes, Design Metrics, and Security Metrics* - These are metrics (per file or per set of files) given as a floating point number. They are founded on the work of [1].
2. *TQI Grade* - This is a grade relative to other projects in the category.
3. *Code Smells* - These are indicators that something may be wrong on the larger scale. They run counter to industry best practices. RefBot is algorithmically detecting a number of these smells.
4. *Table of Classes* - The report gives us a table of classes. The columns are the metrics given above and code smells, as well as "Bug Likelihood" and "Is Critical". I'm not sure what these are.
5. *Table of Solutions* - A table of recommend solutions in order to refactor the project. Each solution is assigned a cluster.

A *solution* is a list of *actions*. A solution is found using an optimization algorithm. Maybe the files involved in a solution overlap with DV8's flaws or roots?

RefBot has some notion of *cluster centers* that I cannot seem to find more about. Peraphs this overlaps with DV8's findings?

## References

[1] [A hierarchical model for object-oriented design quality assessment](https://ieeexplore.ieee.org/document/979986)

[2] RefBot: Intelligent Software Refactoring Bot

[3] Experiences Applying Automated Architecture Analysis Tool Suites