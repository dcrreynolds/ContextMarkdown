# ContextMarkdown

## The problem

As a lead for a development team I found myself following a documentation pattern made up mostly of toil.

I would write a doc for a new feature or idea and need to be able to describe it to 3 distinct groups:

- **Other developers:** Interested in implementation details and generally only curious about *why* something is important to the business
- **Project mangers:** Slightly interested in the implementation details, but mainly interested in risk, cost, and time
- **Company Leadership** Not interested in implementation details (at all), mostly interested in the the *why* and impact

Writing about the same thing in 3 different style is a nuisance, but it is important to the success of the feature that everybody is on board. So, you make 3 different types of docs and have 3 different types of conversations. The information flow looks a little like this:

(Insert a venn diagram here)

Where this gets really cumbersome is updates. As all 3 groups review the feature, make adjustments, and generally improve on the base idea you find you need to continually check and probably update multiple documents. In most organizations these documents are often forked into new documents adding an ever growing pile of slightly off, old, and OBE changes to the feature. In short, its plagued by a few issues:

1. Updating documentation takes more effort than it should
1. This leads to documentation sprawl and causes even small organizations to become out of sync
1. This contributes to worse products that take too long and cost to much

So, what can we do about it?

## Context aware documentation

The struggle above is about context, we are all talking about the same thing. The only thing that differs is how we care about individual pieces of information.

The repo exist as an experiment to answer the question, if we can keep all needed context in the same document and allow for simple block based filtering is this problem improved?

### How it works

Most documents like this one are made up of several blocks of content nested in a tree structure. Elements like an H1 header are containers of text and/or other blocks like lower level headers, images, tables, list, ect. Context tags can be applied at any block of a document to include or exclude that block in the context specific view of the document with that context being inherited in the tree.

Some basic rules:

- Untagged blocks are always included
- The most specific context tag wins
- Blocks can have multiple contexts included or excluded
- Blocks that are only configured to include a context will only be shown in that context
- Context exclusion will be chosen over context inclusion if both tags are present

This will allow us the flexibility

- Write a single or set of documents once that include all the information needed
- Make it easier to make changes in a single place
- Still allow target audiences to only see the information they care about

## Future Exploration

- Build this idea as an extension of popular and existing documentation tools

## Other use cases

- Sales pitches that change from customer to customer
- (expand here a lot more)
