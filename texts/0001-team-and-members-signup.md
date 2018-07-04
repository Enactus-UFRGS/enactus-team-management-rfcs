- Start Date: 04/07/2018
- RFC PR: 
- Issue:

# Summary

As our first RFC we will discuss how Enactus Teams and members should be able
to signup to the Enactus Team Management System (ETMS)

# Motivation

It is important that Enactus teams and members are able to signup to this software
without too much bureaucracy.

At the same time we must ensure that not-Enactus teams and users signup and use this software.
At least not yet, since this software is being thought for Enactus teams only. 

# Detailed design

We want every Enactus team in the world to be able to signup and take advantage of the ETMS.
At the same time, we don't want not-Enactus teams and users signin-up to avoid possible servers overloads
and losing control over the application.

Here's what we want:

* A Enactus team must be able to signup
* A signup Enactus team should be verified before using the application
* A Enactus team must be able to add/remove members
* A Enactus team must be able to select a leader between its members
* Members should be able to signup to a Enactus Team
* Members should be able to signin to application and have access to their team information

# Drawbacks

Why should we *not* do this? Please consider:

- implementation cost, both in term of code size and complexity
- whether the proposed feature can be implemented in user space
- integration of this feature with other existing and planned features

There are tradeoffs to choosing any path. Attempt to identify them here.

# Alternatives

What other designs have been considered? What is the impact of not doing this?

# Adoption strategy

If we implement this proposal, how will existing developers adopt it? Is
this a breaking change? Can we write a codemod? Should we coordinate with
other projects or libraries?

# Unresolved questions

* How will Enactus teams be verified?
    * Every Enactus team has a Enactus Team ID registered to Enactus Worldwide. We could verify
    that.
* How will Enactus teams add members?
    * It can be done via link sent to the Enactus Team e-mail
* Who will be the first Enactus team leader?
    * Maybe the first user who enters the team?
    * Or maybe the user who signs the team up?
* How will the process of changing team leader be done?
    * The current leader `passes-the-flag` (selects) to the new leader?