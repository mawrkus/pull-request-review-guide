# Guidelines for better, faster pull request review

- Pull request (PR) review is a learning process, for both authors AND reviewers.
- PR review must always be done in a respectful way: we are humans, not machines.

## Profiles

- The terrorist
- The picky
- The "checked" bot

## Examples

### 1

> Alan:
> Please dont do this, you are actually creating a layer that the application does not require, and don't say that is temporary, because it isn't
>
> Billy:
> I don't understand
>
> Alan:
> That you don't need the copy-paste that you are doing
>
> Billy:
> Let’s talk, your comment does not help me understand.

### 2

> James:
> Do we really need this? I don’t see the gain
>
> Billy:
> It’s a polyfill used in lazyLoad.js
>
> James:
> Yes I got that, but why not importing there instead of here… I know that the import is not executed always in lazyload.js, but I see it weird.. Maybe a require() instead?
>
> Billy:
> Good point, I don’t know actually!
> I’ll make some tests.

## Guidelines

### For both authors and reviewers

#### Explain why

When you suggest something, explain why, it will make clear for everyone to understand as they are not living in your head. Having a clear understanding of what you mean could help having better, more meaningful conversations and will save a lot of time.

Whenever possible, add a link to relevant documentation, GitHub repository, blog post, etc. to help understand your comment.

#### Stop the "reply" hemorragy

The need for face to face conversation increases with the number of replies to a comment.
If it's the case, schedule a quick meeting with your peer instead of writing a novel in the PR that will create noise for everyone.

Once discussed, add a concise comment to share the agreement with the everyone.

#### Give your thanks

Whether you learn something thanks to one of your peer's comments, or you were invited to a PR that fixes an issue that no one wanted to fix, or just because you want to congratulate your colleague's effort, just say: "thank you!", it's a big deal.

### For the authors

#### Be proactive

If the PR is complex, write a general comment to give an overview of the context, the prupose of the PR and relevant details about the choices being made.

If there's a lot changes (e.g. a refactoring task), hightlight the most important parts of the code.

### For the reviewers

#### Empathize

Writing Software is a discovery process, in the sense that we try to figure out the problem at hands and how to solve it in the best way. As we all have different levels of experience and expertise, it's natural that some of us will suggest "better" solutions than others.

Try to understand the reasons behind their choices, not blaming them, you might also learn something in the process!

Eventually, this is your personal responsibility to use your own experience and expertise to help the authors. We are humans, not machines. Be kind.

#### Use appropriate phrasing

A bit of psychology cannot hurt: don't use the imperative, don't curse, don't impose, don't be sarcastic. Ask questions, suggest, be kind, encourage.

#### Don't take it personnally

There's a difference between what you do and who you are. As a Software Craftsman, how you do what you do can always be improved, constructive and respectful criticism will usually help. But keep in mind that it's not about a better version of you, it's about a better craft.

## Resources

- "The Art of Giving and Receiving Code Reviews (Gracefully)": http://www.alexandra-hill.com/2018/06/25/the-art-of-giving-and-receiving-code-reviews/

### To check

- "Code Review Developer Guide": https://google.github.io/eng-practices/review/
- "Code Reviews: Just Do It": https://blog.codinghorror.com/code-reviews-just-do-it/
- "How to Do Code Reviews Like a Human (Part One)": https://mtlynch.io/human-code-reviews-1/
- "Code Review — The Ultimate Guide": https://www.freecodecamp.org/news/code-review-the-ultimate-guide-aa45c358bbf5/
