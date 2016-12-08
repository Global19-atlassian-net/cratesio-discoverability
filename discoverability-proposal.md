# Crates.io Discoverability Proposal

Work to be done by Integer 32, LLC before 2016-12-31

All initiatives are to be pursued in parallel and billed by actual hours worked. If an initiative is completed, remaining hours may be shifted to other initiatives.

## Initiative 1: Redesign of rust-lang.org and crates.io

    Goals: make information more organized and easily digestible, unify the design of rust-lang.org and crates.io

    Target to have the design work completed by 2016-12-31, not necessarily implementation

    Integer 32 to find a partner designer or design firm to do the UI/UX/IA redesign

    Since Integer 32 would be the eventual implementors of the design, and are also users of the sites, we would be available to answer questions and advise the designers.

    Integer 32 would help to coordinate the project and shepherd an RFC through if the core team decides to go that route.

## Initiative 2: Categorization on crates.io

    Goals: make it easier for Rust developers to find a crate that implements functionality they need for a particular topic

    Implementation assumed to be in the form of:

    A page on crates.io with links to each available category

    Each category's page would list the crates in that category, sorted by download count initially but to be sorted by the ranking decided by Initiative 4 eventually

    Some way for crate owners to manage categories of their crates

    Some way for administrators to manage available categories

## Initiative 3: Badges on crates.io

    Goals: make it easier for Rust developers to evaluate a particular crate's suitability for their use case based on attributes indicative of quality and stability

    Implementation assumed to be in the form of:

    An extensible framework for badges to be shown on a crate's page or on a page listing crates that will allow straightforward addition of new badges at a later time

    1-3 initial badges that could be automatically created without intervention needed from crate owners or crates.io administrators

    Number of badges depends on how complex the implementation of the badges chosen turns out to be

    Likely candidates for initial badges are: whether the crate is pre-1.0 or post-1.0, whether the crate builds on stable and/or nightly, travisci badges

## Initiative 4: RFC for crate rankings, possible implementation if time

    Goals: come to consensus with the community on a way of ranking crates within categories that makes the results useful for finding suitable candidate crates without being easily manipulated in such a way as to make the rankings less useful or unfair.

    The RFC will be in the context of having the categorization and badge work completed first

    If an agreement is reached on implementation details and there are hours left in this contract either from this or other initiatives, we will work on implementation.
