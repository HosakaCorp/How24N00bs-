Book Generator
==============

This portion of the repository houses the dispatch.sr.ht manifest and the mdbook yml configuration.

Fundamentally a git hook fires when commits to this repository happen and trigger the manifest to build and generate the static html book.

Once the static HTML is tested for dead links and generated, it is uploaded to the github pages URL automatically (and forcefully).

Workflow
--------

Commit -> dispatch.sr.ht -> build.sr.ht -> mdbook test -> mdbook generate -> git commit -> git push

Structure
---------

* book.toml - configuration for the mdbook
* manifest.yml - build.sr.ht manifest minus the secrets
* domino/ - theme directory. This holds all the templates and stylesheets for generation
* src/ - source directory, this is where the root gets copied to (should be empty for build purposes)
* build/ - build output directory (should be empty)
