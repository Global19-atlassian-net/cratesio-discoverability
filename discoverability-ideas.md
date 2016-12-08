# Discoverability ideas

Ideas gathered from:

* https://internals.rust-lang.org/t/proposal-the-rust-platform/3745
*    https://www.reddit.com/r/rust/comments/4uxdn8/the_rust_platform_aaron_turon/
*    https://internals.rust-lang.org/t/follow-up-the-rust-platform/3782
*    https://internals.rust-lang.org/t/crates-io-discoverability-and-engagement-starting-the-conversation/4053


## Categorization

*    Have a page listing categories like "Parsing", "Networking", "Serialization", "Debugging"
*    Clicking on a category takes you to a list of crates in that category that are then sorted by download count or some other criteria

### Examples

*    https://www.ruby-toolbox.com/
*     https://emberobserver.com/
*    https://djangopackages.org/

###    Questions

*    Who decides what categories we have? 
*   Does the crate owner pick the category or do curators pick the category?
*    Can we use the existing "keywords" for the categories?
*    What criteria do we sort by within a category?
*    Does this replace these sites, or could we use the info on these sites to bootstrap?
**    https://github.com/kud1ing/awesome-rust
**    https://rust.libhunt.com/
**    http://www.arewewebyet.org/

## Badges

Have various badges on a crate's page that would clearly signify various indicators of quality/stability/etc.

Ideas:

*    Whether it builds on latest stable or nightly or both or neither
*    What versions of stable rust each version of the crate builds on
*    Whether there is documentation and/or integration with docs.rs
*    Whether the crate has reached 1.0 with stability guarantees
* Existing travis-ci badges
*    Whether the crate's dependencies are up-to-date
*   Whether the crate is "official" (is in the rust-lang or rust-lang-nursery github org)
*    Number of reverse dependencies
*    Compatibility with other libraries
*    Cross-platform compatibility
*    a minimum level of API coverage
*    a README and Users Guide
*    unit tests
*    standalone sample code
*    integration tests
*    Explicit opt-out (not maintained, do not include in meta-packages, etc)
*    Presence of unsafe code
*    Percentage of code in unsafe blocks
*    Whether the crate contains a binary, a library, or both

###   Questions

*    Can these badges be automated? Or must the crate owner add them? Or must a curator add them?
*    Would these badges incentivize the behavior we want to see, or would they cause undesired effects?


## Improving search

*    Adding more options for sorting
*    Adding options for filtering
*    Include a rendered README on the main crates page that is searchable
*    Adding more metadata to use in sorting and filtering
  *    # of GitHub stars
  *    # of GitHub watchers
  *    # of GitHub forks
  *    # of GitHub open issues
  *    # of GitHub open PRs
  *    # of GitHub contributors
  *    Age of open issues/PRs
  *    Date of most recent release
  *    Date of first release
  *    Number of releases
  *    Votes
  *    Official-ness
  *    Evaluation score made by curators like ember observer
  *    Number of reverse dependencies
  *    Including a repository link, description, or documentation link ranks higher
  *    Any of the badges


## Meta-Packages

*    Give anyone the ability to create a meta-crate that coordinates multiple crates
*    Is there any reason why this isn't possible today?
*    Automatic integration testing of meta-packages when a new version of a crate in the package comes out; pin version if the tests don't pass

## Keywords on crates.io

*    Have a page that lists all keywords by their usage
*    Remove case sensitivity of keywords

## Guidance for crate authors

*    A "X% complete" bar on the crate page that guides authors to fill in any attributes that define a "good" crate


## Include pointers to crates in stdlib docs


>    So if we are going to embrace the discoverability, can we just ship some chosen 3rd-party documentations by default and do NOT ship the libraries themselves? The user will search for, say, HTTP library, and see that HTTP client is provided by a crate named hyper. The documentation would have large print directing the user to put some dependencies to Cargo.toml (we can do better by making cargo-edit a part of Cargo). We will still have to update the documentations from time to time (especially for major revisions), but it won't break any user experience.


## Distinguish between internal and external dependencies

* So that crates that want to work together only need to collaborate on their external dependencies. See https://github.com/rust-lang/cargo/issues/2064

## Community ratings on crates.io

* >    Let the community rate individual packages with lots of different metrics. "How good is the documentation: 4/5", "Overall quality: 3/5", "Ease of integration 2/5" and use semver actively to restrict search and age of review or other dates so that the rating is updated as the package is.

*    Allow community members to indicate they've audited the source of a particular version of a crate (are we rebuilding WoT at that point?)
