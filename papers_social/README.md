# [papers.social](http://papers.social) Design

Since work on the service has not even started, this document should change a
as it gets implemented.

## Concepts

- __AUTHOR__: A __USER__ that publishes a __PAPER__ in a __PAPER ARCHIVE__.
- __PAPER__: Singular publication __AUTHOR__'ed by one or more __USER__'s. Can
  be a traditional journal entry, conference paper, or any body of work that
  outlines and presents a novel discovery or innovation.
- __PAPER ARCHIVE__: A system that holds a collection of __PAPER__'s from a
  pre-print collection like [arXiv](https://arXiv.org), a peer-reviewed journal,
  or a similar venue.
- __SHARE__: A __USER__ that can _share_ __PAPER__'s they liked to __USER__'s
  that follow them.
- __USER__: These are the entities that will interact with the application.
  They can __AUTHOR__ __PAPER__'s, and __SHARE__ __PAPER__'s. An entity can
  entail an individual researcher, an organization, a team, or any other
  collection of individuals or entities capable of producing __PAPER__'s.
  A __USER__ can also __FOLLOW__ another __USER__ in order to view what they
  __AUTHOR__'ed, and __SHARE__'d.

## Plan for Implementation

Implementation would be done in phases. The first and exploratory phase would
help determine the best steps moving forward.

### Exploratory (First) Phase

1. Figure out the [__PAPER ARCHIVE__ Identity](#paper-archive-identity) dilemma
2. Implement an arXiv __PAPER ARCHIVE__ (Can maybe use RSS feeds for simpler API?)
3. Add __USER__'s and associate __PAPER__'s via __AUTHOR__'ship. Figure out a
   suitable authentication scheme.
4. Implement barebones sharing by only showing __SHARE__'s by __FOLLOW__'ed __USER__'s

Once some sort of initial system is created and deployed, feedback should be
collected. Reach out to individuals that may be interested as well.

## More Work Needed

### __PAPER ARCHIVE__ Identity

__PAPER ARCHIVE__'s should also be a type of __USER__.

Down the line, journals and venues can have a selection of __PAPER__'s they
publish, it would be beneficial for them to assign special _TAG_'s for specific
topics and special recognitions.

### Paper Discovery

Other than showing __PAPER__'s that were shared by __USER__'s someone follows,
it would be beneficial to also show __PAPER__'s that closely match a __USER__'s
interest.

Ideas:

- __PAPER__'s can have associated _TAG_'s. __USER__'s can follow _TAG_'s that
  are of interest.
- _TAG_'s can be "namespaced" (`user-name:tag-name`), so people can follow
  specific _TAG_'s of interest.
- Due to how many venues and publishing archives there are, and can be, there
  should be "global" tags for specific areas. These should be community defined
  and should can be designated some sort of "ownership" to a group of _USER_'s.
- If a __USER__ follow's a _TAG_, __PAPER__'s that have the most __SHARE__'s
  for each _TAG_ should be shown.
- This would open up possibilities of "gaming" the system to appear at the top,
  a naive "recommendation" algorithm may not suffice.

### Reviews and Comments

- A __USER__ can leave a _REVIEW_ for a __PAPER__ on potential improvements to
  their work.
- Figure out a way for an __AUTHOR__ to make a _RESPONSE_ to a _REVIEW_.
- Perhaps the _REVIEW_ + _RESPONSE_ flow should be done in [./../papers_forum/]
  in threads.
- Need a way for __AUTHOR__'s to _UPDATE_ the __PAPER__ after the review to
  allow for modifications to be made on a paper. Should list out changes made
  and also maintain history. The _FORUM_ should be able to track what threads
  were made before and after each version.
- __USER__'s should be incentivized to leave __REVIEW__'s.

### Privacy and Anonymity

Some users may want to publish witha pseudonym. Allowing fully anonymous
publication has some issues and cannot be done in a way that would aide the
mission of the service.

One thing that could be done is allowing temporarily anonymous _REVIEWS_ that
are revealed after some time has passed. This should be controlled by the __AUTHOR__'s
of the __PAPER__.
