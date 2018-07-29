- Start Date: 04/07/2018
- RFC PR: 
- Issue:

# Summary

As our first RFC we will discuss how Enactus Teams and members should be able
to signup and authenticate to the Enactus Team Management System (ETMS)

# Motivation

It is important that Enactus teams and members are able to signup to this software
without too much bureaucracy.

At the same time we must prevent not-Enactus teams and users from signing up and using this software.

We want every Enactus team in the world to be able to signup and take advantage of the ETMS.
At the same time, we don't want not-Enactus teams and users signing in/signing up to avoid possible
servers overloads and losing control over the use of the application.

Here's what we want:

* A Enactus team must be able to signup
* After signed up, an Enactus team must be validated (it must exist and be allowed to use the software)
* A Enactus team must be able to add/remove members
* Members should be able to signup to a Enactus Team
* Members should be able to signin to application

# Detailed design

User registration and authentication will work as most web applications.

![](https://drive.google.com/uc?id=1liI40EAh3DasfmtJYR_WdJdGiZeZtP9N)

1. The user enters his `e-mai` and `password`
    1. also `name` if registering
2. User clicks signin/signup button
3. User is authenticated into the application
    1. User must also be created if registering

After an user is authenticated he is redirected to his team page.
Each user belongs to only one team. Each team has one or more members (users).

![](https://drive.google.com/uc?id=12t3xptUzsERrXJmcGcYXIg60t708nnFJ)

If the users does not belong to a team yet he must either enter an existing team 
or create his Enactus team.

![](https://drive.google.com/uc?id=1lgNZTycusqWgTGQRxgOyjiAhzVt3JEyz)

When an user creates a team we must validate that it is a real Enactus team. We can do that by
verifying the Enactus Team ID with the National Enactus Organization. 

![](https://drive.google.com/uc?id=1pRRO-b-7DsPw_A8bqls8-pngwonKyIYv)

To create an Enactus team the user must provide:

* The Enactus Team name
    * generally in format `Enactus {{university name}}`
* Enactus Team ID
    * an unique ID provided by the National Enactus Organization to every team. It will be used
    to validate the team.

# Drawbacks

* The developers team are responsible for validating each created team with the National Enactus
Organization. In Brazil, for example, it the team will have to send the team name and Enactus Team ID
to Enactus Brazil for validation
* Foreign teams are not allowed to signup yet because there is no information about the team's country


# Alternatives

No alternatives have been thought yet.

# Adoption strategy

This is the very beginning of the ETMS application. These are the steps that we're going to take:
1. Implement user signup and authentitcation (signin)
    1. this will allow Enactus team members to signup and for the developers to collect some feedback
2. Implement team creation and entering
    1. we must deploy both features together to avoid Enactus teams being created multiple times
3. Small improvements and fixes
    1. after some feedback is collected we are going to tune our features to their best.

# Unresolved questions
