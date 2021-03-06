# 1. Think modular

Projects on the CWP should be thought of as modular sets of features made up of a SilverStripe core, a series of
modules, bespoke project customisations, themes, and a configuration layer consisting of database and other sensitive
credentials (which are pre-installed on the CWP). All these components are brought together using the code management
tool, 'Composer'. Composer manages the set of code installed in the project by inspecting a meta data file stored within
the project code that states which modules to install and which versions should be used. Using composer allows new
modules from the open source community and themes to be installed, and unused modules removed from the project easily,
while ensuring the correct code is deployed to the CWP servers.

Note: there are some mandatory packages required for SilverStripe CMS projects running on the CWP which are important in
to include in public sector CWP projects to make use of the provided shared services.

The golden rule is to avoid modifying the SilverStripe core and open source modules directly when working on a project.
The SilverStripe CMS community has developed best practice techniques to extend the functionality of the CMS while
ensuring they can benefit from future upgrades. Using composer and following the golden rule will allow for easy
SilverStripe core upgrades when new versions are release (thorough testing when upgrading is still recommended).
Building and extending modular code hedges the project risk as it encourages better code to be written that is more
readable and well constructed. This makes the maintenance for future developers easier to perform as the commodity logic
remains abstracted from the specific project application logic rather than it being intertwined and harder to share and
maintain (Balter, 2012).

Key to this way of thinking is ensuring features are seen as discrete units of work that encapsulate a set of generic
functionality. Exactly how big or small these are is up to the individual development team, however a good idea is to
think about how these features might be reused in future projects or how they could be combined with other modules to
create further functionality. For instance the SilverStripe blog functionality has a central blog module with
standardised publishing features such as having an author and publishing date. This module itself does not manage
comments. Instead, there is a separate comment module which can be included alongside the blog module. It is when all
these components are together that a full blogging experience is created. However, comments could just as easily be used
for other purposes wherever this feature is required, and the blog module itself could be used without the comments to
create a press release section of a website. When code is broken down into smaller, modular parts they become easier to
share and maintain, further they become more interchangeable. For example, the blog comments module could be exchanged
for some other third party commenting system if need be.
