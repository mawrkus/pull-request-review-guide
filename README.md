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
  + [Be respectful / Ask - Explain - Suggest](#be-respectful--ask---explain---suggest)
  + [Stop the "reply" hemorrhage / Offer to talk in person](#stop-the-reply-hemorrhage--offer-to-talk-in-person)
  + [Offer encouragement & appreciation / Give positive feedback](#offer-encouragement--appreciation--give-positive-feedback)
  + [Agree on a coding style / Automate](#agree-on-a-coding-style--automate)

2. For the authors
  + [And the first reviewer is... you! / Assess your code](#and-the-first-reviewer-is-you--assess-your-code)
  + [Be proactive / Provide context](#be-proactive--provide-context)
  + [Wait for the green light](#wait-for-the-green-light)
  + [Choose your audience](#choose-your-audience)
  + [Choose the right number of reviewers](#choose-the-right-number-of-reviewers)
  + [Keep it small / Divide and conquer](#keep-it-small--divide-and-conquer)
  + [Rome wasn't built in a day / Create new tasks](#rome-wasnt-built-in-a-day--create-new-tasks)
  + [Don't take it personally / Keep an open mind](#dont-take-it-personally--keep-an-open-mind)
  + [Clarify the code first / Help future developers](#clarify-the-code-first--help-future-developers)
  + [Leave this world a little better than you found it / The boy scout rule](#leave-this-world-a-little-better-than-you-found-it--the-boy-scout-rule)
  + [Answer all comments / Write the end of the story](#answer-all-comments--write-the-end-of-the-story)
  + [Practice mindfulness / Love](#practice-mindfulness--love)

3. For the reviewers
  + [Empathize / The other person is you](#empathize--the-other-person-is-you)
  + [Avoid selective ownership / It's our code!](#avoid-selective-ownership--its-our-code)
  + [Provide references](#provide-references)
  + [Seek the author's perspective / We always learn](#seek-the-authors-perspective--we-always-learn)
  + [Don't be a gatekeeper / Improvements have a threshold](#dont-be-a-gatekeeper--improvements-have-a-threshold)
  + [Ensure the best review quality](#ensure-the-best-review-quality)
  + [What to look for](#what-to-look-for)
  + [Practice mindfulness / Gratitude](#practice-mindfulness--gratitude)

4. [Interactions](#-interactions)

5. [Profiles](#-profiles)

6. [Resources](#-resources)

### 🤝 For both authors and reviewers

#### Be respectful / Ask - Explain - Suggest

Always be considerate and respectful, specifically:

- don't use the imperative
- don't judge
- don't blame (don't even think about cursing)
- don't be arrogant
- don't use sarcasm.

Instead:

- ask questions, assuming that everyone is intelligent and well-meaning
- explain your point of view in an explicit manner, even if it's a bit more verbose
- suggest.

Respect and humility remove all frictions. Clarity dispels all doubts about your intentions. Suggesting creates the conditions for improvement.

At the end, the goal is to have better, more meaningful conversations and to save time and energy.

• [Go to top](#-guidelines) •

#### Stop the "reply" hemorrhage / Offer to talk in person

Many replies to a comment might be the symptom of miscommunication, misunderstanding or lack of knowledge. They can create a lot of noise for everyone participating in the review, as well as frustration.

Should it be the case, offer to talk in person to clarify the topic under discussion, to agree on a solution and/or to pair on any changes suggested.

Once done, post a concise comment to summarize the conversation and to share the agreement with everyone.

• [Go to top](#-guidelines) •

#### Offer encouragement & appreciation / Give positive feedback

Code reviews often just focus on mistakes, but they should also offer encouragement and appreciation for good practices.

Whether you learned something thanks to a comment written by one of your peers, or when you read an elegant piece of code, or even just to congratulate the good work, say: "thank you!", "great!", "nice!".

It makes a huge difference to receive positive feedback!

• [Go to top](#-guidelines) •

#### Agree on a coding style / Automate

 Conversations about coding style are often long and unproductive. After all, it's a matter of personal taste and everyone has their own preference.

 This is why it's important to find a coding style that your team can adhere to and to use automation tools to ensure that it is being followed (code formatters, linters). By removing the personal tastes from the review, everyone can focus on what's most important: code quality and best practices.

 • [Go to top](#-guidelines) •

### 🖋️ For the authors

#### And the first reviewer is... you! / Assess your code

After creating the pull request (PR) and before inviting anyone, take some time to assess your own code. Reviewing your changes outside of your IDE could help you spotting inconsistencies, mistakes, missing parts, or even finding easier ways to solve the problem at hand.

• [Go to top](#-guidelines) •

#### Be proactive / Provide context

If the PR is complex, write a general comment to explain its purpose, to give an overview of the changes being made and to share any relevant information about your choices. It will help your reviewers to dive in the review without effort, which will surely result in less comments and a faster review.

If there are many changes, highlight the most important parts.

• [Go to top](#-guidelines) •

#### Wait for the green light

Save time for everyone: if your CI/CD pipeline has a test stage, wait until all tests have passed before inviting anyone to the review. You don't want the first comment to be "The build is failing :/".

• [Go to top](#-guidelines) •

#### Choose your audience

Take some time to choose your reviewers. Prior to inviting them, ask yourself:

- Who should I give visibility of the changes being made? Who could be impacted by those changes?
- Who has time to review my code?
- Who is qualified to give me the best feedback?

• [Go to top](#-guidelines) •

#### Choose the right number of reviewers

Be inclusive, but not too much. Having a large number of reviewers might lead to:

- too many comments/suggestions going into too many different directions
- too few comments, when everyone thinks someone will take care of the review.

To prevent this, you can start with a few core reviewers to receive the main feedback, then add more people, to give them visibility.

• [Go to top](#-guidelines) •

#### Keep it small / Divide and conquer

Small successive PRs, each one focused on a single change, will be reviewed more quickly and more thoroughly.

Try to organize your work in order to be able to break a complex task into a succession of simpler ones. Value your reviewers time, they will thank you and you will benefit of a faster and more valuable feedback.

> 10 lines of code = 10 issues.
>
> 500 lines of code = "looks fine."
>
> Code reviews.

(https://twitter.com/iamdevloper/status/397664295875805184)

• [Go to top](#-guidelines) •

#### Rome wasn't built in a day / Create new tasks

If the need for a big refactoring or substantial changes arise during the review, create a new task and add a link to it in the review.

Remember that, the longer a review takes:
- the bigger the number of changes
- the higher the risks of merge conflicts
- the greater the probability of demotivating everyone involved in the review.

• [Go to top](#-guidelines) •

#### Don't take it personally / Keep an open mind

One of the goals of a code review is to maintain the quality of the code base. When a reviewer provides a critique of your code, think of it as their attempt to help you, rather than as a personal attack on you or your abilities.

If you feel offended, ask for explanations before reacting, take some distance, assume the best intention from the reviewer and try to evaluate your code critically, as if someone else had written it.

Always keep in mind that it's not about you, it's about a better code, a better project built with your colleagues.

• [Go to top](#-guidelines) •

#### Clarify the code first / Help future developers

If a reviewer says that they don't understand something in your code, your first response should be to clarify the code itself. If the code can't be clarified, add a code comment that explains why the code is there. If a comment seems pointless, only then should your response be an explanation in the code review.

If a reviewer doesn't understand some piece of your code, other future readers likely won't understand it either. Writing a response in the code review doesn't help future code readers, but clarifying your code or adding code comments does help them.

• [Go to top](#-guidelines) •

#### Leave this world a little better than you found it / The boy scout rule

Opening a PR is a chance to improve the existing code base: have you noticed a missing test? A method that is too long? Some naming inconsistencies?

You don't have to make a big change or to make the code looks perfect,  just a little bit better than before!

If you find a mess, try to clean it up regardless of who might have made it. By doing this, you intentionally improve the code base for all the developers, helping the project to get better and better as it evolves.

• [Go to top](#-guidelines) •

#### Answer all comments / Write the end of the story

Before closing the review, answer all the comments. Not only as matter of respect for you reviewers (after all, they are spending time and energy as well) but also because a review is a dialogue and, as such, it should have clear a conclusion.

Moreover, it can be helpful as a reference in the future.

• [Go to top](#-guidelines) •

#### Practice mindfulness / Love

Take a few deep breaths... Repeat a mantra that is focused on gratitude and kind speech, for instance:

> Code can travel thousands of miles and affect many people.
>
> I vow to write code mindfully and lovingly.
>
> May this code create mutual understanding and peace.

Find your own mantras and spread the love!

### 👓 For the reviewers

#### Empathize / The other person is you

Always consider the potential impact of your words, not just their original intent. Ask yourself how you would react to the words you're about to post. Take some time to write comments that are not only helpful but also kind, the other person is you ;)

• [Go to top](#-guidelines) •

#### Avoid selective ownership / It's our code!

Instead of using words like: "your", "mine", "not mine", which could be interpreted as finger-pointing, prefer the more inclusive "our" and "we" ones.

Rephrase any comment to be more collaborative, showing that you share ownership of the code being modified.

• [Go to top](#-guidelines) •

#### Provide references

Don't assume that the author knows exactly what you are talking about. To support your comment/suggestion, add:

- a code sample
- a link to relevant documentation
- a link to a previous review
- a link to a blog post on the topic
- a link to a GitHub repository.

Sharing some references can also benefit the other reviewers.

• [Go to top](#-guidelines) •

#### Seek the author's perspective / We always learn

If something bothers you in the code you're reviewing, try to understand the reasons behind the author's choices.

Keep in mind that, often, the author is closer to the code than you are, and so they might really have a better insight about certain aspects of it.

• [Go to top](#-guidelines) •

#### Don't be a gatekeeper / Improvements have a threshold

Do we always need to push "perfect" code to production? Maybe a good increment in quality is enough?

Don't place the author in a never-ending cycle of requests for changes. Instead, try to strike a balance between code quality, performance, and developer happiness.

Remember that you are in the review to provide feedback, not to be a gatekeeper.

• [Go to top](#-guidelines) •

#### Ensure the best review quality

If don’t feel qualified to do some part of the review, don't hesitate to invite a developer who you think is qualified. Ensure that the best possible feedback is always given to the author.

• [Go to top](#-guidelines) •

#### What to look for

In general, examine every line of code and make sure you understand what all the code is doing. In particular, take into consideration these specific points:

- **Design:** Do the interactions of the various pieces of code make sense? Does this change integrate well with the rest of the code base? Is now a good time to add this functionality?
- **Functionality:** Does this code do what the author intended? Is what the author intended good for the users of this code (end-users AND developers)?
- **Complexity:** Can the code be understood quickly? Will developers be likely to introduce bugs when they try to call or modify this code? Is it over-engineered? Is it trying to solve a problem that the author speculates might need to be solved in the future instead of solving the problem they know needs to be solved now?
- **Tests:** Does the code have appropriate unit tests? Are they correct, sensible and useful? [Review them first](https://github.com/mawrkus/js-unit-testing-guide#-review-test-code-first), they will help you understand the intent of the author very quickly (could be just by looking at their names).
- **Naming:** Did the author pick good names for everything? Long enough to fully communicate what the item is or does, without being so long that it becomes hard to read?
- **Comments:** Did the author wrote clear and useful comments? Do they explain the "why?" or the "what" instead of the "how"?
- **Consistency:** Does the code follow the existing agreements about style, naming, files organization, etc.?
- **Documentation:** If the code changes how users build, test, interact with, or release code, check that the relevant documentation is also updated, deleted or added.

• [Go to top](#-guidelines) •

#### Practice mindfulness / Gratitude

Take a few deep breaths... Repeat a mantra that is focused on gratitude and kind speech, for instance:

> Reviewing this code,
>
> I am grateful to those that wrote it
>
> and for the tools that were used to write it.
>
> May this code bring health, peace, and well-being.

Find your own mantras and spread the love!

• [Go to top](#-guidelines) •

## 📔 Interactions

In the following interactions, can you spot which guideline applies?

### 1

> Alan:
> Please don't do this, you are actually creating a layer that the application does not require, and don't say that is temporary, because it isn't.
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
> Jamie:
> Do you know why?

### 5

> Evan:
> Do you want to keep this line?

### 6

> Alan:
> It's not consistent this tracking, because it directly depends on the provided options.
>
> Billy:
> Ok, what do you suggest we should do instead?

### 7

> Alan:
> I can imagine why you are putting this fix here now, but our mission is to make the templates simpler, and the only way to accomplish that is to move all the business logic related to the page to the model.
> It's a bit more complicated, but this is the way that we need to follow now. There are many benefits of doing that, and one of them is to have tests.
> If you need some help about it, drop me a message.

• [Go to top](#-guidelines) •

## 📔 Profiles

- The terrorist: destroys every piece of code one by one.
- The picky: will approve the PR with great difficulty, because there's always a little something to improve.
- The bot: will always approve the PR without any comment. For some, their best friend, for others, the most annoying reviewer.
- The vague: can be found by following the trail of "What do you mean?" comments.
- The bull: answers comments by committing new changes.
- The ghost: was in the PR, or not. Have you seen them?
- The purist: does not live in a world of trade-offs and concessions. Do they even create PRs?
- The novelist: loves to explain in great lengths the history, the context and all the nuances that you should definitely know before merging the PR.

• [Go to top](#-guidelines) •

## 📔 Resources

- "The Art of Giving and Receiving Code Reviews (Gracefully)": http://www.alexandra-hill.com/2018/06/25/the-art-of-giving-and-receiving-code-reviews/
- "How to Make Your Code Reviewer Fall in Love with You": https://mtlynch.io/code-review-love
- "8 Causes of Miscommunication and Misunderstanding" https://www.userlike.com/en/blog/causes-of-miscommunication
- "A guide for reviewing code and having your code reviewed": https://github.com/thoughtbot/guides/tree/master/code-review
- "A practical guide for conducting efficient code reviews": https://www.heartinternet.uk/blog/a-practical-guide-for-conducting-efficient-code-reviews/
- "Code Reviews: Just Do It": https://blog.codinghorror.com/code-reviews-just-do-it/
- "How to Do Code Reviews Like a Human (Part One)": https://mtlynch.io/human-code-reviews-1/
feedback-ladders-how-we-encode-code-reviews-at-netlify/
- "Google's Code Review Developer Guide": https://google.github.io/eng-practices/review/
- "Best Practices for Peer Code Review ": https://www.kessler.de/prd/smartbear/BestPracticesForPeerCodeReview.pdf
- "Conventional comments (comments that are easy to grok and grep)": https://conventionalcomments.org
- "Feedback Ladders: How We Encode Code Reviews at Netlify": https://www.netlify.com/blog/2020/03/05/
- "Mindful Code Exercises": https://dev.to/kev_mcg/mindful-code-exercises

• [Go to top](#-guidelines) •
