# A practical guide for better, faster code reviews

> "A code review is a dialogue, but it is also a critique of a person’s work, and both reviewer and author should bear in mind the psychology of ownership and criticism. Some of the most valuable things that come up during code review are things which different developers can reasonably disagree about, and discussing such things is exactly how we learn and innovate." -- Alexandra Hill, The Art of Giving and Receiving Code Reviews (Gracefully)

## 📔 Considerations

- A code review is a dialogue, and as such, it should always be done in a respectful and constructive way.
- Many programming decisions are opinions. A code review opens a conversation about tradeoffs in order to reach a resolution that everyone is satisfied with.
- For both authors and reviewers, a code review is a collaborative tool for knowledge spreading and for code quality improvement.

## 📔 Guidelines

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

#### Stop the "reply" hemorragy / Offer to talk in person

Many replies to a comment might be the symptom of miscommunication, misunderstanding or lack of knowledge. They can create a lot of noise for everyone participating in the review.

Should it be the case, offer to talk in person to clarify the topic under discussion, to agree on a solution and/or to pair on any changes suggested.

Once done, post a concise comment to summarize the conversation and to share the agreement with everyone.

#### Give positive feedback / Be grateful

Whether you've just learned something thanks to one of your peers comment or you've just read an elegant line of code, or just to congratulate the good work, say: "thank you!".

It makes a huge difference to receive positive feedback!

### 🖋️ For the authors

#### And the first reviewer is... you / Assess your code

After creating the pull request and before inviting anyone, take some time to assess your own code. Reviewing your changes outside of your IDE might help you spotting inconstencies, mistakes, missing parts, or even finding easier ways to solve the problem at hand.

#### Be proactive / Annotate

If the PR is complex, write a general comment to explain its purpose, to give an overview of the changes being made and to share any relevant information about your choices. It will help your reviewers to dive in the review without effort, which will surely result in less comments and a faster review.

If there are many changes, highlight the most important parts.

#### Choose your audience

Take some time to choose your reviewers. Prior to inviting them, ask yourself:

- Who should I give visibility of the changes being made?
- Who has time to review my code?
- Who could give me the best feedback?

#### Choose the right number of reviewers

Be inclusive, but not too much. Having a large number of reviewers could lead to:

- too many comments and/or too many suggestions going into too many different directions,
- too few comments, when everyone thinks someone will take care of reviewing.

To prevent this, you can start with a few core reviewers to receive the main feedback, then add more people, to give them visibility.

#### Keep it small / Divide and conquer

Small successive PRs, each one focused on a single change can help having faster reviews. Always try to organize your work in order to be able to break a complex task into a succession of simpler ones. Your reviewers will thank you for not stealing all their time!

#### Rome wasn't built in a day / Create new tasks

If the need for a big refactoring or substantial changes arise during the review, create directly a new task and add a link to it in the review.

Remember that, the longer a review takes, the more the changes, the higher are the risks for merge conflicts, and for a decrease in motivation for everyone participating in the review.

#### Don't take it personally / Take some distance

There's a difference between who you are and what you do. What you do can always be improved through constructive and respectful criticism.

If you feel hurt, take some distance, assume the best intention from the reviewer's comment and try to see it through their lens.

Always keep in mind that it's not about a better version of you, it's about a better software craft.

#### Answer all comments / Write the end of the story

Be sure to answer all the comments. Not only as matter of respect for you reviewers (after all, they are spending time and energy to help you) but also because a review is a conversation and, as such, it should have a conlusion.

### 👓 For the reviewers

#### Empathize / The other person is you

Always consider the potential impact of your words, not just their original intent. Ask yourself how you would react to the words you're about to post. Take some time to write comments that are not only helpful but also kind, the other person is you ;)

#### Avoid selective ownership / It's ours

Instead of using words like: "your", "mine", "not mine", prefer "our" and "we".

Rephrase any comment to be inclusive, showing that you share ownership of the code being modified.

#### Provide references

Don't assume that the author knows exactly what you are talking about, to support your comment/suggestion, don't hesitate to add:

- a code sample,
- a link to relevant documentation,
- a link to a previous review,
- a link to a blog post on the topic,
- a link to a GitHub repository.

Sharing some references might also benefit the other reviewers.

#### Don't be a gatekeeper / Improvements have a threshold

Maybe we don't always need to have "perfect" code pushed to production? Maybe a good increment in quality is enough?

Don't place the author in a never-ending cycle of requests for changes, instead, try to strike a balance between code quality, performance, and developer happiness.

Remember that you are in the review to provide feedback, not to be a gatekeeper.

#### Seek the author's perspective / We always learn

Writing software is a discovery process, in the sense that we try to figure out the problem at hand and how to solve it in the best way.

As we all have different levels of experience and expertise, it's natural that we end up suggesting different kinds of solutions. Some better than the others, some worse.

If something bothers you in the implementation you're reviewing, try to understand the reasons behind the author's choices, assume they have already considered alternative implementations, you might learn something valuable in the process!

#### Review test code first

Tests are mini use cases of the code that you can drill into. It will help you understand the intent of the author very quickly (could be just by looking at the names of the tests).

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

Missing: Ask - Explain Why - Suggest

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

Present: Ask - Explain Why - Suggest

### 3

> Alan:
> Maybe it is time to stop the tradition of providing all the arguments as props.

Missing: Ask - Explain Why - Suggest

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

Missing: Ask - Explain Why - Suggest

### 5

> Evan:
> Do you want to keep this line?

Missing: Explain Why - Suggest

## 📔 Profiles

- The terrorist
- The picky
- The "checked" bot
- The vague

## 📔 Resources

- "The Art of Giving and Receiving Code Reviews (Gracefully)": http://www.alexandra-hill.com/2018/06/25/the-art-of-giving-and-receiving-code-reviews/
- "8 Causes of Miscommunication and Misunderstanding" https://www.userlike.com/en/blog/causes-of-miscommunication
- "A guide for reviewing code and having your code reviewed": https://github.com/thoughtbot/guides/tree/master/code-review

### To check

- "A practical guide for conducting efficient code reviews": https://www.heartinternet.uk/blog/a-practical-guide-for-conducting-efficient-code-reviews/
- "Code Review Developer Guide": https://google.github.io/eng-practices/review/
- "Code Reviews: Just Do It": https://blog.codinghorror.com/code-reviews-just-do-it/
- "How to Do Code Reviews Like a Human (Part One)": https://mtlynch.io/human-code-reviews-1/
- "Code Review — The Ultimate Guide": https://www.freecodecamp.org/news/code-review-the-ultimate-guide-aa45c358bbf5/
- "Best Practices for Peer Code Review ": https://www.kessler.de/prd/smartbear/BestPracticesForPeerCodeReview.pdf

- Again: http://www.alexandra-hill.com/2018/06/25/
