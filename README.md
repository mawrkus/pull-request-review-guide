# A practical guide for better, faster code reviews

> "A code review is a dialogue, but it is also a critique of a person’s work, and both reviewer and author should bear in mind the psychology of ownership and criticism. Some of the most valuable things that come up during code review are things which different developers can reasonably disagree about, and discussing such things is exactly how we learn and innovate." -- Alexandra Hill, The Art of Giving and Receiving Code Reviews (Gracefully)

## 📔 Considerations

- A code review is a dialogue, and as such, it should always be done in a respectful and constructive way. We are humans, not machines.
- A code review is a tool for learning and improvement, for both authors and reviewers.
- Practically speaking, the purpose of code review should be to ensure that the quality standards agreed with your peers are met.

## 📔 Guidelines

### 🤝 For both authors and reviewers

#### Explain why, be explicit / Avoid ambiguity and vagueness

When you suggest something, explain why. Having a clear understanding of why you made this suggestion will help having better, more meaningful conversations and will save a lot of time.

Remember that, even if your suggestion seems straightforward, it might be interpreted by the author in a very different way. Take some time to fully explain your idea in an explicit manner, even if it's a bit more verbose. Clarity dissipes all doubts.

#### Stop the "reply" hemorragy / Don't write a novel

Many replies to a comment might be the symptom of miscommunication/misunderstanding. This usually creates noise for everyone involved in the review. Should it be the case, schedule a quick face to face meeting with your peer to clarify the topic under discussion.

Once discussed, add a concise comment to share the agreement with everyone involved in the review.

#### Give positive feedback / Recognize the work

Whether you learn something thanks to one of your peer's comment or you were invited to a review that fixes an issue no one wanted to fix, or just to congratulate the good work, just say: "thank you!", it makes a huge difference to receive positive feedback.

### 🖋️ For the authors

#### Be proactive / Help the reviewers

If the PR is complex, write a general comment to explain its purpose, to give an overview of the changes being made and to share any relevant information about your choices. It will help the reviewers dive in the review without much effort, which will certainly result in less comments and a faster review.

If there are many changes, highlight the most important parts.

#### Don't take it personnally / Take some distance

There's a difference between who you are and what you do. What you do can always be improved. Constructive and respectful criticism can always help. If you feel hurt by a comment, take some distance and try to keep in mind that it's not about a better version of you, it's about a better software craft.

#### Choose the right number of reviewers

Having the right number of reviewers can prevent:

- too many comments and/or too many suggestions going into too many different directions,
- too few comments, when everyone thinks someone will take care of writing comments.

You could start with a few core reviewers and when everything has been reviewd proprly, you could add more reviewers to give them visibility.

### 👓 For the reviewers

#### Empathize / The other person is you

Always consider the potential impact of your words, not just their original intent. Take some time to write comments that are not only helpful but also kind.

#### Be respectful / Use appropriate phrasing

A bit of psychology cannot hurt, specifically:

- don't use the imperative,
- don't curse,
- don't be sarcastic.

Instead, you can:

- ask questions,
- suggest,
- encourage.

#### Help the author / Don't blame (their choices)

Writing Software is a discovery process, in the sense that we try to figure out the problem at hands and how to solve it in the best way.

As we all have different levels of experience and expertise, it's natural that some of us will suggest "better" solutions than others.

Try to understand the reasons behind their choices, not to blame them, you might also learn something in the process!

Eventually, this is your personal responsibility to use your own experience and expertise to help the authors. We are humans, not machines. Be kind.

### Provide code samples / Provide references

Don't assume the author knows exactly what you are talking about. When necessary, consider adding:

- a code sample,
- a link to relevant documentation,
- a link to a previous review,
- a link to a blog post on the topic,
- a link to a GitHub repository.

This will provide a nice support to your comment/suggestion and will certainly benefit all the persons participating in the review.

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

### To check

- https://thoughtbot.com/blog/five-tips-for-more-helpful-code-reviews
- https://github.com/thoughtbot/guides/tree/master/code-review
- "A practical guide for conducting efficient code reviews": https://www.heartinternet.uk/blog/a-practical-guide-for-conducting-efficient-code-reviews/
- "Code Review Developer Guide": https://google.github.io/eng-practices/review/
- "Code Reviews: Just Do It": https://blog.codinghorror.com/code-reviews-just-do-it/
- "How to Do Code Reviews Like a Human (Part One)": https://mtlynch.io/human-code-reviews-1/
- "Code Review — The Ultimate Guide": https://www.freecodecamp.org/news/code-review-the-ultimate-guide-aa45c358bbf5/
