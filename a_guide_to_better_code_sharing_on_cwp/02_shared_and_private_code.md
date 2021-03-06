# 2. Shared and private code

When thinking about modular code it is important to consider whether a legitimate security or privacy risk exists in
which case code should be kept private. A key outcome of this paper is to advocate for greater sharable code
contributions into the open source community to make more commodity, reusable code for everyone. The principle of being
open by default applies here. However, some code inevitably may contain sensitive information about how a system is
configured and it might not be appropriate to share this (Stewart, 2014). In this case there are some approaches that
can be taken to minimise the amount privately maintained code.

1. Avoid storing configuration credentials such as passwords, api keys or tokens in shared code. Keep these isolated and
stored on an environment configuration file. When building modular code to share, allow for dynamic configuration and
these values to be passed to the module from the configuration layer. This configuration layer is stored on the CWP and
is per environment, that is, you can arrange to have different settings on a testing server versus a production one.

2. If code contains features that could be shared, intertwined with those that cannot, it is an argument for abstracting
and decoupling these components. The generic code moved into a module and the more sensitive features added to a private
module or custom project code.

3. If a case can be made for an entire module to remain private and it might still be reusable within government only,
these should still be constructed in the same way as sharable code, the process of construction should be no different,
only the availability should be different. In this case private modules can be stored on the CWP private code repository
(GitLab) and still included into projects via the composer tool (with a [slight variation to indicate private module use
when deploying code on to the CWP](https://www.cwp.govt.nz/guides/core-technical-documentation/common-web-platform-core/en/development-tutorials/working-with-modules#including-a-module-in-your-project)).

4. If the code is highly sensitive, and unlikely to be used in other project, then it should be stored in the custom
project codebase and reside on CWP GitLab.
