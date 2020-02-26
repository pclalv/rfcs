# Meta
[meta]: #meta
- **Name:** Flexible Buildpack Versions
- **Start Date:** 2020-03-11
- **Supersedes:** N/A

# Summary
[summary]: #summary

The buildpacks project **does not** want to enforce rules or format requirements for buildpack versions. This RFC explains that buildpack authors can use any pattern (ie. semantic versioning) when deciding how to release versions of buildpacks.

# Motivation
[motivation]: #motivation

There aren't specific guidelines in the buildpack documentation for buildpack authors that explain how versioning works for buildpacks. It should be explicitly stated that the API supports any version format.

Therefore, buildpack authors have clear documentation that they can use any versioning system that works for their development workflow.

# What it is
[what-it-is]: #what-it-is

Buildpack authors can version buildpacks how they want. This requires no additional code, but instead clarification around how versions are referred to.

# How it Works
[how-it-works]: #how-it-works

The Buildpack team is making a commitment to the future of the project that buildpack developers will have the freedom to format buildpacks anyway, and these format decisions will not break the Buildpack API.

### TODO:
- explicitly state that there are no versioning restrictions in the buildpack spec, as well as the docs
- change any current messaging (ie. variable names or code comments) that states otherwise

# Drawbacks
[drawbacks]: #drawbacks

- This decision could cause issues with the Buildpack API if there is specific types that are required. For example, if versions need to be integers in a later version of the API, semantic versioning would not work because it requires a string.
- Buildpack authors may request more guidance on buildpack versioning.

# Alternatives
[alternatives]: #alternatives

- Do nothing/Don't explicitly specify that there are no restrictions on versions
  - This isn't ideal because there is currently conflicting messaging between code and documentation that's not clear if there are API restrictions.
- Restrict buildpack versions to certain rules or format.
  - There isn't an immediate benefit to this since versioning can tie into a development process and workflow (and should not be dictated by the tool).

# Prior Art
[prior-art]: #prior-art

- Issue opened to specify version requirements in the spec: https://github.com/buildpacks/spec/issues/72
- Code comment that makes it seem like sem-ver is expected: https://github.com/buildpacks/libbuildpack/blob/b2e4a9ef07aff26c430dfac2fbc928ee4164af35/buildpack/info.go#L27

# Unresolved Questions
[unresolved-questions]: #unresolved-questions

- N/A
