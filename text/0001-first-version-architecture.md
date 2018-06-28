- Start Date: 19/06/2018
- RFC PR:


# Summary

Here we will discuss the architecture for the first version of the Enactus Team Management System.
This involves which features will be developed, which classes/models
will be added and how they relate to each other.

# Motivation

We want the Enactus Team Management System to be open source and an opportunity of learning
to any Enactus developer. The first opportunity we see is to provide our first developers
the chance to elaborate a good and well thought architecture for the first version of the software
seeking a great code quality application.


# Detailed design

## Functional Requirements

### Signup a team
A user must be able to signup his team by providing these informations
* `email`
* `university / institution`
* `enactus team ID`
* `name`

### Invite team members
After a team is successfully signed up, an e-mail must be sent to
the team's email containing a link to invite members.

On signup, each member must provide the following information

* `email`
* `password`
* `name`
* `documents` (`CPF` is required for certificates, `RG` is optional)

The team leader must be able to invite more members.

### Team leader
The first signed up member is temporarily the team leader. After other members
have signed, the current leader can choose another member to become the new leader

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