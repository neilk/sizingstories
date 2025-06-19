# Sizing development tasks

## *Or, how hard will it be to do that thing?*

![measure-measuring](https://github.com/neilk/sizingstories/assets/266804/f36f4f1a-bbf2-4453-a432-ae78a2861f8d)

As developers, we are often asked to shoot from the hip and estimate how long a thing will take. In your mind, you visualize the working code. You know you can blast out a pretty large program in no time. What could go wrong?

You probably _can_ blast out a prototype, even of a very large feature, very quickly! What's going to slow you down are all the interactions with (shudder) *other things*. Not to mention, making sure that what is coded is going to be useful to someone else. Sure, if you are working in a tiny shop with a couple of programmers, sizing tasks is less important. When you start working with bigger teams, or with other teams, it starts to become very important.

This is a checklist I made to help my team remember all the things that complicate delivery.

I've added sample "story points" and T-shirt sizes, but if you hate those methods, that's okay.

If you take away one thing from this guide: try not to guess how long the task will take; instead think about how complex the task is. Some things which increase complexity:

- Design needed
- Configuration
- Multiple programming languages
- New library or framework
- Number of files to edit
- Number of modules
- Changes to how data is stored
    - Especially when multiple programs access that data 
- Tests
- Multiple disciplines (Frontend, Backend, Platform, Data, Analytics)
- Requires coordinated deploys
- Requires service interruption to deploy
- Changes how we deploy
- Documentation

## Caveat

There are good arguments for not doing estimation at all.

We assume here that you've made the decision to use story points, 
or it's company policy where you work.

## Rubric 

I gave sample Agile points and t-shirt sizes, but they are of course just suggestions.

It may seem surprising to consider one CSS change to be 1/3 of a new feature. But, consider the constant drag that applies to almost any change.
Communicating what is needed, researching what you're going to do, then coding it, making sure it's what the customer or product owner wanted, 
committing, getting code review, making sure tests pass, etc. etc. This is not a measure of how long it takes to type.

*As always, use your common sense!*

### 1 point or Extra-Small (XS)

Looks like

- Trivial change
- No risk
- No risk of regression
- No tests

Examples

- Change one line of a config file
- Fix a simple CSS bug
- Copy change

### 2 points or Small (S)

Looks like

- Simple logic change to existing code. 
- No new class. 
- No new test. 
- No new behavior. 
- May have to edit a test. 
- One repo.

Examples

- Make straightforward changes to a couple of files in a programming language
- Write some extensive documentation
- Add a small feature and a test.
- A 1-pointer applied to many files

No feature flag required
 
### 3 points or Medium (M)

Looks like

- Introduces new logic. 
- New functions, new classes. 
- Requires new unit tests. 
- Focuses on single repo, but may impact other repos in a simple way. 
- No research required.
- "Multiple moving parts"
- "Changing with side effects"

Examples

- Database change / API change
- Simple changes to multiple repositories.
- Complex change to one repo.
- Adding new behavior to the frontend.
- Simple change that touches frontend and the backend (but consider making two stories)
 
Feature flag may be required

### 5 points or Large (L)

Looks like

- Research may be needed
- Nontrivial changes to multiple repos. 
- Many new unit tests. 
- May need behavioral tests (UI tests).
- May require input from other teams

Examples

- A simple change, but with a lot of impact on other services. Needs to be carefully tested.
- New nontrivial API method
- Data migrations required

A feature flag is almost certainly required

### 8 points or Extra-Large (XL)

Looks like

- It requires other teams to do work. 
- Research definitely required. Ambiguity, unknowns.
- Unfamiliar territory.
- Complex change that touches multiple services.

Examples
 
- A new page in the app with simple functionality.

A feature flag is required
 
### Anything bigger than that

*Don't make a task of this size! Break it down into multiple tasks, or do a minimal prototype first.*

- A new service or feature
- Introducing or migrating to a new framework
- Something that changes how we have to deploy the service
