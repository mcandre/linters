# linters: a community wiki for improving code quality

# What is a linter?

Originally, `lint` was a tool for scanning C code for potentially risky lines of code.

The C compiler already includes some checks for risky code, such as scanning to making sure that function signatures match. And unit testing adds dynamic checks to verify the behavior of a running program. Beyond these checks, `lint` adds even more checks, that neither the compiler nor the tests scan.

By *statically* analyzing the code itself before compilation, programmers could maintain a higher level of code discipline, increasing the reliability of the code in multiple compilers and environments.

As time went on, static code analysis was nearly eclipsed in attention, by dynamic analysis: [unit tests](https://en.wikipedia.org/wiki/Unit_test), that examine how code behaves for different inputs and corner cases. But the linting practice has restored, and spread to more languages--C++ and beyond.

Today, linters are used to supplement unit tests, serving primarily as low priority style checkers. Linters are being written for many programming languages and document formats, detailed below.

[Wikipedia:List of tools for static analysis](http://en.wikipedia.org/wiki/List_of_tools_for_static_code_analysis)

This document often interprets the term "linter" in a wide sense, to include resources for SAST, SCA, memory management validators, code formatters, and style guides.

# Linters

Many compilers include an option like `-Wall` to turn on warnings, `-Wextra` for even more warnings, and also `-Werror` to treat warnings as errors, preventing dirty code from compiling.

## *

[anorack](https://github.com/jwilk/anorack) is a specialized spell-checker that finds incorrect indefinite articles.

[astyle](http://astyle.sourceforge.net/) can help enforce a uniform coding style in a large software project.

[check-all-the-things](https://anonscm.debian.org/cgit/collab-maint/check-all-the-things.git/plain/doc/README) is a command-line tool for automatically running many static analysis and similar tools over packages and upstream codebases.

[checkov](https://www.checkov.io/) scans cloud resources for CVE's, including Kubertes and Terraform projects.

[cicada](https://github.com/mcandre/cicada) scans environments for software components at risk of falling off of LTS security support timelines.


[Code Climate](https://codeclimate.com/) is a paid web service for automatically generating code quality reports.

[eclint](https://github.com/jedmao/eclint) can derive the code style used in a project, and save it as a dotfile for use in other projects.

[driftwood](https://github.com/trufflesecurity/driftwood) looks up private keys in common registries.

[editorconfig](http://editorconfig.org/) is an editor-agnostic configuration system for code styling.

[editorconfig-cli](https://github.com/amyboyd/editorconfig-cli) is a Go-based editorconfig linter.

[editorconfig-tools](https://www.npmjs.com/search?q=editorconfig-tools) is a command line linter against editorconfig rules.

[dotenv-linter](https://github.com/wemake-services/dotenv-linter) finds errors and stylistic violations in `.env` files.

[KICS](https://kics.io/) scans Docker and Kubernetes resources.

[lint-spaces](https://github.com/schorfES/node-lintspaces) checks line endings and indentation.

[pfff](https://github.com/facebook/pfff/) is a collection of tools by Facebook for analyzing code style, with support for multiple programming languages.

[proselint](https://github.com/amperser/proselint/) is a linter for usage and style errors in English prose.

[Sonarqube](http://www.sonarqube.org/) is a cross-programming language linting system.

[Phabricator Contributing Guide](http://www.phabricator.com/docs/phabricator/article/Contributor_Introduction.html#suggested-reading) offers coding standards generally, as well as for PHP, and JavaScript code specifically.

[google-styleguide](https://code.google.com/p/google-styleguide/) is a collection of documents detailing Google's preferred code style, for a variety of programming languages and data formats.

[Hemingway](http://www.hemingwayapp.com/) is a software application for improving the readability of English text. By using Hemingway, we can make our documentation more understandable for others.

[Mozilla Coding Style](https://developer.mozilla.org/en-US/docs/Developer_Guide/Coding_Style?redirectlocale=en-US&redirectslug=Mozilla_Coding_Style_Guide) is a document detailing Mozilla's preferred coding style.

[MSDN Library: Coding Techniques and Programming Practices](http://msdn.microsoft.com/en-us/library/aa260844(v=vs.60).aspx) offers general tips for coding.

[Microsoft patterns & practices](http://pnp.azurewebsites.net/en-us/) are recommended for .NET projects.

[MSDN Library: Design Guidelines for Class Library Developers](http://msdn.microsoft.com/en-us/library/czefa0ke%28VS.71%29.aspx) presents guidelines for .NET library developers.

[sunshine](https://github.com/mcandre/sunshine) validates chmod permissions, such as for SSH files.

[trufflehog](https://github.com/trufflesecurity/trufflehog) reports credential exposure.

[Vale](https://github.com/errata-ai/vale) validates English text against a wide variety of prebuilt style guides, and is easily and highly configurable.

[vuls](https://vuls.io/) scans assorted computing environments for CVE's.

[Web Package Update Checker](https://github.com/fulldecent/web-puc) validates web projects to ensure they use the latest available versions of web packages (like Bootstrap, Font Awesome, JQuery).

[write-good](https://github.com/btford/write-good) validates english prose with the aim of helping developers write better code.

## SLOC

[sloccount](http://www.dwheeler.com/sloccount/) is an older line counter.

[cloc](https://github.com/AlDanial/cloc) is a newer line counter with support for more programming languages.

[wc](https://pubs.opengroup.org/onlinepubs/9699919799/utilities/wc.html) is a line counter for UNIX systems.

## Android

[lint](http://developer.android.com/tools/help/lint.html) is a tool for static analysis of Android projects.

## Awk

[gawk](http://www.gnu.org/software/gawk/manual/gawk.html) has a `--lint` option for checking script compatibility with other awk implementations.

## BitTorrent

[torrentcheck](https://sourceforge.net/projects/torrentcheck/) verifies file download hashes against .torrent files.

## C

[splint](http://lclint.cs.virginia.edu/) has largely replaced the old `lint` tool, offering the same old checks, as well as additional security checks.

[lint](https://en.wikipedia.org/wiki/Lint_%28software%29) the original C static analysis tool.

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

[cpplint](https://pypi.python.org/pypi/cpplint/) is provided as part of the `google-styleguide`. Note that cpplint is a Python tool, which means you would also want to run Python SCA tools on all environments that install cpplint.

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

[roslyn-analyzers](https://github.com/dotnet/roslyn-analyzers) is a collection of static analyzers developed by Microsoft with the Roslyn APIs.

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

### Homebrew

`brew doctor`

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

## Ansible

[ansible-later](https://ansible-later.geekdocs.de/) checks Ansible playbooks.

[ansible-lint](https://ansible-lint.readthedocs.io/) is a classic Ansible linter.

[Lockdown](https://www.lockdownenterprise.com/) provides recommendations for securing Ansible playbooks.

[steampunk-spotter](https://pypi.org/project/steampunk-spotter/) offers additional checks for Ansible playbooks.

## Arch

[arch-audit](https://github.com/ilpianista/arch-audit) generates CVE reports for Arch Linux.

## BSD

[pkg-audit](https://man.freebsd.org/cgi/man.cgi?query=pkg-audit&sektion=8&n=1) generates CVE reports for FreeBSD, DragonflyBSD, and HardenedBSD.

[pkg_admin](https://man.netbsd.org/pkg_admin.1) provides an `audit` subcommand for generating CVE reports on NetBSD.

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

[Docker First Aid Kit](https://github.com/mcandre/docker-first-aid-kit) provides performance and general advice for Docker newbies.

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

## GIF

[buttery](https://github.com/mcandre/buttery) is a GIF loop editor, with an option to validate basic GIF format file integrity.

## Go

The standard `go` command offers `go fmt` and `go vet` for styling and checking package integrity.

[goimports](https://godoc.org/golang.org/x/tools/cmd/goimports) supplements `go fmt` by organizing imports.

[golint](https://github.com/bytbox/golint) was an early stage Go linter, since deprecated in favor of staticcheck.

[golang/lint](https://github.com/golang/lint)

[errcheck](https://github.com/kisielk/errcheck) identifies unchecked errors. In particular, the `-blank` flag (disabled by default) identifies errors assigned to `_`.

[nakedret](https://github.com/alexkohler/nakedret) identifies named returns, which often present unexpected behavior that can obfuscate error messages. Recommended usage: `nakedret -l 0 ./...`

[opennota/check](https://github.com/opennota/check) includes linters for reducing in-memory and in-transit struct size; identifying unused struct fields; and identifying unused global variables and constants.

[megacheck](https://github.com/dominikh/go-tools/tree/master/cmd/megacheck) runs staticcheck, gosimple, and unused.

[staticcheck](https://staticcheck.io/) adds additional checks compared to the built-in `go vet` tool.

[gosimple](https://github.com/dominikh/go-tools/tree/master/cmd/gosimple) recommends more idiomatic code forms.

[unconvert](https://github.com/mdempsky/unconvert) detects redundant conversions.

[unused](https://github.com/dominikh/go-tools/tree/master/cmd/unused) reports some unused Go code elements.

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

[Android lint](http://tools.android.com/tips/lint) checks Android source files for potential bugs and optimization improvements for correctness, security, performance, usability, accessibility, and internationalization.

[CheckStyle](http://checkstyle.sourceforge.net/), with decent CLI support, as well as decent Maven support, through [maven-checkstyle-plugin](http://maven.apache.org/plugins/maven-checkstyle-plugin/). Checkstyle also supports identifying undocumented code, through its [JavaDoc](http://checkstyle.sourceforge.net/config_javadoc.html) settings.

[Error-prone](https://github.com/google/error-prone) catches common Java mistakes as compile-time errors.

[FindBugs](http://findbugs.sourceforge.net/) is an old Java linter, but has kept up with Java advances (for example, by offering a standard Gradle plugin).

[google-java-format](https://github.com/google/google-java-format) formats Java code according to the Google Style Guide.

[Infer](http://fbinfer.com/) is a static program analyzer for Java, C, and Objective-C, written in OCaml.

[javac](http://www.oracle.com/technetwork/java/javase/downloads/index.html) offers a `-Xlint` option to print additional warnings. The [maven-compiler-plugin](https://maven.apache.org/plugins/maven-compiler-plugin/compile-mojo.html) can be configured to automatically pass `-Xlint` to the underlying Java compiler every time a project is built.

In Java 8, javac will feature an `-Xdoclint` option to identify undocumented code.

[PMD](http://pmd.sourceforge.net/) detects flaws and duplicated code.

## JavaScript / Node.js

[CLosure Compiler](https://developers.google.com/closure/) refactors code to improve performance.

[Closure Linter](https://pypi.python.org/pypi/closure_linter/) checks JavaScript for conformance to the Google Style Guide.

[Code Conventions for the JavaScript Programming Language](http://javascript.crockford.com/code.html) is a document detailing community standards for JavaScript code style.

[CoffeeScript](http://coffeescript.org/) is a compiles-to-JavaScript language designed to enforce good JavaScript coding habits at compiler level.

[ESLint](http://eslint.org) is a pluggable and configurable javascript linter that aims to fix the non-extensibility issues of JSHint and JSLint.

[JSHint](http://jshint.com/) is far and away the best modern linter available. It's simultaneously easy to use, and highly customizable; offering global and directory specific `.jshintrc` files for rule configuration; and global and directory specific `.jshintignore` files for ignoring certain files and directories, trimming down `jshint`'s output to exactly what you want to see.

[JSLint](http://jslint.com/) helps coders match the code style described in [JavaScript: The Good Parts](http://www.amazon.com/JavaScript-Good-Parts-Douglas-Crockford/dp/0596517742/).

[JSLint Errors](http://linterrors.com/js) explains warnings you may see from JSHint or JSLint.

[npm-package-json-lint](https://github.com/tclindner/npm-package-json-lint) is a configurable linter to enforce standards in npm package.json files.

[rslint](https://rslint.org/) is a fast JavaScript linter.

[standardjs](https://standardjs.com/) is a JavaScript linter and formatter.

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

[luacheck](https://github.com/mpeterv/luacheck) is a Lua linter.

[lualint](https://github.com/philips/lualint) is an early Lua linter.

[lua-checker](https://code.google.com/p/lua-checker/) is another old Lua linter.

[luainspect](http://lua-users.org/wiki/LuaInspect) is yet another dead linter.

## Make

make offers a `-n` dry run option, though sometimes commands are still printed. Use `make -n 1>/dev/null` to suppress this output. Of course, this represents UNIX sh syntax, so redirect stdout to the null device in Windows syntax with `1>NUL` when in Windows.

GNU make offers an additional `--warn-undefined-variables` flag to check for... undefined variables.

[unmake](https://github.com/mcandre/unmake) is a POSIX makefile linter focusing on portability.

## Markdown

[markdownlint](https://github.com/DavidAnson/markdownlint) enforces standards for Markdown and CommonMark files via Node.js or [Ruby](https://github.com/markdownlint/markdownlint)

[remark](https://github.com/remarkjs/remark-lint) checks Markdown files for various errors.

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

[cpan-audit](https://metacpan.org/dist/CPAN-Audit/view/script/cpan-audit) scans Perl projects for CVE's.

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

## pkgsrc

[pkglint](https://github.com/rillig/pkglint) checks `pkgsrc` projects, including BSD makefiles, embedded shell commands, and pkgsrc conventions.

## PNG

[pngcheck](http://www.libpng.org/pub/png/apps/pngcheck.html) analyzes .png files for errors.

## PostgreSQL

[pgsanity](https://github.com/markdrago/pgsanity) verifies the correctness of PostgreSQL query syntax.

## Puppet

[puppet-lint](http://puppet-lint.com/) checks Puppet scripts for proper style.

[vulnerability](https://forge.puppet.com/modules/enterprisemodules/vulnerability/readme) checks for Puppet CVE's.

## Python

[bandit](https://github.com/openstack/bandit) security focused Python static analyzer. Your mileage may vary, regarding the usefulness of its warnings. (For example, if your application intends to open an SSH connection, then it is not particularly helpful for bandit to complain about open SSH connections.)

[dlint](https://github.com/dlint-py/dlint)) is another security focused analyzer.

[flake8](https://pypi.python.org/pypi/flake8) is a meta linter for Python, including PyFlakes, pep8, and McCabe.

[flake8-quotes](https://github.com/zheller/flake8-quotes) is a plugin for flake8 that enforces single vs double quotes.

[pep8](https://pypi.python.org/pypi/pep8/) checks Python code for PEP8 conformance.

[pep257](https://pypi.python.org/pypi/pep257/) checks Python code for PEP257 docstring conformance.

[PyChecker](http://pychecker.sourceforge.net/) requires executing code in order to analyze it.

[PyLint](http://www.pylint.org/) is fast and customizable.

[PyFlakes](https://pypi.python.org/pypi/pyflakes) offers few configuration options.

[Python Style Guide](http://www.python.org/doc/essays/styleguide/) is a collection of documents for community standards for Python code style.

[refurb](https://github.com/dosisod/refurb) recommends Python idioms.

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

[fasterer](https://github.com/DamirSvrtan/fasterer) provides performance tips.

[flog](http://ruby.sadi.st/Flog.html) identifies the most complex code in your codebase.

[churn](https://github.com/danmayer/churn) looks at version control history to look for frequently changing code, often a sign of poor coding.

[laser](https://github.com/michaeledgar/laser) provides basic detection for logic errors.

[metric_fu](https://github.com/metricfu/metric_fu) scans with a suite of Ruby linters.

[laser](https://github.com/michaeledgar/laser) is a slightly out of date Ruby linter.

[ruby-style-guide](https://github.com/bbatsov/ruby-style-guide) is a document describing community standards for Ruby code style.

[rails_upgrade](https://github.com/rails/rails_upgrade) helps Rails 2 code upgrade to Rails 3.

[ruby-lint](https://github.com/YorickPeterse/ruby-lint) relies on the pure Ruby [parser](https://rubygems.org/gems/parser), so it may lag behind in supported Ruby version syntaxes.

[rubycritic](https://github.com/whitesmith/rubycritic) provides HTML and CLI linting.

[standard](https://github.com/testdouble/standard) provides a Ruby formatter.

## Rust

[crev](https://github.com/crev-dev/cargo-crev) assists with dependency reviews.

[rustc](http://www.rust-lang.org/), the Rust compiler, offers a `-Wall` option for additional warnings.

[clippy](https://github.com/rust-lang-nursery/rust-clippy) is a Rust linter.

[cargo-audit](https://crates.io/crates/cargo-audit) scans Rust dependencies for vulnerabilities.

[rustfmt](https://github.com/rust-lang/rustfmt) for styling.

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

[checkbashisms.rb](http://manpages.ubuntu.com/manpages/xenial/en/man1/checkbashisms.1.html) is an unmaintained sh linter that reports bashisms. Because it is unmaintained, it features an inverted ROC curve.

[bashate](https://pypi.python.org/pypi/bashate/) is a pep8-like linter for bash scripts. Note that bashate is a Python tool, which means you would also want to run Python SCA tools on all environments that install bashate.

[shfmt](https://github.com/mvdan/sh) provides consistent styling for shell scripts.

[stank](https://github.com/mcandre/stank) offers several utilities for A) identifying POSIXy shell scripts among large directories of source files and B) warnings for oddities such as shebang mismatches.

## Smalltalk

[SmallLint](http://c2.com/cgi/wiki?SmallLint) integrates with the OmniBrowser to lint Smalltalk code.

## Snort

[pulledpork](https://github.com/shirkdog/pulledpork) helps manage Snort rulesets.

## Swift

[swiftlint](https://github.com/realm/SwiftLint) encourages better Swift style

## Terraform

`terraform validate` provides built-in suport for basic syntactical correctness.

[terrascan](https://runterrascan.io/) scans Terraform CVE's.

[tflint](https://github.com/terraform-linters/tflint) checks Terraform plans.

[tfsec](https://github.com/aquasecurity/tfsec) scans Terraform CVE's.

## Travis

[travis-lint](https://github.com/travis-ci/travis-lint) checks `.travis.yml` for errors.

## Typescript

[TSLint](https://palantir.github.io/tslint/) checks your TypeScript code for readability, maintainability, and functionality errors.

## XML

[xmllint](https://en.wikipedia.org/wiki/Libxml2) is provided as part of the `libxml2` package.

## YAML

[yamllint](https://github.com/adrienverge/yamllint) is a syntax checker and linter for YAML source. Note that yamllint is a Python tool, which means you would also want to run Python SCA tools on all environments that install yamllint.

# Continuous Integration

A [Jenkins](http://jenkins-ci.org/) server can generate HTML linter reports for each new code commit.

[Guard](http://guardgem.org/) + [guard-shell](https://github.com/guard/guard-shell) can monitor local code files, automatically outputting linter warnings as the programmer edits his code, simulating a local continuous integration server.

A [make](https://www.gnu.org/software/make/) task can bundle several linters together (e.g. `csslint`, HTML `tidy`, `jshint`), to lint different kinds of files all at once.

[git hooks](http://git-scm.com/book/en/Customizing-Git-Git-Hooks) can be added to a git repo, preventing a programmer from submitting his work until it passes a configured suite of linters.

# See Also

* [Awesome Linters](https://github.com/caramelomartins/awesome-linters)
* [Wikipedia List of tools for static code analysis](https://en.wikipedia.org/wiki/List_of_tools_for_static_code_analysis)
