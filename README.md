# Sizing stories

*Or, things that complicate delivery*

Don't think about how long the task will take, but rather how complex the task is. Some things which increase complexity:

- Design needed
- Configuration
- Multiple programming languages
- New library or framework
- Number of files to edit
- Number of modules
- Changes to how data is stored 
    - Database migration
    - Change in values shared in a networked cache
- Tests
- Multiple disciplines (Frontend, Backend, Platform, Data)
- Requires coordinated deploys
- Requires service interruption to deploy
- Changes how we deploy
- Documentation

## Rubric 

This was developed to "size" stories with Agile-esque points, but should be helpful even if your process is less formal.
Agile points are completely imaginary and specific to a team. You may want to use different numbers, or t-shirt sizes, or something else.

It may seem surprising to consider one CSS change to be 1/3 of a new feature. But, consider the constant drag that applies to almost any change.
Communicating what is needed, researching what you're going to do, then coding it, making sure it's what the customer or product owner wanted, 
committing, getting code review, making sure tests pass, etc. etc. This is not a measure of how long it takes to type.

*As always, use your common sense*

### 1 point

Looks like

- Trivial change
- No risk
- No risk of regression
- No tests

Examples

- Change one line of a config file
- Fix a simple CSS bug
- Copy change

### 2 points

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
 
### 3 points

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

### 5 points

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

### 8 points

Looks like

- It requires other teams to do work. 
- Research definitely required. Ambiguity, unknowns.
- Unfamiliar territory.
- Complex change that touches multiple services.

Examples
 
- A new page in the app with simple functionality.

A feature flag is required
 
### &gt; 8 points 

*Consider breaking it down, or doing a minimal prototype first?*

- A new service or feature
- Introducing or migrating to a new framework
- Something that changes how we have to deploy the service
