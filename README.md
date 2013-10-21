# linters - an introduction to static code analysis

# What is a linter?

Originally, `lint` was a tool for scanning `.c` code for additional, stricter warnings. By statically analyzing the code itself before compilation, programmers could maintain a higher level of code discipline, increasing the reliability of the code in multiple compilers and environments.

As time went on, static code analysis was eclipsed by dynamic analysis: [unit tests](https://en.wikipedia.org/wiki/Unit_test), that examine how code behaves for different inputs and corner cases.

Today, linters are used to supplement unit tests, serving primarily as low priority style checkers. Linters are being written for many programming languages and document formats, detailed below.

[Wikipedia:List of tools for static analysis](http://en.wikipedia.org/wiki/List_of_tools_for_static_code_analysis)

# Linters

## *

[astyle](http://astyle.sourceforge.net/) can help enforce a uniform coding style in a large software project.

## C

[splint](http://splint.org/) has largely replaced the old `lint` tool, offering the same old checks, as well as additional security checks.

[lint](http://www.unix.com/man-page/FreeBSD/1/lint) the original.

[gcc](http://gcc.gnu.org/) offers additional warnings, through its `-Wall` option.

[clang](http://clang.llvm.org/) offers additional warnings, through its `-Wall` option.

[sparse](https://sparse.wiki.kernel.org/index.php/Main_Page) is designed to find potential sources of program faults.

## C++

[cppcheck](http://cppcheck.sourceforge.net/) can check `.cpp` implementation code, as well as `.h` definition code.

[cpplint](https://code.google.com/p/google-styleguide/) is provided as part of the `google-styleguide`.

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

## Erlang

[erl_tidy](http://www.erlang.org/doc/man/erl_tidy.html), a library that comes with Erlang, attempts to automatically change unidiomatic code.

[ehrlich](http://www.yellosoft.us/ehrlich) provides a safer linter that does NOT automatically change your code.

[dialyzer](http://www.erlang.org/doc/man/dialyzer.html), a tool that comes with Erlang, helps detect type errors.

## Go

[golint](https://github.com/bytbox/golint) is an early stage Go linter.

## Haskell

[GHC](http://www.haskell.org/platform/), the official Haskell compiler, is reknown for producing correct programs, though its strict type system.

[hlint](https://github.com/ndmitchell/hlint) displays a refactored version of your code, helping users more quickly resolve warnings.

## HTML

[W3C Validator](http://validator.w3.org/) is an online service for linting HTML, XML, and CSS data.

[tidy](http://tidy.sourceforge.net/) can lint HTML files.

## Java

[javac](http://www.oracle.com/technetwork/java/javase/downloads/index.html) offers a `-Xlint` option to print additional warnings. The [maven-compiler-plugin](https://maven.apache.org/plugins/maven-compiler-plugin/compile-mojo.html) can be configured to automatically pass `-Xlint` to the underlying Java compiler every time a project is built.

[CheckStyle](http://checkstyle.sourceforge.net/), with decent CLI support, as well as decent Maven support, through [maven-checkstyle-plugin](http://maven.apache.org/plugins/maven-checkstyle-plugin/).

[PMD](http://pmd.sourceforge.net/) detects flaws and duplicated code.

## JavaScript / Node.js

[JSHint](http://jshint.com/) is far and away the best modern linter available. It's simultaneously easy to use, and highly customizable; offering global and directory specific `.jshintrc` files for rule configuration; and global and directory specific `.jshintignore` files for ignoring certain files and directories, trimming down `jshint`'s output to exactly what you want to see.

[JSLint](http://jslint.com/) is JSHint's predecessor.

[JSLint Errors](http://jslinterrors.com/) explains warnings you may see from JSHint or JSLint.

## LaTeX

[lacheck](http://www.rootr.net/man/man/lacheck/1) comes with LaTeX.

## Lua

[lualint](https://github.com/philips/lualint) is an early Lua linter.

[lua-checker](https://code.google.com/p/lua-checker/) is another old Lua linter.

## Perl

[perl](http://www.perl.org/) offers extra warnings through the `use warnings;` (`#!/usr/bin/env perl -w`) and `use strict;` options.

[perltidy](http://perltidy.sourceforge.net/) generates a recommended refactored version of your code.

## PHP

[php](http://php.net/) comes with a builtin `-l` option to check for valid syntax.

[PHPMD](http://phpmd.org/) is a configurable frontend for static checks.

## Python

[PyChecker](http://pychecker.sourceforge.net/)

[PyLint](http://www.pylint.org/)

[PyFlakes](https://pypi.python.org/pypi/pyflakes)

## Racket

[Typed Racket](http://docs.racket-lang.org/ts-guide/index.html) offers additional checks for type safety.

## Ruby

[contracts.ruby](http://egonschiele.github.io/contracts.ruby/) provides a dynamically enforced type safety system.

[reek](https://github.com/troessner/reek) has an extensive list of checks for improving your code.

[flog](http://ruby.sadi.st/Flog.html) helps to make code more amenable to unit testing.

[flay](https://github.com/seattlerb/flay) looks for repeated code patterns, recommending ways to reduce boilerplate and increase reliability.

[heckle](http://ruby.sadi.st/Heckle.html) performs mutation testing.

[roodi](https://github.com/roodi/roodi) is an old design pattern linter.

[saikuro](https://github.com/metricfu/Saikuro) examines code complexity.

[churn](https://github.com/danmayer/churn) looks at version control history to look for frequently changing code, often a sign of poor coding.

[cane](https://github.com/square/cane) applies code quality checks, and can be used to fail a build on encountering poor quality code.

[metric_fu](https://github.com/metricfu/metric_fu) scans with a suite of Ruby linters.

## Rust

[rustc](http://www.rust-lang.org/), the Rust compiler, offers a `-Wall` option for additional warnings.

## Sass

[sasslint](https://github.com/dfltr/Sasslint) for Sass files.

## Scala

[Scalastyle](http://www.scalastyle.org/) offers CLI, SBT, and Maven interfaces to a flexible, extensible Scala linter.

[linter](https://github.com/foursquare/linter) is an early Scala linter.

## Smalltalk

[SmallLint](http://c2.com/cgi/wiki?SmallLint) integrates with the OmniBrowser to lint Smalltalk code.

## XML

[xmllint](https://en.wikipedia.org/wiki/Libxml2) is provided as part of the `libxml2` package.

# Continuous Integration

A [Jenkins](http://jenkins-ci.org/) server can generate HTML linter reports for each new code commit.

[Guard](http://guardgem.org/) + [guard-shell](https://github.com/guard/guard-shell) can monitor local code files, automatically outputting linter warnings as the programmer edits his code, simulating a local continuous integration server.

A [make](https://www.gnu.org/software/make/) task can bundle several linters together (e.g. `csslint`, HTML `tidy`, `jshint`), to lint different kinds of files all at once.

[git hooks](http://git-scm.com/book/en/Customizing-Git-Git-Hooks) can be added to a git repo, preventing a programmer from submitting his work until it passes a configured suite of linters.
