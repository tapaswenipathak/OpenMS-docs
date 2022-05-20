Contribute to OpenMS
====================

If you would like to contribute to OpenMS:

* Familiarise yourself with our [online documentation](https://abibuilder.informatik.uni-tuebingen.de/archive/openms/Documentation/release/latest/html/index.html).

* Learn how to [build OpenMS](build-openms-from-source.md).

* Check out the [OpenMS tutorial for developers](https://abibuilder.informatik.uni-tuebingen.de/archive/openms/Documentation/release/latest/html/OpenMS_tutorial.html).

Any questions can be directed at the mailing list.

## Technical Documentation
Untested installers, containers, etc., known as the nightly snapshot, are released every night. They generally pass automated continuous integration tests but no manual tests.  
View the documentation for the nightly snapshot of [OpenMS develop branch](https://github.com/OpenMS/OpenMS/tree/develop) at the [build archive](https://abibuilder.informatik.uni-tuebingen.de/archive/openms/Documentation/nightly/html/index.html).

View the [doxygen log](https://abibuilder.informatik.uni-tuebingen.de/jenkins/job/openms_nightly_packaging/lastBuild/compiler=appleclang-7.3.0,os_label=elcapitan/artifact/build/doc/doxygen/doxygen-error.log).

See the documentation for the [latest release](https://abibuilder.informatik.uni-tuebingen.de/archive/openms/Documentation/release/latest/html/index.html).
View the ([doxygen log](https://abibuilder.informatik.uni-tuebingen.de/jenkins/job/openms_release_packaging/lastBuild/compiler=appleclang-7.3.0,os_label=elcapitan/artifact/build/doc/doxygen/doxygen-error.log)).

## Development Model

OpenMS follows the Gitflow development workflow that is described [here](http://nvie.com/posts/a-successful-git-branching-model/).

We encourage every developer (even if they are eligible to push directly to OpenMS) to create their own fork (e.g. @username). The GitHub people provide documentation on [forking](https://help.github.com/articles/fork-a-repo) and how to [keep your fork up-to-date](https://help.github.com/articles/syncing-a-fork). With your own fork you can follow the Gitflow development model, but instead of merging into `develop` in your own fork you can open a [pull request] (https://help.github.com/articles/using-pull-requests). Before opening the pull request, please check the [checklist](pull-request-checklist.md).

Some more details and tips are collected [here]().

## Coding Conventions

See the manual for coding style recommended by OpenMS: [Coding conventions](coding-conventions.md).
also see: [C++ Guide]().

View the [manual]() for creating a new build unit (to be completed).

We automatically test for common coding convention violations using a modified version of `cpplint`.
Style testing can be enabled using `cmake` options. We also provide a configuration file for `Uncrustify` for automated style corrections (see `tools/uncrustify.cfg`).

## Commit Messages

View the guidelines for commit messages: [How to write commit messages] (alinkstob).

## Automated Unit Tests

We perform nightly test runs on different platforms. Try to test on as many platforms as possible. This will save you time and surprises during continuous integration tests.

Nightly tests: [CDASH](http://cdash.openms.de/index.php?project=OpenMS)

## Further Developer Resources

You may want to consider the following resources:
* **Guidelines for adding new dependency libraries**

  View the guidelines for [adding new dependency libraries]().
* **Experimental installers**

  We automatically build installers for different platforms. These usually contain unstable or partially untested code. Use them at your own risk.

  The nightly (unstable) installers are available at the [build archive](https://abibuilder.informatik.uni-tuebingen.de/archive/openms/OpenMSInstaller/nightly/).
* **Developer FAQ**

  Visit the [Developer FAQ](developer-faq.md) to get answers to frequently asked questions.