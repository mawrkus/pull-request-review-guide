# A practical guide for better, faster code reviews

> "A code review is a dialogue, but it is also a critique of a person’s work, and both reviewer and author should bear in mind the psychology of ownership and criticism. Some of the most valuable things that come up during code review are things which different developers can reasonably disagree about, and discussing such things is exactly how we learn and innovate." -- Alexandra Hill, The Art of Giving and Receiving Code Reviews (Gracefully)

## Disclaimer

*All the information provided has been compiled & adapted from the references cited at the end of the document. The guidelines are illustrated by my own examples, fruit of my personal experience writing and reviewing code. Many thanks to all of the sources of information & contributors.*

## 📔 Considerations

- A code review is a dialogue, and as such, it should always be done in a respectful and constructive way.
- Many programming decisions are opinions. A code review opens a conversation about trade-offs in order to reach a resolution that everyone is satisfied with.
- A code review is a form of asynchronous communication, so a lot of context (like body language and the opportunity for back-and-forth) is lost.
- For both authors and reviewers, a code review is a collaborative tool for knowledge spreading and for code quality improvement.

## 📔 Guidelines

1. For both authors and reviewers
  + [Be respectful / Ask - Explain - Suggest](#)
  + [Stop the "reply" hemorragy / Offer to talk in person](#)
  + [Give positive feedback / Be grateful](#)
  + [Agree on a coding style / Automate](#)

2. For the authors
  + [And the first reviewer is... you / Assess your code](#)
  + [Be proactive / Provide context](#)
  + [Wait for the green light](#)
  + [Choose your audience](#)
  + [Choose the right number of reviewers](#)
  + [Keep it small / Divide and conquer](#)
  + [Rome wasn't built in a day / Create new tasks](#)
  + [Don't take it personally / Keep an open mind](#)
  + [Leave this world a little better than you found it / The boy scout rule](#)
  + [Answer all comments / Write the end of the story](#)

3. For the reviewers
  + [Empathize / The other person is you](#)
  + [Avoid selective ownership / It's ours](#)
  + [Provide references](#)
  + [Seek the author's perspective / We always learn](#)
  + [Don't be a gatekeeper / Improvements have a threshold](#)
  + [Ensure review quality](#)
  + [Ask for clarifications](#)
  + [What to look for](#)

4. [Interactions](#-interactions)

5. [Profiles](#-profiles)

6. [Resources](#-resources)

### 🤝 For both authors and reviewers

#### Be respectful / Ask - Explain - Suggest

Always be considerate and respectful, specifically:

- don't use the imperative,
- don't judge,
- don't blame (don't even think about cursing),
- don't be arrogant,
- don't use sarcasm.

Instead:

- ask questions, assuming that everyone is intelligent and well-meaning,
- explain your point of view in an explicit manner, even if it's a bit more verbose,
- suggest.

Respect and humility remove all frictions. Clarity dissipes all doubts about your intentions. Suggesting creates the conditions for improvement.

At the end, the goal is to have better, more meaningful conversations and saving time and energy.

• [Go top](#-guidelines) •

#### Stop the "reply" hemorragy / Offer to talk in person

Many replies to a comment might be the symptom of miscommunication, misunderstanding or lack of knowledge. They can create a lot of noise for everyone participating in the review, as well as frustration.

Should it be the case, offer to talk in person to clarify the topic under discussion, to agree on a solution and/or to pair on any changes suggested.

Once done, post a concise comment to summarize the conversation and to share the agreement with everyone.

• [Go top](#-guidelines) •

#### Give positive feedback / Be grateful

Whether you've just learned something thanks to one of your peers comment or you've just read an elegant line of code, or just to congratulate the good work, say: "thank you!", "great!", "nice!".

It makes a huge difference to receive positive feedback!

• [Go top](#-guidelines) •

#### Agree on a coding style / Automate

 Conversations about coding style can be long and unproductive. After all, it's a matter of personal taste and everyone has their own preference.

 This is why it's important to find a coding style that your team can adhere to and to use automation tools to ensure that it is being followed (code formatters, linters). By removing the personal tastes from the review, everyone can focus on what's most important: code quality and best practices.

 • [Go top](#-guidelines) •

### 🖋️ For the authors

#### And the first reviewer is... you / Assess your code

After creating the pull request (PR) and before inviting anyone, take some time to assess your own code. Reviewing your changes outside of your IDE could help you spotting inconstencies, mistakes, missing parts, or even finding easier ways to solve the problem at hand.

• [Go top](#-guidelines) •

#### Be proactive / Provide context

If the PR is complex, write a general comment to explain its purpose, to give an overview of the changes being made and to share any relevant information about your choices. It will help your reviewers to dive in the review without effort, which will surely result in less comments and a faster review.

If there are many changes, highlight the most important parts.

• [Go top](#-guidelines) •

#### Wait for the green light

Save time for everyone: if your CI/CD pipeline has a test stage, wait until all tests have passed before inviting ayone to the review. You don't want the first comment to be "The build is failing :/".

• [Go top](#-guidelines) •

#### Choose your audience

Take some time to choose your reviewers. Prior to inviting them, ask yourself:

- Who should I give visibility of the changes being made?
- Who has time to review my code?
- Who is qualified to give me the best feedback?

• [Go top](#-guidelines) •

#### Choose the right number of reviewers

Be inclusive, but not too much. Having a large number of reviewers could lead to:

- too many comments and/or too many suggestions going into too many different directions,
- too few comments, when everyone thinks someone will take care of reviewing.

To prevent this, you can start with a few core reviewers to receive the main feedback, then add more people, to give them visibility.

• [Go top](#-guidelines) •

#### Keep it small / Divide and conquer

Small successive PRs, each one focused on a single change can help having faster reviews. Always try to organize your work in order to be able to break a complex task into a succession of simpler ones. Your reviewers will thank you for not stealing all their time!

• [Go top](#-guidelines) •

#### Rome wasn't built in a day / Create new tasks

If the need for a big refactoring or substantial changes arise during the review, create directly a new task and add a link to it in the review.

Remember that, the longer a review takes, the more the changes, the higher are the risks for merge conflicts, and for a decrease in motivation for everyone participating in the review.

• [Go top](#-guidelines) •

#### Don't take it personally / Keep an open mind

If you receive negative feedback, take some distance, assume the best intention from the reviewer and try to evaluate your code critically, as if someone else had written it. Should you feel offended, ask for some explanations before reacting.

Always keep in mind that it's not about you, it's about a better code, a better project built with your colleagues, a better software craft.

• [Go top](#-guidelines) •

#### Leave this world a little better than you found it / The boy scout rule

Opening a PR is a chance to improve the existing code base: have you noticed a missing test? A method that is too long? Some naming inconsistencies?

You don't have to make a big change or to make the code looks perfect,  just a little bit better than before!

If you find a mess, try to clean it up regardless of who might have made it. By doing this, you intentionally improve the code base for all the developers, helping the project to get better and better as it evolves.

• [Go top](#-guidelines) •

#### Answer all comments / Write the end of the story

Before closing the review, answer all the comments. Not only as matter of respect for you reviewers (after all, they are spending time and energy as well) but also because a review is a conversation and, as such, it should have clear a conclusion.

• [Go top](#-guidelines) •

### 👓 For the reviewers

#### Empathize / The other person is you

Always consider the potential impact of your words, not just their original intent. Ask yourself how you would react to the words you're about to post. Take some time to write comments that are not only helpful but also kind, the other person is you ;)

• [Go top](#-guidelines) •

#### Avoid selective ownership / It's ours

Instead of using words like: "your", "mine", "not mine", which could be interpreted as finger-pointing, prefer the more inclusives "our" and "we".

Rephrase any comment to be more collaborative, showing that you share ownership of the code being modified.

• [Go top](#-guidelines) •

#### Provide references

Don't assume that the author knows exactly what you are talking about. To support your comment/suggestion, don't hesitate to add:

- a code sample,
- a link to relevant documentation,
- a link to a previous review,
- a link to a blog post on the topic,
- a link to a GitHub repository.

Sharing some references can also benefit the other reviewers.

• [Go top](#-guidelines) •

#### Seek the author's perspective / We always learn

If something bothers you in the code you're reviewing, try to understand the reasons behind the author's choices and assume they have already considered alternative implementations, you could learn something valuable in the process!

• [Go top](#-guidelines) •

#### Don't be a gatekeeper / Improvements have a threshold

Maybe we don't always need to push "perfect" code to production? Maybe a good increment in quality is enough?

Don't place the author in a never-ending cycle of requests for changes, instead, try to strike a balance between code quality, performance, and developer happiness.

Remember that you are in the review to provide feedback, not to be a gatekeeper.

• [Go top](#-guidelines) •

#### Ensure review quality

If don’t feel qualified to do some part of the review, don't hesitate to invite a peer who you think is qualified.

#### Ask for clarifications

If you can’t understand the code, it’s very likely that other developers won’t either. Ask the author to clarify it, this will also help future developers to understand it.

• [Go top](#-guidelines) •

#### What to look for

In general, examine every line of code and make sure to you understand what all the code is doing. In particular, take into considerations these specific points:

- **Design:** Do the interactions of the various pieces of code make sense? Does this change integrate well with the rest of the code base? Is now a good time to add this functionality?
- **Functionality:** Does this code do what the author intended? Is what the author intended good for the users of this code (end-users AND developers)?
- **Complexity:** Can the code be understood quickly? Will developers be likely to introduce bugs when they try to call or modify this code? Is it over-engineered? Is it trying to solve a problem that the author speculates might need to be solved in the future instead of solving the problem they know needs to be solved now?
- **Tests:** Does the code have appropriate unit tests? Are they correct, sensible and useful? Review them first, they will help you understand the intent of the author very quickly (could be just by looking at their names).
- **Naming:** Did the author pick good names for everything? Long enough to fully communicate what the item is or does, without being so long that it becomes hard to read?
- **Comments:** Did the author wrote clear and useful comments in understandable English? Do they explain the "why?" instead of the "what".
- **Consistency:** Does the code follow the existing agreements about style, naming, files organization, etc.?
- **Documentation:** If the code changes how users build, test, interact with, or release code, check that the relevant documentation is also updated, deleted or added.

## 📔 Interactions

### 1

> Alan:
> Please dont do this, you are actually creating a layer that the application does not require, and don't say that is temporary, because it isn't.
>
> Billy:
> I don't understand.
>
> Alan:
> That you don't need the copy-paste that you are doing.
>
> Billy:
> Let’s talk, your comment does not help me understand.

### 2

> Jamie:
> Do we really need this? I don’t see the gain.
>
> Billy:
> It’s a polyfill used in lazyLoad.js
>
> Jamie:
> Yes I got that, but why not importing there instead of here? I know that the import is not executed always in lazyload.js, but I see it weird.. Maybe a require() instead?
>
> Billy:
> Good point, I don’t know actually!
> I’ll make some tests.

### 3

> Alan:
> Maybe it is time to stop the tradition of providing all the arguments as props.

### 4

> Alan:
> I'm not sure if it's a good idea to return to this, it's a screenshot from project X.
>
> Billy:
> It’s not human-friendly indeed. But do we need human-friendly?
>
> Alan:
> Yes.
>
> Jamie
> Do you know why?

### 5

> Evan:
> Do you want to keep this line?

### 6

> Alan:
> It's not consistent this tracking, because it directly depends on the the provided options.
>
> Billy:
> Ok, what do you suggest we should do instead?

### 7

> Alan:
> I can imagine why you are putting this fix here now, but our mission is to make the templates simplier, and the only way to accomplish that is to move all the business logic related to the page to the model.
> It's a bit more complicated, but this is the way that we need to follow now. There are many benefits of doing that, and one of them is to have tests.
> If you need some help about it, drop me a message.

• [Go top](#-guidelines) •

## 📔 Profiles

- The terrorist: destroys every piece of code one by one.
- The picky: will approve the PR with great difficulty, because there's always a little something to improve.
- The bot: will always approve the PR without any comment. For some, their best friend, for others, the most annoying reviewer.
- The vague: can be found by following the trail of "What do you mean?" comments.
- The bull: answers comments by committing new changes.
- The ghost: was in the PR, or not. Have you seen him?
- The purist: does not live in a world of trade-offs and concessions.

• [Go top](#-guidelines) •

## 📔 Resources

- "The Art of Giving and Receiving Code Reviews (Gracefully)": http://www.alexandra-hill.com/2018/06/25/the-art-of-giving-and-receiving-code-reviews/
- "8 Causes of Miscommunication and Misunderstanding" https://www.userlike.com/en/blog/causes-of-miscommunication
- "A guide for reviewing code and having your code reviewed": https://github.com/thoughtbot/guides/tree/master/code-review
- "A practical guide for conducting efficient code reviews": https://www.heartinternet.uk/blog/a-practical-guide-for-conducting-efficient-code-reviews/
- "Feedback Ladders: How We Encode Code Reviews at Netlify": https://www.netlify.com/blog/2020/03/05/feedback-ladders-how-we-encode-code-reviews-at-netlify/
- "Google's Code Review Developer Guide": https://google.github.io/eng-practices/review/

• [Go top](#-guidelines) •

### To check

- "Code Reviews: Just Do It": https://blog.codinghorror.com/code-reviews-just-do-it/
- "How to Do Code Reviews Like a Human (Part One)": https://mtlynch.io/human-code-reviews-1/
- "Code Review — The Ultimate Guide": https://www.freecodecamp.org/news/code-review-the-ultimate-guide-aa45c358bbf5/
- "Best Practices for Peer Code Review ": https://www.kessler.de/prd/smartbear/BestPracticesForPeerCodeReview.pdf
- https://dev.to/jnschrag/10-lessons-learned-conducting-code-reviews-5di6
- https://www.ibm.com/developerworks/rational/library/11-proven-practices-for-peer-review/index.html
- https://www.processimpact.com/articles/humanizing_reviews.pdf
- https://www.smashingmagazine.com/2018/07/collaboration-designers-code-review-process/

- Again: http://www.alexandra-hill.com/2018/06/25/
