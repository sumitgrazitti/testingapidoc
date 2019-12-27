# Issue: Queries with Vertical Line (|)
I keep on seeing a lot of queries with a vertical line. What could be wrong?

## Context
A lot of the users are developers.

## Resolution
Ask your search users to refer to [Use Advanced Search](https://docs.searchunify.com/Content/End-User-Personalization/Use-Advanced-Search.htm). The article documents the proper use of search operators. The vertical line might be a valid OR operator in some implementations of search, but not in SearchUnify. The correct way is to prefix the search query with a hash and use two vertical lines.

## Causes
Nothing is wrong. It means that some of your search client users know how advanced search works in general. The vertical line (|) is a Boolean operator. Its value is OR. It is used in search queries where the user is of which keyword is more likely to bring them results. In such scenarios, they can use "lift | elevator" to fetch documents using "lift" and documents using "elevator." It is fast and it saves them from running multiple search queries.

## Related Docs
[Use Advanced Search](https://docs.searchunify.com/Content/End-User-Personalization/Use-Advanced-Search.htm)


## Tags
search engines, advanced search, search operators
