# How to contribute

So, you're reading the contributing guidelines... Does this mean that you have a god idea for this project? I'm so excited to hear it! Please don't let that thought go before you've let me know about it. You can simply [open an issue](https://github.com/krilor/wordpress-website-standards/issues/new) just outlining what you are thinking about or read this document and open a proper pull request. Any input, corrections, additions and ideas are welcome!

This document covers how do [pull requests](https://help.github.com/articles/about-pull-requests/) and some conventions on how the standard is written. 

# Branching and pull requests

This project tries to use [github flow](https://guides.github.com/introduction/flow/). For you, as a contributor, that simply means that pull request goes directly into the master branch.

Please try to be descriptive in both branch name, commits and pull request.

# Conventions

When helping out, please consider the following guidelines for this document.

* Each requirement or recommendation **should** have it’s own short level three headline
    * Remember to update the Table of Contents. It's set up to use [Sublime3 MarkdownTOC](https://github.com/naokazuterada/MarkdownTOC)
* The actual requirement or recommendation **must** follow directly after the headline as a quote, and contain either of the words “must” or “should” in bold to make it clear whether it is a requirement or recommendation.
* After the quote there can be text or images that describes why the requirement **should** be met, and how.
* The standard **should** be as short as possible, but descriptive enough to be unambiguous.
* Refer to pillar content other places on the web rather than including in this documents.
* Refer to WordPress documentation whenever possible.
* Try to think about the testability of requirements.

# Semantic Versioning

This project uses [Semantic Versioning](https://semver.org/), but on a text resource. This means that the interpretation of Major.Minor.Patch has to be a bit different. Please refer point 6-8 in [Semantic Versioning](https://semver.org/)

<dl>
  <dt>Backwards compatible bug fixes</dt>
  <dd>Additional clarifications, spelling corrections or any other small change that does not change the standard at all.</dd>
  <dt>Backwards compatible functionality</dt>
  <dd>Added or removed requirements or any substantial changes to existing ones.</dd>
  <dt>Backwards incompatible changes</dt>
  <dd>Major changes to the structure of the document.</dd>
</dl>

Bumping the major version can also be done at important project milestones.
