# Code Reviews

## Course Goals

* Describe the process of creating and submitting a pull request
* Explain what to look for when reviewing code

## Pull Requests

Code reviews are a tool to help to ensure a standard of quality for a code base, and are an opportunity for you to solicit feedback for the code you've written. Pull requests are the means we as developers use to submit code for review. In order to ensure that the pull request and code review process goes smoothly, you should adhere to some general guidelines for submitting code for review.

The pull request feedback cycle for first timers is usually longer than developers anticipate, because first pull requests almost always require a lot of feedback. There are some measures that you can take to reduce this feedback cycle.

### Length

Pull requests should be small. Small PRs mean faster turnaround time, less chance of a merge conflict, and less back and forth between the reviewer and submitter. When you are working on a project that involves production code, having smaller merge requests means that more code gets promoted to a production environment, more quickly.

### Title

PR titles should include the relevant ticket number and title, ie: *TODO-001 Display a list of tasks*. If tickets are small, or if the tickets tasks are effectively broken down, then the PRs should reflect that structure.

### Branch name

The branch name should model the ticket name ie: *todo-001-display-a-list-of-tasks*.

### PR description

What the description of the code review should contain varies from team to team, so check with your team to see what the norm is. It is generally better to be more descriptive than less, so as to help the reviewer understand what they should be looking for during the review.

A common template used for PR description is as follows:

#### Overview

What changed? This doesn't need to be overly technical, just plainly and concisely state the change this will introduce once merged.

Include why the change was made if the change was linked to a bug or special request or something not documented elsewhere. You can include the acceptance criteria for your story to satisfy this requirement.

#### Testing

All code submitted for review should be tested so that you ensure that you are only merging functional code into your . You should indicate how the changes were tested if that needs further description. Unit tests should be included in the code to review, but were there other tests not included in the code change? Did you do any manual testing for these changes?

#### Screenshots (optional)

If there is a UI change, screen shots should also be included.

### Commits

We learned about git maintenance in a previous section. Part of git maintenance includes maintaining a clean and clear commit history. Reviewers will look at your commit history and check for the following:

* Commits should be prepended by the ticket number ie: *TODO-001 Display a single task*, *TODO-001 Display multiple tasks*
* Commits should be in the imperative mood (**Fix a typo**, and not *Fixes a typo*, *Fixing a typo*, *Fixed a typo*)
* Commits should be concise
* Commits should follow convention
  * First word should be capitalized
  * Use plain English–don’t include uncommon abbreviations
  * Don’t add a period at the end
* Squash unnecessary commits

### Test coverage

All pull requests should include tests for the features that were added. All tests must be passing. You **never** should commit and push up broken code for a PR, because if it gets merged, that broken code will infect the main branch of your repository.

## Code Reviews

Code reviews should be thorough and prompt. Delivering quality code reviews is a skill that comes with practice and exposure. Being on a team with a developer that has experience with providing quality code reviews is the simplest way to level up your code reviewing skills, but if that is not an option, you can pay attention to these factors when reviewing a pull request:

* Functionality
* Testing
* Style
* Quality

### Functionality

* Does the code description adequately explain the effect that will take place if the code is merged?
* Does the code submitted line up with that expectation / does it work?

### Testing

* Are there unit tests included for each public method?
* Do the tests cover all logical scenarios?
* Does the PR include instructions for how to test?

### Style

* Do the UI changes look good?

### Quality

* Is the PR appropriately documented?
* Does the PR include information like screen shots and acceptance criteria?
* Is the code well-designed?
  * Does the code adhere to language norms?
  * Are the names used for functions, variables, objects, etc clear and concise?
  * Is there any unnecessary complexity? Is it easy to understand?
  * Does it include anything that is not stated in the description or ticket? In other words, are they adding anything that doesn't belong?
  * If there are comments, are they necessary and useful?
gi