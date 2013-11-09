# linters - an introduction to static code analysis

# What is a linter?

Originally, `lint` was a tool for scanning `.c` code for additional, stricter warnings. By statically analyzing the code itself before compilation, programmers could maintain a higher level of code discipline, increasing the reliability of the code in multiple compilers and environments.

As time went on, static code analysis was eclipsed by dynamic analysis: [unit tests](https://en.wikipedia.org/wiki/Unit_test), that examine how code behaves for different inputs and corner cases.

Today, linters are used to supplement unit tests, serving primarily as low priority style checkers. Linters are being written for many programming languages and document formats, detailed below.

[Wikipedia:List of tools for static analysis](http://en.wikipedia.org/wiki/List_of_tools_for_static_code_analysis)

# Linters

Many compilers include an option like `-Wall` to turn on warnings, `-Wextra` for even more warnings, and also `-Werror` to treat warnings as errors, preventing dirty code from compiling.

## *

[astyle](http://astyle.sourceforge.net/) can help enforce a uniform coding style in a large software project.

[pfff](https://github.com/facebook/pfff/) is a collection of tools by Facebook for analyzing code style, with support for multiple programming languages.

[Phabricator Contributing Guide](http://www.phabricator.com/docs/phabricator/article/Contributor_Introduction.html#suggested-reading) offers coding standards generally, as well as for PHP, and JavaScript code specifically.

[google-styleguide](https://code.google.com/p/google-styleguide/) is a collection of documents detailing Google's preferred code style, for a variety of programming languages and data formats.

[Mozilla Coding Style](https://developer.mozilla.org/en-US/docs/Developer_Guide/Coding_Style?redirectlocale=en-US&redirectslug=Mozilla_Coding_Style_Guide) is a document detailing Mozilla's preferred coding style.

[MSDN Library: Coding Techniques and Programming Practices](http://msdn.microsoft.com/en-us/library/aa260844(v=vs.60).aspx) offers general tips for coding.

[Microsoft patterns & practices](http://pnp.azurewebsites.net/en-us/) are recommended for .NET projects.

[MSDN Library: Design Guidelines for Class Library Developers](http://msdn.microsoft.com/en-us/library/czefa0ke%28VS.71%29.aspx) presents guidelines for .NET library developers.

[Code Climate](https://codeclimate.com/) is a paid web service for automatically generating code quality reports.

## BitTorrent

[torrentcheck](https://sourceforge.net/projects/torrentcheck/) verifies file download hashes against .torrent files.

## C

[splint](http://splint.org/) has largely replaced the old `lint` tool, offering the same old checks, as well as additional security checks.

[lint](http://www.unix.com/man-page/FreeBSD/1/lint) the original.

[gcc](http://gcc.gnu.org/) offers additional warnings, through its `-Wall` and `-Wextra` options.

[clang](http://clang.llvm.org/) offers even more warnings, through its `-Wall`, `-Wextra`, `-Wmost`, and `-Weverything` options.

[sparse](https://sparse.wiki.kernel.org/index.php/Main_Page) is designed to find potential sources of program faults, especially in kernel code.

[pclint](http://www.keil.com/pclint/) is a classic, nonfree C/C++ linter.

[Misra C CodeCheck](http://www.abxsoft.com/misra/misra-index.html) is a demo C linter.

[uno](http://spinroot.com/uno/) is a simple C linter.

## C++

[cppcheck](http://cppcheck.sourceforge.net/) can check `.cpp` implementation code, as well as `.h` definition code.

g++, part of [gcc](http://gcc.gnu.org/), offers additional checks through its `-Wall` and `-Wextra` options. g++ also includes a `-Weffc++` option to check against rules in Effective C++.

[cpplint](https://pypi.python.org/pypi/cpplint/) is provided as part of the `google-styleguide`.

[nsiqcppstyle](https://code.google.com/p/nsiqcppstyle/) is a South Korean C++ style checker.

[C++ Coding Standards](http://www.gotw.ca/publications/c++cs.htm) is a textbook documenting recommended C++ code style.

[Bjarne Stroustrup's C++ Style and Technique FAQ](http://www.stroustrup.com/bs_faq2.html) is a another document detailing Bjarne Stroustrup's C++ code style.

[Effective C++](http://www.aristeia.com/books.html) details recommended patterns in C++ code.

[Boost Library Requirements and Guidelines](http://www.boost.org/development/requirements.html) is a document detailing community standards for C++ code style.

## C#

[StyleCop](http://archive.msdn.microsoft.com/sourceanalysis) is a C# linter.

[C# Coding Conventions](http://msdn.microsoft.com/en-us/library/vstudio/ff926074.aspx) is a document detailing Microsoft's recommended patterns for C# code.

[patterns & practices Guidance Explorer](http://guidanceexplorer.codeplex.com/) presents a grapical checklist of Microsoft style rules.

## Clojure

[core.typed](https://github.com/clojure/core.typed) offers annotations for type safety.

[eastwood](https://github.com/jonase/eastwood) provides a Leiningen plugin for linting Clojure code.

[kibit](https://github.com/jonase/kibit/) also provides a Leiningen plugin for linting Clojure code.

## CoffeeScript

[coffeelint](https://github.com/clutchski/coffeelint) for Coffee files.

## Common Lisp

[lisp-critic](http://www.mail-archive.com/gardeners@lispniks.com/msg00372.html) is an old analyzer of arbitrary CL code.

[xref](http://www.cs.cmu.edu/Groups/AI/lang/lisp/code/tools/xref/0.html) is an old static analysis tool for CL code.

## Coq

[Coq](http://coq.inria.fr/) is a proof assistant, requiring all programs to be logically valid.

## CSS

[csslint](https://github.com/stubbornella/csslint) for CSS files.

[minify](https://npmjs.org/package/minify) can help compress, CSS, JS, and HTML files.

[csstidy](http://csstidy.sourceforge.net/) can help compress CSS files.

## D

[gdc](http://dlang.org/) offers a builtin `-Wall` flag for additional warnings.

## Dart

`pub publish` offers a `--dry-run` option.

## Debian packages

[Lintian](http://lintian.debian.org/) checks for bugs and policy violations in .deb packages.

## DNS

[Dlint](http://freecode.com/projects/Dlint) analyzes DNS records.

## Elisp

[elisp-lint](https://github.com/nschum/elisp-lint)

[elint](http://repo.or.cz/w/emacs.git/blob/03e680f0ad11461b40b8d07e99541e2cd32681ae:/lisp/emacs-lisp/elint.el)

## ePUB

[epubcheck](https://github.com/IDPF/epubcheck) analyzes .epub files for errors.

## Erlang

[erl_tidy](http://www.erlang.org/doc/man/erl_tidy.html), a library that comes with Erlang, attempts to automatically change unidiomatic code.

[ehrlich](http://www.yellosoft.us/ehrlich) provides a safer linter that does NOT automatically change your code.

[dialyzer](http://www.erlang.org/doc/man/dialyzer.html), a tool that comes with Erlang, helps detect type errors.

## F#

[fantomas](https://github.com/dungpa/fantomas)

## File systems

[fslint](http://www.pixelbeat.org/fslint/) can identify and correct errors in file systems.

[Disk Utility](https://support.apple.com/kb/HT1782) can repair HFS/HFS+ partitions.

[gParted](http://gparted.sourceforge.net/) can check for errors in several file systems.

[fixmbr Windows](http://www.microsoft.com/resources/documentation/windows/xp/all/proddocs/en-us/bootcons_fixmbr.mspx?mfr=true) is a DOS tool for repairing boot sectors, available in Recovery mode in Windows installation media.

[fixmbr Linux](https://launchpad.net/~lenski/+archive/ms-sys/+packages) is a Linux tool for repairing boot sectors, part of the ms-sys package.

## Fortran

[fortranlint](http://stellar.cleanscape.net/products/fortranlint/)

## Go

[golint](https://github.com/bytbox/golint) is an early stage Go linter.

[lint](https://github.com/golang/lint)

## Groovy

[CodeNarc](http://codenarc.sourceforge.net)

## Haskell

[GHC](http://www.haskell.org/platform/), the official Haskell compiler, is reknown for producing correct programs, though its strict type system.

[hlint](https://github.com/ndmitchell/hlint) displays a refactored version of your code, helping users more quickly resolve warnings.

## HTML

[W3C Validator](http://validator.w3.org/) is an online service for linting HTML, XML, and CSS data.

[tidy](http://tidy.sourceforge.net/) can lint HTML files.

[linklint](http://linklint.org/) checks hyperlinks.

## Java

[javac](http://www.oracle.com/technetwork/java/javase/downloads/index.html) offers a `-Xlint` option to print additional warnings. The [maven-compiler-plugin](https://maven.apache.org/plugins/maven-compiler-plugin/compile-mojo.html) can be configured to automatically pass `-Xlint` to the underlying Java compiler every time a project is built.

In Java 8, javac will feature an `-Xdoclint` option to identify undocumented code.

[CheckStyle](http://checkstyle.sourceforge.net/), with decent CLI support, as well as decent Maven support, through [maven-checkstyle-plugin](http://maven.apache.org/plugins/maven-checkstyle-plugin/). Checkstyle also supports identifying undocumented code, through its <a href="http://checkstyle.sourceforge.net/config_javadoc.html">JavaDoc</a> settings.

[PMD](http://pmd.sourceforge.net/) detects flaws and duplicated code.

## JavaScript / Node.js

[JSHint](http://jshint.com/) is far and away the best modern linter available. It's simultaneously easy to use, and highly customizable; offering global and directory specific `.jshintrc` files for rule configuration; and global and directory specific `.jshintignore` files for ignoring certain files and directories, trimming down `jshint`'s output to exactly what you want to see.

[JSLint](http://jslint.com/) is JSHint's predecessor.

[JSLint Errors](http://jslinterrors.com/) explains warnings you may see from JSHint or JSLint.

[CLosure Compiler](https://developers.google.com/closure/) refactors code to improve performance.

[Closure Linter](https://pypi.python.org/pypi/closure_linter/) checks JavaScript for conformance to the Google Style Guide.

[Code Conventions for the JavaScript Programming Language](http://javascript.crockford.com/code.html) is a document detailing community standards for JavaScript code style.

[CoffeeScript](http://coffeescript.org/) is a compiles-to-JavaScript language designed to enforce good JavaScript coding habits at compiler level.

## LaTeX

[lacheck](http://www.rootr.net/man/man/lacheck/1) comes with LaTeX.

[style-check.rb](http://www.cs.umd.edu/~nspring/software/style-check-readme.html) is a LaTeX checker written in Ruby.

## Lua

[luac](http://www.lua.org/manual/4.0/luac.html) offers a builtin `-p` option for syntax validation..

[lualint](https://github.com/philips/lualint) is an early Lua linter.

[lua-checker](https://code.google.com/p/lua-checker/) is another old Lua linter.

[luainspect](http://lua-users.org/wiki/LuaInspect) is yet another dead linter.

## MP3

[mp3check](https://code.google.com/p/mp3check/) analyzes .mp3 files for errors.

## Objective C

[clang](http://clang.llvm.org/) offers builtin options `-Wall`, `-Wextra`, `-Wmost`, and `-Weverything` for showing additional compiler warnings.

[OCLint](http://oclint.org/) can lint ObjC, C, and C++ code.

## OCaml

[mascot](http://mascot.x9c.fr/)

## Pascall

[fpc](http://www.freepascal.org/) offers a `-vw` flag to show additional warnings.

## Perl

[perl](http://www.perl.org/) offers extra warnings through the `use warnings;` (`#!/usr/bin/env perl -w`) and `use strict;` options.

[perltidy](http://perltidy.sourceforge.net/) generates a recommended refactored version of your code.

[perlcritic](https://metacpan.org/pod/perlcritic) applies rules based on O'Reilly Perl Best Practices.

[Perl Best Practices](http://shop.oreilly.com/product/9780596001735.do) is a textbook of recommended Perl coding conventions.

## PHP

[php](http://php.net/) comes with a builtin `-l` option to check for valid syntax.

[PHPMD](http://phpmd.org/) is a configurable frontend for static checks.

[PSR-Huh?](http://net.tutsplus.com/tutorials/php/psr-huh/) is a document detailing community standards for PHP code style.

[PEAR Coding Standards](http://pear.php.net/manual/en/standards.php) is a collection of documents detailing community standards for PHP code style.

[CodeIgniter General Style and Syntax](http://ellislab.com/codeigniter/user-guide/general/styleguide.html) is a another document offering PHP code style tips.

## PNG

[pngcheck](http://www.libpng.org/pub/png/apps/pngcheck.html) analyzes .png files for errors.

## Puppet

[puppet-lint](http://puppet-lint.com/) checks Puppet scripts for proper style.

## Python

[PyChecker](http://pychecker.sourceforge.net/)

[PyLint](http://www.pylint.org/)

[PyFlakes](https://pypi.python.org/pypi/pyflakes)

[Python Style Guide](http://www.python.org/doc/essays/styleguide.html) is a collection of documents for community standards for Python code style.

## R

CRAN has a [lint](http://cran.r-project.org/web/packages/lint/index.html) package.

## Racket

[Typed Racket](http://docs.racket-lang.org/ts-guide/index.html) offers additional checks for type safety.

## RPM

[rpmlint](http://linux.die.net/man/1/rpmlint) checks .rpm packages for errors.

## Ruby

[contracts.ruby](http://egonschiele.github.io/contracts.ruby/) provides a dynamically enforced type safety system.

[reek](https://github.com/troessner/reek) has an extensive list of checks for improving your code.

[flay](https://github.com/seattlerb/flay) looks for repeated code patterns, recommending ways to reduce boilerplate and increase reliability.

[roodi](https://github.com/roodi/roodi) is an old design pattern linter.

[cane](https://github.com/square/cane) applies code quality checks, and can be used to fail a build on encountering poor quality code.

[excellent](https://github.com/simplabs/excellent) is easy to use and configure.

[rubocop](https://github.com/bbatsov/rubocop) can help users update Ruby 1.8 style code to Ruby 1.9/2.0.

[heckle](http://ruby.sadi.st/Heckle.html) performs mutation testing.

[saikuro](https://github.com/metricfu/Saikuro) examines code complexity. Saikuro is currently incompatible with Ruby 1.9/2.0.

[brakeman](https://github.com/presidentbeef/brakeman) is a linter for [Ruby on Rails](http://rubyonrails.org/) projects.

[pelusa](https://github.com/codegram/pelusa) is a linter for specifically [Rubinius](http://rubini.us/) Ruby code.

[flog](http://ruby.sadi.st/Flog.html) identifies the most complex code in your codebase.

[churn](https://github.com/danmayer/churn) looks at version control history to look for frequently changing code, often a sign of poor coding.

[metric_fu](https://github.com/metricfu/metric_fu) scans with a suite of Ruby linters.

[laser](https://github.com/michaeledgar/laser) is a slightly out of date Ruby linter.

[ruby-style-guide](https://github.com/bbatsov/ruby-style-guide) is a document describing community standards for Ruby code style.

## Rust

[rustc](http://www.rust-lang.org/), the Rust compiler, offers a `-Wall` option for additional warnings.

## Sass

[sasslint](https://github.com/dfltr/Sasslint) for Sass files.

## Scala

[Scalastyle](http://www.scalastyle.org/) offers CLI, SBT, and Maven interfaces to a flexible, extensible Scala linter.

[wartremover](https://github.com/puffnfresh/wartremover)

[linter](https://github.com/foursquare/linter) is an early Scala linter.

## sh / shell / bash

[Shellcheck](http://www.shellcheck.net/) is a bash linter written in Haskell.

[checkbashisms.rb](http://manpages.ubuntu.com/manpages/natty/man1/checkbashisms.1.html) is bash linter written in Ruby.

## Smalltalk

[SmallLint](http://c2.com/cgi/wiki?SmallLint) integrates with the OmniBrowser to lint Smalltalk code.

## Snort

[pulledpork](https://code.google.com/p/pulledpork/) helps manage Snort rulesets.

## XML

[xmllint](https://en.wikipedia.org/wiki/Libxml2) is provided as part of the `libxml2` package.

# Continuous Integration

A [Jenkins](http://jenkins-ci.org/) server can generate HTML linter reports for each new code commit.

[Guard](http://guardgem.org/) + [guard-shell](https://github.com/guard/guard-shell) can monitor local code files, automatically outputting linter warnings as the programmer edits his code, simulating a local continuous integration server.

A [make](https://www.gnu.org/software/make/) task can bundle several linters together (e.g. `csslint`, HTML `tidy`, `jshint`), to lint different kinds of files all at once.

[git hooks](http://git-scm.com/book/en/Customizing-Git-Git-Hooks) can be added to a git repo, preventing a programmer from submitting his work until it passes a configured suite of linters.
