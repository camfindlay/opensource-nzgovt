# 5. Code Repositories

## 5.1 Version control and git

Version control allows multiple contributors to software code by allowing small bundles of work to be committed by
individual developers to a project over time. Think of it like track-changes for document files, however much more
useful as it allows multiple authors working on the document simultaneously and avoids having to pass the document back
and forth via some other communication mechanism (email for example). One such version control system (VCS) called 'Git'
has become one of the most widely used throughout the world (Git, 2015). Git is a distributed VCS that allows many
developers to work simultaneously on the same project code by allowing multiple branches and incremental improvements to
be peer reviewed and included back to the project. Git is utilised as the VCS on the CWP through the use of a private
code repository tool called 'GitLab' (henceforth referred to as 'CWP GitLab' due to it's similar name to the social
coding platform GitHub). Git is the underlying technology of both CWP GitLab, GitHub and many other social coding
platforms where FOSS code is shared and contributed to.

## 5.2 What is GitHub?

[GitHub](http://github.com/) is a social coding platform that allows teams to collaborate among themselves or with the
general public and has quickly become the go-to social network for the FOSS community. For example, the govt.nz website
has a organisational GitHub account where they release their FOSS modules and tools for the CWP. Code is grouped by
organisation, which can consist of teams, or user who maintain repositories of code. The SilverStripe CMS core and many
of the modules utilised on the CWP are maintained and actively worked on by the community via GitHub. It is in effect
the social network of the SilverStripe CMS community (complemented by other digital channels such as mailing lists,
forums and an IRC channel). GitHub is based on the VCS known as [Git](http://en.wikipedia.org/wiki/Git_(software).
In essence, Git keeps a running log of all changes to a software project's code. Each time you make a change, you
describe that change (a commit message) and then push that change to GitHub. GitHub also allows members of the public to
'[fork](http://ben.balter.com/open-source-for-government/#forks)' existing projects, improve upon them, and then submit
their changes back as a "[pull request](http://ben.balter.com/open-source-for-government/#pull_requests)". GitHub offers
free public repositories for FOSS projects as well as subscription-based private repositories for closed projects.

Agencies looking to get started should create an organisation account with GitHub, which can include an unlimited number
of individual developer accounts. There is an existing government-friendly terms of service that GitHub has already
reviewed and signed with many US based government entities (among others around the world). As the core purpose of
GitHub is to track who made changes to what code and when, this may help with any requirements for public records
keeping. Before using the service you should double check with your agency's digital service procurement policy though
referring back to the NZ Govt ICT Strategy there is a push to acquire more ICT resources on a services basis which
aligns with what GitHub offers. [GitHub also has a Goverment CoP](https://government.github.com/) that any government
staff with a .govt.nz email address account associated with their GitHub account can access and discuss the ideas of
code sharing, open innovation and the use of social coding platforms within government.

## 5.3 What is CWP GitLab?

CWP GitLab is used to manage website projects on the CWP that are eventually deployed onto testing and later, production
environments. It enables sharing, collaboration, and audit trails of the code worked on by development teams. It is run
securely on the CWP infrastructure which is based within New Zealand. Agencies can choose whether code they produce is
private or shared, on a case by case basis however as a matter of principle, if the agency has created reusable modular
code it should be made open and available for others to use. CWP GitLab is provisioned as part of the shared services
when an agency onboards to the CWP. Access to accounts can be granted to agency ICT staff and vendors working on their
behalf. CWP GitLab is however not open to the wider FOSS community to contribute (though there are some [publicly listed
modules](https://gitlab.cwp.govt.nz/public) available on CWP GitLab that agencies have listed as public). When existing
FOSS modules are contributed to or an agency creates a new module which they would like to openly share, a more
appropriate location to release this code is the social coding platform, GitHub. CWP GitLab has a virtually identical
set of features to GitHub, however it is only accessible to those that have signed on to the CWP.

## 5.4 Where to start building projects and modules for the CWP?

Given git's distributed nature, modules are able to be started on CWP GitLab and later moved to the more open code
sharing space, GitHub. This allows agencies new to the idea of code sharing a safe space to develop the initial set of
code before open sourcing it and making it available to others in the FOSS community. However there are benefits for
starting new open source modules directly in the most open space such as getting peer review early and attracting
interest from other users in the community. You may even learn from the community at this point that such a module
already exists and in this case perhaps the time is better spent improving the existing shared code rather than
developing a new one from scratch. CWP also allows for modules to be made public and still reside on CWP Gitlab, note
however that in this situation, developers outside of the CWP cannot give feedback or contribute improvements, therefore
GitHub is preferred and not mandated. Private project code (code that is not modules and relates to the customisation of
SilverStripe CMS) should also be kept on CWP GitLab. This space should be used as a collaborative coding space for the
development team doing work on the project. It also need to reside here in order for it to be safely deployed on to the
CWP instance environments.
