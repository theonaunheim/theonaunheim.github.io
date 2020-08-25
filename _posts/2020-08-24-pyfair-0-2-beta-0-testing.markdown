---
layout: post
title:  "pyfair 0.2-beta.0 Testing"
date:   2020-08-24 21:06:46 -0500
categories: update
---

<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
<img src="/assets/2020-08-24-pyfair-0-2-beta-0-testing/logo.PNG" alt="pyfair_logo" width="50%"/>

# Overview

Thanks for your interest in testing pyfair!

The jump from version 0.1-alpha.10 to to 0.2-beta.0 is the project's
biggest change since the first commit. The changes include but are
not limited to:

* Changing $$ \alpha $$ and $$ \beta $$ for PERT derivations from
  `prvalence` derivation to the more commonly accepted version from
  Wikipedia;
* Universally changing mode argument to most_likely;
* Added backwards compatability options to allow cross-version model
  sharing;
* Added methods for export of loss curves to models and metamodels;
* Supporting different currency prefixes, while still defaulting to
  dollars; and,
* Testing against: `python 3.8.3`, `matplotlib 3.2.2`, `numpy 1.18.5`,
  `pandas 1.0.5`, and `scipy 1.5.0`.

Because of these changes (and because we're making the jump from alpha
to beta), I'd like to formally gather feedback and bugs before
finalizing release.

# Process

