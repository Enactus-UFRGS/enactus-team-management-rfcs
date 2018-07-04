- Start Date: 19/06/2018
- RFC PR:


# Summary

Here we will discuss the architecture for the first version of the Enactus Team Management System.
This involves which features will be developed and how they will be modeled and developed

# Motivation

We want the Enactus Team Management System to be an open source solution for Enactus teams and an opportunity of learning
to any Enactus developer. The first opportunity we see is to provide our first developers
the chance to elaborate a good and well thought architecture for the first version of the software
seeking a great code quality application.

Thinking about the challenges of a Enactus Team we see that managing members, projects and activities is
one of the hardest. Every team must collect the worked hours of its members and the project activities to
provide those informations for their national Enactus organization so that the team is able to take part on
the national championship and project notices.

That's why the first set of features will be focused on enabling team members to register their activities
in each project or team and providing usefull reports for the team leaders.

Here's what we want without much detail:

* A member must be able to register his activities including
    * A description of the activity
    * The duration of the activity
    * For which project or team the activity has been done
* A team/project leader must be able to see reports of
    * A members activities
    * A projects/teams activities


# Detailed design

## Functional Requirements

### Register projects/teams
The team leader must be able to create projects/teams. Each project/team must contain

* `name`
* `description`
* `members`

### Register activities
A member must be able to register his activities. Each activity must have

* `startedAt`
* `finishedAt`
* `name`
* `description`
* `members`
* `project`/`team`

A member can add other members to his activities, so that the activity hours
are counted for them too.

### Member monthly hours report
A member can generate a report of the hours he worked during the desired month.


# Drawbacks

Yet to be discussed

# Alternatives

Yet to be discussed

# Adoption strategy

yet to be discussed

# Unresolved questions

yet to be discussed 