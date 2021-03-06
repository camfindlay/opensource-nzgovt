# 6. Social coding on GitHub

## 6.1 Organisation accounts for agencies

For agencies looking to maintain sharable code on GitHub, they should create an organisation account. For example, the
govt.nz website team have a GitHub organisation account as do many other [government agencies in New Zealand and around
the world](https://government.github.com/community/). Organisation accounts can have an unlimited number of public
projects associated with them, and an unlimited number of both public and undisclosed individual members with various
levels of permissions. These could include agency ICT staff, contractors or vendor staff accounts that are carrying out
work on the code on the agency's behalf. Contractors and government employees should use individual GitHub accounts to
commit code (rather than an agency account), respond to issues and pull requests just as they would on any other
project, or on any other social network. However to ensure records retention and that the commits come from an official
source (for instance to delineate commits of code in an official capacity versus commits in a personal capacity), the
account should be associated with a .govt.nz e-mail address. This provides a level of transparency and accountability,
and is a long-standing norm in the FOSS community. Almost without exception, all government agencies that have released
FOSS, both on GitHub and otherwise have followed this model.

## 6.2 Individual user accounts

If you don't yet have a GitHub account simply register for a new GitHub account using your .govt.nz e-mail address.
Follow the normal instructions to set up Git, setting your Git e-mail address as your .govt.nz address so that all code
commits are associated with your official account. If you already have a GitHub account:

1. Navigate to the [e-mail settings page](https://github.com/settings/emails) and add and confirm your .govt.nz e-mail
address.

2. Ensure that notifications for the organisation go to your .govt.nz account on the [notifications settings page]
(https://github.com/settings/notifications).

3. Create a new repository, or clone and navigate to your team's repository on your computer.

4. Configure the repository to use your .govt.nz account when making commits.

## 6.3 Issues

GitHub issues are most commonly used to raise bugs that have been found. They can also be used to communicate proposed
new features that are being worked on or that might be worked on. Issues are open to both the module maintainer and the
wider community to open and start a two-way forum like discussion detailing how a bug might be solved or how the feature
might be implemented. What is most important is that the conversations are open and public for anyone with expertise to
comment on. This aims to get the best possible solution and work towards high quality maintainable code. No matter how
trivial the issue, make the discussion open. You may find constructive conflict occurs and this should be viewed in a
positive light as it leads towards the best ideas (the SilverStripe community also has a code of conduct to help resolve
these conflicts). Even if issues are discussed in-person, summarise the conversation and make it available in the
appropriate GitHub issue. This does a few things, firstly, it creates a record of the decision, so that in the future
your team or other community contributors can understand the reasoning for why and how features have been implemented.
Secondly, it helps break down the us/them mentality, by showing engagement with community and broadening the
decision-making process. Finally, participating in the community has the potential to generate trust and better
discourse, creating more diverse perspectives and better overall decision making.

## 6.4 Forking

A fork is a complete copy of a publicly shared code repository often from developers unaffiliated to the original set of
code. A GitHub user will usually fork a repository because they simply want a snapshot of the code (to act as a kind of
bookmark when they are scanning the FOSS environment for code they might reuse), or more commonly, they fork the
repository in order to modify and improve it, later offering the contribution back to the original code repository. Even
if a user does not have permission to write to an agency's repository. For instance, a member of the public, or another
agency, can always fork the repository, make the desired changes in their fork without affecting the original project.
This allows for wide reuse of shared code and greater autonomy as no explicit permission needs to be granted (which when
paired with an appropriate open source license creates a highly dynamic and innovative ecosystem of reuse). Taking a
fork and improving the code will usually lead to a pull request when contributions are passed back to improve the
original code.

## 6.5 Pull requests

Pull requests allow other developers in the FOSS community to submit their improvements for consideration by the
original project maintainer(s). The maintainers are publicly presented with the changes made by the contributor, along
with a forum to discuss and peer review the code. Often suggestions for improvements to the proposed code are made by
the module maintainer that may lead to further improvements to the quality of the code before it is accepted into the
project. Maintainers can then either choose to accept or reject the proposed improvements, that is, the maintainer of
the original repository has full control over their codebase, clearly dispelling the myth that FOSS code is an open
free-for-all. In most cases, once accepted, the changes are automatically merged into the codebase and the contributor
is given credit in the commit log. It should be [perfectly acceptable](http://ben.balter.com/2012/04/15/cfpb-accepts-first-citizen-submitted-pull-request-on-behalf-of-federal-government/)
and even encouraged for government agencies to accept pull requests from the FOSS community, other agencies, vendors and
the wider public as long as it is appropriately licensed this all leads to improved code and better digital services for
citizens and businesses.

Pull requests are kept alongside the code repository as a list of reviewable comments and code. Regular review of pull
requests is key to ensure that they are dealt with in a timely fashion and do not end up piling up. Ideally agencies
should empower their teams of developers by entrusting them to make decisions on pull requests by allowing them to
respond to comments, accept or reject pull requests based on robust peer review and coordinate the releases of new
versions of the shared code. In cases where the agency is working alongside a vendor it may be that the vendor and
agency can come to a service agreement where the vendor will perform the task of peer reviewing pull requests on their
behalf. Either way, of key importance is to keep the process informal (this does not mean unorganised). Adding the
overhead of a traditional governance layer to the acceptance of pull requests is likely to slow the code sharing process
down and reduce many of the benefits of working with FOSS in an openly innovative way.

## 6.6 Release management

A final topic of importance for social coding is the idea of release management for shared code. One of the maxims of
FOSS development is to *'release early, and often'* (The Cathedral and the Bazaar, 2015). When working on GitHub, it is
culturally acceptable to have public code that is not yet ready for production. This is how bugs and improvements can be
actioned early and improve the quality of the code before it is production ready. Best practice is to use what is
referred to as semantic versioning (SemVer) to indicate to other users developers the current state of the code and
which sets of code they should be using in their projects. The benefit of this approach in the SilverStripe ecosystem is
that the composer code management tool makes use of these versioning conventions to ensure you always have the correct
versions of modules to work alongside SilverStripe CMS core and any of the CWP specific modules. It can also be useful
to SemVer your custom project as the CWP deployment tool can also use SemVer to deploy specific versions to the platform
environments. SemVer follows a three point numbering system of x.y.z. For example, 3.1.9 is the current semantic version
of the SilverStripe CMS at the time of writing. Let's break down what this actually means.

**X**.y.z - **X** indicates the major version release of the code. If the code undergoes a major rewrite with backwards
incompatible public API changes this number is incremented indicating to developers they will need to do some work to
gain the benefits of any new features released in the new major version, as well as upgrades to modules.

x.**Y**.z -**Y** indicates the minor version release of code. If new features have been added they will be backwards
compatible, that is, you will be able to use them alongside your existing code dependencies and bespoke code.

x.y.**Z** - **Z** is the patch version release of the code. This indicates a bug or security fix has been added to the
current minor version and should be able to be a completely backwards compatible drop in upgrade. It is these versions
that you should be most regularly releasing as pull requests are raised and quick fixes to shared code are contributed.

When creating publicly shared modules they should start off with a 0.1.0 tagged release and begin to increment from this
point forward. This indicates that there is no major stable version yet ready for production. Over time as incremental
contributions are made and the code is improved, tested and deemed ready to use in projects the semantic version would
increment to 1.0.0. However this is not to say that earlier versions of code cannot be used in projects, however caution
and thorough testing would need to occur. Both git version control, GitHub, CWP GitLab and the composer code management
tool utilise SemVer tagging as this widely practiced standard in the wider FOSS community.
