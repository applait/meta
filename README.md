meta
====

Policies and decisions and workflows for Applait

Workflow
========

1. Pitching ideas
-----------------
 - For any new idea or suggestion, [create an issue](https://github.com/applait/meta/issues/new).
 - Label the issue as `proposal`.
 - Any discussion that are necessary on that idea go on in that issue thread.

2. Storing decisions
--------------------
 - Once an issue is accepted, put that up as a document in the repository with the final design decisions, maintaining a link to the issue(s) in which the decisions were taken.

Setting priorities through labels
=================================

The two labels `urgent` and `important` can be used to set the priority of an issue. The combination of these two tags on an issue would mean the following:

`urgent` | `important` | Interpretation
---------|-------------|-----------------
Yes      | Yes         | Really important. Do it right now!
Yes      | No          | Needs to be done quickly, but is not that significant from business perspective.
No       | Yes         | Significant from business perspective, but can be done later.
No       | No          | Take these up when you have nothing else to do.
