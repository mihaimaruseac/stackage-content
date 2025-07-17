---
author: Mihai Maruseac
title: LTS 24 release for ghc-9.10 and Nightly now on ghc-9.12
description: Stackage LTS 24 (ghc-9.10.2) has been released and Stackage Nightly moved to ghc-9.12.2.
timestamp: 2025-07-16T07:00:00Z
---

## Stackage LTS 24 has been released

The Stackage team is happy to announce that
[Stackage LTS version 24](https://www.stackage.org/lts-24.0) has finally been
released a couple of days ago, based on GHC stable version 9.10.2.

LTS 24 includes many
[package changes](https://www.stackage.org/diff/lts-23.27/lts-24.0), and over
3400 packages! Thank you for all your nightly contributions that made this
release possible: the initial release was prepared by Mihai Maruseac. The
closest nightly snapshot to lts-24.0 is
[nightly-2025-07-13](https://www.stackage.org/diff/nightly-2025-07-13/lts-24.0).

If your package is missing from LTS 24 and can build there, you can easily
have it added by opening a PR in
[lts-haskell](https://github.com/commercialhaskell/lts-haskell/) to the
[build-constraints/lts-24-build-constraints.yaml](https://github.com/commercialhaskell/lts-haskell/blob/master/build-constraints/lts-24-build-constraints.yaml)
file.

## Stackage Nightly updated to ghc-9.12.2

At the same time we are excited to move [Stackage
Nightly](https://www.stackage.org/nightly) to GHC 9.12.2: the initial snapshot
release is [nightly-2025-07-15](https://www.stackage.org/nightly-2025-07-15).
Current nightly has over 3100 packages, and we expect that number to grow over
the coming weeks and months: we welcome your contributions and help with this.
This initial release build was made by Jens Petersen (31 commits).

A number of packages have been disabled, with the switch to a new GHC version.
You can see all the
[changes](https://www.stackage.org/diff/nightly-2025-07-14/nightly-2025-07-15)
made relative to the preceding last 9.10 nightly snapshot.
Apart from trying to build yourself, the easiest way to understand why
particular packages are disabled is to look for their `< 0` lines in
[build-constraints.yaml](https://github.com/commercialhaskell/stackage/blob/master/build-constraints.yaml),
particularly under the `"Library and exe bounds failures"` section.
We also have some
[tracking issues](https://github.com/commercialhaskell/stackage/issues?q=is%3Aissue+is%3Aopen+label%3Aghc-9.12)
still open related to 9.12 core boot libraries.

Thank you to all those who have already done work updating their packages for ghc-9.12.

Adding or enabling your package for Nightly is just a simple
[pull request](https://github.com/commercialhaskell/stackage/blob/master/MAINTAINERS.md#adding-a-package)
to the large
[build-constraints.yaml](https://github.com/commercialhaskell/stackage/blob/master/build-constraints.yaml)
file.

If you have questions, you can ask in Stack and Stackage Matrix room
(`#haskell-stack:matrix.org`) or Slack
[channel](https://haskell-foundation.slack.com/archives/C023DF5202X).
