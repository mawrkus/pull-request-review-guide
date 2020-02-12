# Guidelines for better, faster pull request review

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

#### Stop the "reply" hemorragy

The need for face to face conversation increases with the number of replies to a comment.
If it's the case, schedule a quick meeting with your peer instead of writing a novel in the PR that will create noise for everyone.

Once discussed, add a concise comment to share the agreement with the everyone.

### For the authors

#### Be proactive

If the PR is complex, write a general comment to give an overview of the context and the choices being made.

If there's a lot changes (e.g. a refactoring task), hightlight the most important parts of the code.

### For the reviewers

#### Empathize

Writing Software is a discovery process, in the sense that we try to figure out the problem at hands and how to solve it in the best way.

As we all have different levels of experience and expertise, it's natural that some of us will suggest "better" solutions than others.

This is your personal responsibility to use your own experience and expertise to help the authors, not to blame them. We are humans, not machines. Be kind.

#### Use appropriate phrasing

A bit of psychology cannot hurt: don't use the imperative, don't curse, don't impose. Suggest, ask questions and if you suggest something better, explain why you think it's better.

## Resources

- "The Art of Giving and Receiving Code Reviews (Gracefully)": http://www.alexandra-hill.com/2018/06/25/the-art-of-giving-and-receiving-code-reviews/

### To check

- "Code Review Developer Guide": https://google.github.io/eng-practices/review/
- "Code Reviews: Just Do It": https://blog.codinghorror.com/code-reviews-just-do-it/
- "How to Do Code Reviews Like a Human (Part One)": https://mtlynch.io/human-code-reviews-1/
- "Code Review — The Ultimate Guide": https://www.freecodecamp.org/news/code-review-the-ultimate-guide-aa45c358bbf5/
