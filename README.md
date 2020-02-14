# linters - an introduction to static code analysis

# What is a linter?

Originally, `lint` was a tool for scanning `.c` code for additional, stricter warnings. By statically analyzing the code itself before compilation, programmers could maintain a higher level of code discipline, increasing the reliability of the code in multiple compilers and environments.

As time went on, static code analysis was eclipsed by dynamic analysis: [unit tests](https://en.wikipedia.org/wiki/Unit_test), that examine how code behaves for different inputs and corner cases.

Today, linters are used to supplement unit tests, serving primarily as low priority style checkers. Linters are being written for many programming languages and document formats, detailed below.

[Wikipedia:List of tools for static analysis](http://en.wikipedia.org/wiki/List_of_tools_for_static_code_analysis)

# Linters

Many compilers include an option like `-Wall` to turn on warnings, `-Wextra` for even more warnings, and also `-Werror` to treat warnings as errors, preventing dirty code from compiling.

## *

[check-all-the-things](https://anonscm.debian.org/cgit/collab-maint/check-all-the-things.git/plain/doc/README) is a command-line tool for automatically running many static analysis and similar tools over packages and upstream codebases.

[anorack](https://github.com/jwilk/anorack) is a specialized spell-checker that finds incorrect indefinite articles.

[aspelllint](https://github.com/mcandre/aspelllint) provides spell checking for large projects.

[astyle](http://astyle.sourceforge.net/) can help enforce a uniform coding style in a large software project.

[cowl](https://github.com/mcandre/cowl) identifies lines wider than n columns (typically 80), with help from `grep`.

[eclint](https://github.com/jedmao/eclint) can derive the code style used in a project, and save it as a dotfile for use in other projects.

[editorconfig](http://editorconfig.org/) is an editor-agnostic configuration system for code styling.

[editorconfig-cli](https://github.com/amyboyd/editorconfig-cli) is a Go-based editorconfig linter.

[editorconfig-tools](https://www.npmjs.com/search?q=editorconfig-tools) is a command line linter against editorconfig rules.

[enlint](https://github.com/mcandre/enlint) helps identify strangely encoded text files, with help from programs like Unix `find` and `enca`.

[dotenv-linter](https://github.com/wemake-services/dotenv-linter) finds errors and stylistic violations in `.env` files.

[gtdlint](https://github.com/mcandre/gtdlint) identifies TODO notes left in code comments, with help from `grep`.

[lili](https://github.com/mcandre/lili) scans projects for strange line endings.

[line-detector](https://github.com/mcandre/line-detector) identifies line ending formats.

[lint-spaces](https://github.com/schorfES/node-lintspaces) checks line endings and indentation.

[pfff](https://github.com/facebook/pfff/) is a collection of tools by Facebook for analyzing code style, with support for multiple programming languages.

[proselint](https://github.com/amperser/proselint/) is a linter for usage and style errors in English prose.

[sloccount](http://www.dwheeler.com/sloccount/) calculates sources lines of code and extrapolates project man-hours and development cost based on industry averages.

[Sonarqube](http://www.sonarqube.org/) is a cross-programming language linting system.

[Phabricator Contributing Guide](http://www.phabricator.com/docs/phabricator/article/Contributor_Introduction.html#suggested-reading) offers coding standards generally, as well as for PHP, and JavaScript code specifically.

[google-styleguide](https://code.google.com/p/google-styleguide/) is a collection of documents detailing Google's preferred code style, for a variety of programming languages and data formats.

[Hemingway](http://www.hemingwayapp.com/) is a software application for improving the readability of English text. By using Hemingway, we can make our documentation more understandable for others.

[Mozilla Coding Style](https://developer.mozilla.org/en-US/docs/Developer_Guide/Coding_Style?redirectlocale=en-US&redirectslug=Mozilla_Coding_Style_Guide) is a document detailing Mozilla's preferred coding style.

[MSDN Library: Coding Techniques and Programming Practices](http://msdn.microsoft.com/en-us/library/aa260844(v=vs.60).aspx) offers general tips for coding.

[Microsoft patterns & practices](http://pnp.azurewebsites.net/en-us/) are recommended for .NET projects.

[MSDN Library: Design Guidelines for Class Library Developers](http://msdn.microsoft.com/en-us/library/czefa0ke%28VS.71%29.aspx) presents guidelines for .NET library developers.

[Code Climate](https://codeclimate.com/) is a paid web service for automatically generating code quality reports.

[Web Package Update Checker](https://github.com/fulldecent/web-puc) validates web projects to ensure they use the latest available versions of web packages (like Bootstrap, Font Awesome, JQuery).

[write-good](https://github.com/btford/write-good) validuates english prose with the aim of helping developers write better code.

## Android

[lint](http://developer.android.com/tools/help/lint.html) is a tool for static analysis of Android projects.

## Awk

[gawk](http://www.gnu.org/software/gawk/manual/gawk.html) has a `--lint` option for checking script compatibility with other awk implementations.

## BitTorrent

[torrentcheck](https://sourceforge.net/projects/torrentcheck/) verifies file download hashes against .torrent files.

## C

[splint](http://lclint.cs.virginia.edu/) has largely replaced the old `lint` tool, offering the same old checks, as well as additional security checks.

[lint](http://www.unix.com/man-page/FreeBSD/1/lint) the original.

[gcc](http://gcc.gnu.org/) offers additional warnings, through its `-Wall` and `-Wextra` options.

[clang](http://clang.llvm.org/) offers even more warnings, through its `-Wall`, `-Wextra`, `-Wmost`, and `-Weverything` options.

[vera++](https://bitbucket.org/verateam/vera/wiki/Home) is a static analysis tool for C/C++ code.

[banned.h](https://cloudblogs.microsoft.com/microsoftsecure/2012/08/30/microsofts-free-security-tools-banned-h/) helps C/C++ programmers identify deprecated, unsafe dependencies.

[sparse](https://sparse.wiki.kernel.org/index.php/Main_Page) is designed to find potential sources of program faults, especially in kernel code.

[pclint](http://www.keil.com/pclint/) is a classic, non-free C/C++ linter.

[Misra C CodeCheck](http://www.abxsoft.com/misra/misra-index.html) is a demo C linter.

[uno](http://spinroot.com/uno/) is a simple C linter.

[Infer](http://fbinfer.com/) is a static program analyzer for Java, C, Objective-C, and Swift, written in OCaml.

## C++

[cppcheck](http://cppcheck.sourceforge.net/) can check `.cpp` implementation code, as well as `.h` definition code.

g++, part of [gcc](http://gcc.gnu.org/), offers additional checks through its `-Wall` and `-Wextra` options. g++ also includes a `-Weffc++` option to check against rules in Effective C++.

[cpplint](https://pypi.python.org/pypi/cpplint/) is provided as part of the `google-styleguide`.

[nsiqcppstyle](https://code.google.com/p/nsiqcppstyle/) is a South Korean C++ style checker.

[flint++](https://github.com/L2Program/FlintPlusPlus) is a cross-platform, zero-dependency port of [flint](https://github.com/facebook/flint) - a linter developed at Facebook.

[C++ Coding Standards](http://www.gotw.ca/publications/c++cs.htm) is a textbook documenting recommended C++ code style.

[Bjarne Stroustrup's C++ Style and Technique FAQ](http://www.stroustrup.com/bs_faq2.html) is another document detailing Bjarne Stroustrup's C++ code style.

[Effective C++](http://www.aristeia.com/books.html) details recommended patterns in C++ code.

[Boost Library Requirements and Guidelines](http://www.boost.org/development/requirements.html) is a document detailing community standards for C++ code style.

## C&#35;

[StyleCop](https://github.com/StyleCop/StyleCop) is a C# linter that enforces style guidelines.

[Gendarme](http://www.mono-project.com/docs/tools+libraries/tools/gendarme/) is a .NET Static analysis tool created by the mono team. Gendarme enforces best practices, and compatibility with the mono runtime.

[FxCop](https://en.wikipedia.org/wiki/FxCop) is a .NET Static analysis tool created at microsoft. FxCop enforces best practices.

[C# Coding Conventions](http://msdn.microsoft.com/en-us/library/vstudio/ff926074.aspx) is a document detailing Microsoft's recommended patterns for C# code.

[patterns & practices Guidance Explorer](http://guidanceexplorer.codeplex.com/) presents a graphical checklist of Microsoft style rules.

## Chef

[foodcritic](http://www.foodcritic.io/) offers built-in rules for identifying potential problems with Chef cookbooks.

## Clojure

[core.typed](https://github.com/clojure/core.typed) offers annotations for type safety.

[eastwood](https://github.com/jonase/eastwood) provides a Leiningen plugin for linting Clojure code.

[kibit](https://github.com/jonase/kibit/) also provides a Leiningen plugin for linting Clojure code.

## CoffeeScript

[coffeelint](https://github.com/clutchski/coffeelint) for Coffee files.

## Common Lisp

[lisp-critic](http://www.mail-archive.com/gardeners@lispniks.com/msg00372.html) is an old analyzer of arbitrary CL code.

[xref](http://www.cs.cmu.edu/Groups/AI/lang/lisp/code/tools/xref/0.html) is an old static analysis tool for CL code.

## Conf

Linux .conf configuration files may vary in format, but many popular services offer a way to check the syntax of their particular configuration files.

### Apache

`apache2 -t`

### Exim

`exim -bV`

### CUPS

`cupsd -f -t`

### dhcpd

`dhcpd (-t -cf) | (-T -lf)`

### Lighttp

`lighttpd -t`

### MySQL

`mysqld --help --verbose --skip-networking`

### Nagios

`nagios -v`

### named

`named-checkconf`

`named-checkzone`

### Nginx

`nginx -t`

### ntp

`ntpd -n | -d`

### pf

`pfctl -n`

### Postfix

`postfix check`

### proftpd

`proftpd -t`

### rsyslogd

`rsyslogd -c4 -N 1`

### Samba

`testparm -v`

### slapd

`slapd -Tt`

### SQL (PostgreSQL, MySQL, MSSQL, ...)

* SQL implementations tend to include an `EXPLAIN`... statement which can validate syntax for individual statements.
* [prql](https://github.com/mcandre/prql) is a command line SQL syntax validator for SQL scripts.

### Squid

`squid -k (check | parse)`

### sshd

`sshd -t | -T`

### syslogd

`syslogd -d`

### tcpd

`tcpdchk -a | -d | -i | -v`

### Upstart

```
eval `dbus-launch --auto-syntax` && \
  find . -type f -name '*.conf' -exec init-checkconf {} \;
```

### varnishd

`varnishd -C`

### vsftpd

`vsftpd -olisten=NO`

## Coq

[Coq](http://coq.inria.fr/) is a proof assistant, requiring all programs to be logically valid.

## CSS

[csslint](https://github.com/stubbornella/csslint) for CSS files.

[minify](https://npmjs.org/package/minify) can help compress, CSS, JS, and HTML files.

[csstidy](http://csstidy.sourceforge.net/) can help compress CSS files.

## CSV

[csv-validator](https://github.com/digital-preservation/csv-validator) verifies CSV data against a given CSV schema.

## D

[gdc](http://dlang.org/) offers a built-in `-Wall` flag for additional warnings.

## Dart

`pub publish` offers a `--dry-run` option.

## Debian packages

[Lintian](https://lintian.debian.org/) checks for bugs and policy violations in .deb packages.

## DNS

[Dlint](http://freecode.com/projects/Dlint) analyzes DNS records.

## Docker

[dockerlint](https://www.npmjs.com/package/dockerlint)

## Elisp

[elisp-lint](https://github.com/nschum/elisp-lint)

[elint](http://repo.or.cz/emacs.git/blob/HEAD:/lisp/emacs-lisp/elint.el)

## ePUB

[epubcheck](https://github.com/IDPF/epubcheck) analyzes .epub files for errors.

## Erlang

[erl_tidy](http://www.erlang.org/doc/man/erl_tidy.html), a library that comes with Erlang, attempts to automatically change unidiomatic code.

[ehrlich](https://github.com/mcandre/ehrlich) provides a safer linter that does NOT automatically change your code.

[dialyzer](http://www.erlang.org/doc/man/dialyzer.html), a tool that comes with Erlang, helps detect type errors.

[elvis](https://github.com/inaka/elvis) is an Erlang style checker.

## F#

[fantomas](https://github.com/dungpa/fantomas)

## File systems

[fslint](http://www.pixelbeat.org/fslint/) can identify and correct errors in file systems.

[Disk Utility](https://support.apple.com/kb/HT1782) can repair HFS/HFS+ partitions.

[gParted](http://gparted.sourceforge.net/) can check for errors in several file systems.

[fixmbr Windows](http://web.archive.org/web/20171024104649/http://www.microsoft.com/resources/documentation/windows/xp/all/proddocs/en-us/bootcons_fixmbr.mspx?mfr=true) is a DOS tool for repairing boot sectors, available in Recovery mode in Windows installation media.

[fixmbr Linux](https://launchpad.net/~lenski/+archive/ms-sys/+packages) is a Linux tool for repairing boot sectors, part of the ms-sys package.

## Fortran

[fortranlint](http://stellar.cleanscape.net/products/fortranlint/)

## Go

The standard `go` command offers `go fmt` and `go vet` for styling and checking package integrity.

[goimports](https://godoc.org/golang.org/x/tools/cmd/goimports) supplements `go fmt` by organizing imports.

[golint](https://github.com/bytbox/golint) was an early stage Go linter.

[golang/lint](https://github.com/golang/lint)

[errcheck](https://github.com/kisielk/errcheck) identifies unchecked errors. In particular, the `-blank` flag (disabled by default) identifies errors assigned to `_`.

[nakedret](https://github.com/alexkohler/nakedret) identifies named returns, which often present unexpected behavior that can obfuscate error messages. Recommended usage: `nakedret -l 0 ./...`

[opennota/check](https://github.com/opennota/check) includes linters for reducing in-memory and in-transit struct size; identifying unused struct fields; and identifying unused global variables and constants.

[megacheck](https://github.com/dominikh/go-tools/tree/master/cmd/megacheck) runs staticcheck, gosimple, and unused.

[staticcheck](https://github.com/dominikh/go-tools/tree/master/cmd/staticcheck) adds additional checks compared to the built-in `go vet` tool.

[gosimple](https://github.com/dominikh/go-tools/tree/master/cmd/gosimple) recommends more idiomatic code forms.

[unused](https://github.com/dominikh/go-tools/tree/master/cmd/unused) reports some unused Go code elements.

[gometalinter](https://github.com/alecthomas/gometalinter) incorporates several linters in one, though one sub-linter `gotype` appears to be broken for `vendor/`ed Go 1.5+ code, so ensure that gotype is disabled, such as with `gometalinter --disable=gotype`.

## Groovy

[CodeNarc](http://codenarc.sourceforge.net)

## Haskell

[GHC](http://www.haskell.org/platform/), the official Haskell compiler, is renown for producing correct programs, though its strict type system.

[hlint](https://github.com/ndmitchell/hlint) displays a refactored version of your code, helping users more quickly resolve warnings.

## HTML

[W3C Validator](http://validator.w3.org/) is an online service for linting HTML, XML, and CSS data.

[tidy](http://tidy.sourceforge.net/) can lint HTML files.

[linklint](http://linklint.org/) checks hyperlinks.

## Java

[javac](http://www.oracle.com/technetwork/java/javase/downloads/index.html) offers a `-Xlint` option to print additional warnings. The [maven-compiler-plugin](https://maven.apache.org/plugins/maven-compiler-plugin/compile-mojo.html) can be configured to automatically pass `-Xlint` to the underlying Java compiler every time a project is built.

In Java 8, javac will feature an `-Xdoclint` option to identify undocumented code.

[CheckStyle](http://checkstyle.sourceforge.net/), with decent CLI support, as well as decent Maven support, through [maven-checkstyle-plugin](http://maven.apache.org/plugins/maven-checkstyle-plugin/). Checkstyle also supports identifying undocumented code, through its [JavaDoc](http://checkstyle.sourceforge.net/config_javadoc.html) settings.

[FindBugs](http://findbugs.sourceforge.net/) is an old Java linter, but has kept up with Java advances (for example, by offering a standard Gradle plugin).

[PMD](http://pmd.sourceforge.net/) detects flaws and duplicated code.

[Error-prone](https://github.com/google/error-prone) catches common Java mistakes as compile-time errors.

[Android lint](http://tools.android.com/tips/lint) checks Android source files for potential bugs and optimization improvements for correctness, security, performance, usability, accessibility, and internationalization.

[Infer](http://fbinfer.com/) is a static program analyzer for Java, C, and Objective-C, written in OCaml.

## JavaScript / Node.js

[ESLint](http://eslint.org) is a pluggable and configurable javascript linter that aims to fix the non-extensibility issues of JSHint and JSLint.

[JSHint](http://jshint.com/) is far and away the best modern linter available. It's simultaneously easy to use, and highly customizable; offering global and directory specific `.jshintrc` files for rule configuration; and global and directory specific `.jshintignore` files for ignoring certain files and directories, trimming down `jshint`'s output to exactly what you want to see.

[JSLint](http://jslint.com/) helps coders match the code style described in [JavaScript: The Good Parts](http://www.amazon.com/JavaScript-Good-Parts-Douglas-Crockford/dp/0596517742/).

[JSLint Errors](http://linterrors.com/js) explains warnings you may see from JSHint or JSLint.

[CLosure Compiler](https://developers.google.com/closure/) refactors code to improve performance.

[Closure Linter](https://pypi.python.org/pypi/closure_linter/) checks JavaScript for conformance to the Google Style Guide.

[Code Conventions for the JavaScript Programming Language](http://javascript.crockford.com/code.html) is a document detailing community standards for JavaScript code style.

[CoffeeScript](http://coffeescript.org/) is a compiles-to-JavaScript language designed to enforce good JavaScript coding habits at compiler level.

[npm-package-json-lint](https://github.com/tclindner/npm-package-json-lint) is a configurable linter to enforce standards in npm package.json files.

## JPEG

[jpegtran](http://jpegclub.org/jpegtran/) manipulates .jpg files.

## JSON

[json.py](http://docs.python.org/2/library/json.html) is a built-in Python module, offering a `-mjson.tool` option for linting JSON files.

[jq](http://stedolan.github.io/jq/) isn't a linter per-se, but jq can prettify JSON for creating more readable code examples.

[jsonschemalint](https://github.com/nickcmaynard/jsonschemalint) verifies JSON data against a given JSON schema.

## LaTeX

[lacheck](http://manpages.ubuntu.com/manpages/xenial/en/man1/lacheck.1.html) comes with LaTeX.

[style-check.rb](http://www.cs.umd.edu/~nspring/software/style-check-readme.html) is a LaTeX checker written in Ruby.

## Lua

`luac` offers a `-p` option to skip output file generation, useful for checking syntax without altering any files.

[luac](http://www.lua.org/manual/4.0/luac.html) offers a built-in `-p` option for syntax validation..

[lualint](https://github.com/philips/lualint) is an early Lua linter.

[lua-checker](https://code.google.com/p/lua-checker/) is another old Lua linter.

[luainspect](http://lua-users.org/wiki/LuaInspect) is yet another dead linter.

## Make

make offers a `-n` dry run option, though sometimes commands are still printed. Use `make -n 1>/dev/null` to suppress this output. Of course, this represents UNIX sh syntax, so redirect stdout to the null device in Windows syntax with `1>NUL` when in Windows.

Ironically, `make -n` would fail as a `lint:` task if the Makefile *does* happen to contain syntax errors. If this paradox bothers you, consider linting this Makefile from a separate Makefile, process, build system, etc. Or realize that you will receive an appropriate exist status either way!

make also offers a `--warn-undefined-variables` flag, often paired with `-n`, for warning when make variables are referenced but not defined.

[checkmake](https://github.com/mrtazz/checkmake) provides experimental analysis for Makefiles.

[mint](https://github.com/softprops/mint) is another linter for Makefiles.

## Markdown

[remark](https://github.com/remarkjs/remark-lint) checks markdown files for various errors.

## MP3

[mp3check](https://code.google.com/p/mp3check/) analyzes .mp3 files for errors.

## Objective C

[clang](http://clang.llvm.org/) offers built-in options `-Wall`, `-Wextra`, `-Wmost`, and `-Weverything` for showing additional compiler warnings.

[OCLint](http://oclint.org/) can lint ObjC, C, and C++ code.

[Infer](http://fbinfer.com/) is a static program analyzer for Java, C, and Objective-C, written in OCaml.

## OCaml

[mascot](http://mascot.x9c.fr/)

## Pascal

[fpc](http://www.freepascal.org/) offers a `-vw` flag to show additional warnings.

## Perl

[perl](http://www.perl.org/) offers extra warnings through the `use warnings;` (`#!/usr/bin/env perl -w`) and `use strict;` options.

[perltidy](http://perltidy.sourceforge.net/) generates a recommended refactored version of your code.

[perlcritic](https://metacpan.org/pod/perlcritic) applies rules based on O'Reilly Perl Best Practices.

[Perl Best Practices](http://shop.oreilly.com/product/9780596001735.do) is a textbook of recommended Perl coding conventions.

## PHP

[php](http://php.net/) comes with a built-in `-l` option to check for valid syntax.

[PHPMD](http://phpmd.org/) is a configurable frontend for static checks.

[PHP Code Sniffer](http://pear.php.net/package/PHP_CodeSniffer) checks .php, .js, and .css code for style.

[PSR-Huh?](http://net.tutsplus.com/tutorials/php/psr-huh/) is a document detailing community standards for PHP code style.

[PEAR Coding Standards](http://pear.php.net/manual/en/standards.php) is a collection of documents detailing community standards for PHP code style.

[CodeIgniter General Style and Syntax](http://ellislab.com/codeigniter/user-guide/general/styleguide.html) is another document offering PHP code style tips.

## PNG

[pngcheck](http://www.libpng.org/pub/png/apps/pngcheck.html) analyzes .png files for errors.

## PostgreSQL

[pgsanity](https://github.com/markdrago/pgsanity) verifies the correctness of PostgreSQL query syntax.

## Puppet

[puppet-lint](http://puppet-lint.com/) checks Puppet scripts for proper style.

## Python

[PyLint](http://www.pylint.org/) is fast and customizable.

[PyFlakes](https://pypi.python.org/pypi/pyflakes) offers few configuration options.

[PyChecker](http://pychecker.sourceforge.net/) requires executing code in order to analyze it.

[flake8](https://pypi.python.org/pypi/flake8) is a meta linter for Python, including PyFlakes, pep8, and McCabe.

[flake8-quotes](https://github.com/zheller/flake8-quotes) is a plugin for flake8 that enforces single vs double quotes.

[bandit](https://github.com/openstack/bandit) security focused Python static analyzer. Your mileage may vary, regarding the usefulness of its warnings. (For example, if your application intends to open an SSH connection, then it is not particularly helpful for bandit to complain about open SSH connections.)

[pep8](https://pypi.python.org/pypi/pep8/) checks Python code for PEP8 conformance.

[pep257](https://pypi.python.org/pypi/pep257/) checks Python code for PEP257 docstring conformance.

[Python Style Guide](http://www.python.org/doc/essays/styleguide/) is a collection of documents for community standards for Python code style.

[safety](https://pypi.org/project/safety/) identifies installed pip packages known to include vulnerabilities.

[wemake-python-styleguide](https://github.com/wemake-services/wemake-python-styleguide) is the strictest and most opinionated python linter ever.

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

[rails_upgrade](https://github.com/rails/rails_upgrade) helps Rails 2 code upgrade to Rails 3.

[ruby-lint](https://github.com/YorickPeterse/ruby-lint) relies on the pure Ruby [parser](https://rubygems.org/gems/parser), so it may lag behind in supported Ruby version syntaxes.

## Rust

[rustc](http://www.rust-lang.org/), the Rust compiler, offers a `-Wall` option for additional warnings.

[clippy](https://github.com/rust-lang-nursery/rust-clippy) is a Rust linter.

## Sass

[sass-lint](https://github.com/sasstools/sass-lint) is a Sass/SCSS linter.

[scss-lint](https://github.com/brigade/scss-lint) is a Sass/SCSS and CSS linter.

## Scala

The [scalac](http://www.scala-lang.org/old/sites/default/files/linuxsoft_archives/docu/files/tools/scalac.html) compiler offers optional `-Xlint` and `-deprecation` warnings.

[Scalastyle](http://www.scalastyle.org/) offers CLI, SBT, and Maven interfaces to a flexible, extensible Scala linter.

[Wartremover](https://github.com/puffnfresh/wartremover) is a flexible Scala code linting tool.

[Scapegoat](https://github.com/sksamuel/sbt-scapegoat) is a compiler plugin for static code analysis.

[Abide](https://github.com/scala/scala-abide) is a library for quick scala code checking and validation by the compiler developers.

[Linter](https://github.com/HairyFotr/linter) is a static analysis compiler plugin which adds various compile-time checks.

## sh / shell / bash

Many shells offer a `-n` option for validating syntax, e.g. `bash -n`, `zsh -n`, `ksh -n`, ...

Note that `sh -n` on many systems actually expands to `bash -n`, `ksh -n`, etc. as `/bin/sh` is usually symlinked to superset shells. Observers keen to guarantee that their portable sh scripts are pure POSIX and not bash scripts, can either run `sh -n` on a system with a bare bones `/bin/sh`, such as Alpine Linux, Busybox, etc., either on bare metal or Docker.

[slick](https://github.com/mcandre/slick) is a cross-platform POSIX `-n` checker. Substitute for `sh -n` for more reliable linting!

[shlint](https://github.com/duggan/shlint) is a meta-linter, which runs `-n` checks, for any shells available, as well as `checkbashisms`.

[Shellcheck](http://www.shellcheck.net/) is a bash linter written in Haskell.

[checkbashisms.rb](http://manpages.ubuntu.com/manpages/xenial/en/man1/checkbashisms.1.html) is a sh linter that reports bashisms.

[Bashate](https://pypi.python.org/pypi/bashate/) is a pep8-like linter for bash scripts.

[shfmt](https://github.com/mvdan/sh) provides consistent styling for shell scripts.

[stank](https://github.com/mcandre/stank) offers several utilities for A) identifying POSIXy shell scripts among large directories of source files and B) warnings for oddities such as shebang mismatches.

## Smalltalk

[SmallLint](http://c2.com/cgi/wiki?SmallLint) integrates with the OmniBrowser to lint Smalltalk code.

## Snort

[pulledpork](https://github.com/shirkdog/pulledpork) helps manage Snort rulesets.

## Swift

[swiftlint](https://github.com/realm/SwiftLint) encourages better Swift style

## Travis

[travis-lint](https://github.com/travis-ci/travis-lint) checks `.travis.yml` for errors.

## Typescript

[TSLint](https://palantir.github.io/tslint/) checks your TypeScript code for readability, maintainability, and functionality errors.

## XML

[xmllint](https://en.wikipedia.org/wiki/Libxml2) is provided as part of the `libxml2` package.

## YAML

[yamllint](https://github.com/adrienverge/yamllint) is a syntax checker and linter for YAML source.

# Continuous Integration

A [Jenkins](http://jenkins-ci.org/) server can generate HTML linter reports for each new code commit.

[Guard](http://guardgem.org/) + [guard-shell](https://github.com/guard/guard-shell) can monitor local code files, automatically outputting linter warnings as the programmer edits his code, simulating a local continuous integration server.

A [make](https://www.gnu.org/software/make/) task can bundle several linters together (e.g. `csslint`, HTML `tidy`, `jshint`), to lint different kinds of files all at once.

[git hooks](http://git-scm.com/book/en/Customizing-Git-Git-Hooks) can be added to a git repo, preventing a programmer from submitting his work until it passes a configured suite of linters.

# See Also

https://en.wikipedia.org/wiki/List_of_tools_for_static_code_analysis
