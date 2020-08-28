---
layout: post
title:  "pyfair 0.2-beta.0 Testing"
date:   2020-09-01 21:00:00 -0500
categories: update
---

<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
<img src="/assets/2020-09-01-pyfair-0-2-beta-0-testing/logo.PNG" alt="pyfair_logo" width="25%"/>

## TL;DR

Please:

1. Please download the [beta package of pyfair and install](https://github.com/theonaunheim/pyfair/archive/dev.zip);
2. Run through your typical workflow in the beta version.
3. Send me your responses on [Github](https://github.com/theonaunheim/pyfair/tree/dev) or via this [survey link](https://forms.gle/R4yP2UcqdH4JkztP6).

## Overview

Thanks for your interest in testing pyfair!

The jump from version 0.1-alpha.10 to to 0.2-beta.0 is the project's
biggest change since the first commit. These changes include but are
not limited to:

* Changing $$ \alpha $$ and $$ \beta $$ for PERT derivations from
  `prevalence` derivation to the more commonly accepted version from
  Wikipedia;
* Universally changing `mode` argument to `most_likely`;
* Added backwards compatability options to allow cross-version model
  sharing;
* Added methods for export of loss curves directly to models and
  metamodels;
* Supporting different currency prefixes, while still defaulting to
  dollars; and,
* Testing against: `python 3.8.3`, `matplotlib 3.2.2`, `numpy 1.18.5`,
  `pandas 1.0.5`, and `scipy 1.5.0`.

Because of these changes (and because we're making the jump from alpha
to beta), I'd like to formally gather feedback and bugs before
finalizing release. What follows below is the way I would like to
coordinate testing.

## Process

Generally speaking my ask can be summed up as: install the new version
of pyfair on your machine and use it for a few weeks. If you have any
problems while using it, I ask that you email me so I can log an issue
in Github. At the end of the usage period I will send the testers an
anonymous survey in which they can provide their candid opinions.

## How to set up environment

This guide presumes that you have Python (version 3 or higher) installed 
on your machine (either via [the reference implementation](https://www.python.org/downloads/)
or a [derivative implementation such as Anaconda](https://www.anaconda.com/products/individual)).

Should you run into any difficulties please contact me.

### Setup Step 1 (Download)

Download the most recent version of the pyfair development branch by
clicking [here](https://github.com/theonaunheim/pyfair/archive/dev.zip)
and save the "pyfair-dev.zip" file to a folder of your choosing.

### Setup Step 2 (Environment Creation)

To prevent side effects, your testing will be performed in an isolated
environment. To create this environment you will be using the `venv`
tool. You will navigate to your folder of choice and then create your
environment using the following commands:

{% highlight shell %}
cd FOLDER_OF_CHOICE
python -m venv ./pyfair_beta
{% endhighlight %}

This will create a folder containing your isolated environment called
"pyfair_beta".

### Setup Step 3 (Activate / Install / Deactivate)

The next step is to install the development package. You do this by
first "activating" your virtual environment. Within your "pyfair_beta"
folder will be a subfolder called
"Scripts". Executing the appropriate activation file for your platform
(e.g. "activate", "activate.bat" or "Activate.ps1") will start your
virtual environment. Your shell may also give you a visual cue. For
example:

{% highlight shell %}
cd FOLDER_OF_CHOICE/pyfair_beta/Scripts
activate
{% endhighlight %}

Would bring up the virtual environment on a Windows system using CMD.
Afer the environment has been activated, you can install the development
package. This is done by running the command:

{% highlight shell %}
pip install FOLDER_OF_CHOICE/pyfair-dev.zip
{% endhighlight %}

You may also install any other items you require in your environment
at this time, such as:

{% highlight shell %}
pip install jupyter
{% endhighlight %}

After you are done testing and wish to go back to your "normal" Python
install, you can deactivate your environment by running the command:

{% highlight shell %}
deactivate
{% endhighlight %}

### Testing: Activate / Test / Deactivate

**Note: this step must be performed each and every time you want to test.**

The next portion of the process is the actual testing. Every time you
begin testing you must activate the pyfair_beta environment you
created earlier. You will do this by executing the appropriate
activation file for your platform (e.g. "activate", "activate.bat" or
"Activate.ps1")

{% highlight shell %}
cd FOLDER_OF_CHOICE/pyfair_beta/Scripts
activate
{% endhighlight %}

Then run through your typical development process, whether it is in the
form of using a Jupyter Notebook or simply using scripts. The closer
you can keep your work to your typical, day-to-day processes, the better.
This should give me good coverage. If nothing immediately comes to mind,
I'd recommend going through the samples on the [ReadTheDocs page](https://pyfair.readthedocs.io/en/latest/).

### Removal: Uninstall

To remove your environment, simply close your shell and delete the
"pyfair_beta" folder.

### Post-Review Questionnaire

After the review period I ask that you fill out [this questionnaire](https://forms.gle/R4yP2UcqdH4JkztP6).
If you want to email me or simply file a Github issue that is also
welcomed.

Thanks again for your taking the time to test pyfair. This project
would not exist without the contributions of people like you.
