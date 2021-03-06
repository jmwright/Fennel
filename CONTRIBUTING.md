# Guidelines for contributing to Fennel

Thanks for taking time to contribute to Fennel!

Please read this document before making contributions.

## Reporting bugs

* Check past and current issues to see if your problem has been run into before.
* If you can't find a past issue for your problem, or if the issues has been
  closed you should open a new issue. If there is a closed issue that is
  relevant, make sure to reference it.
* As with any project, include a comprehensive description of the problem and
  instructions on how to reproduce it. If it is a compiler or language bug,
  please try to include a minimal example. This means don't post all 200 lines
  of code from your project, but spend some time distilling the problem to just
  the relevant code.
* Add the `bug` label to the issue.

## Contributing Changes

If you want to contribute code to the project, please [send patches][1] to the
[mailing list][2]. (Note that you do not need to subscribe to the mailing list
in order to post to it.) We also accept code contributions on the
[GitHub mirror](https://github.com/bakpakin/Fennel) if you prefer not
to use email.

For large changes, please discuss it first either on the mailing list,
IRC/Matrix channel, or in the issue tracker before sinking time and effort into
something that may not be able to get merged.

* Branch off the `main` branch. The contents of this branch should be
  the same on Sourcehut as they are on the Github mirror. But make
  sure that `main` on your copy of the repo matches upstream.
* Include a description of the changes.
* If there are changes to the compiler or the language, please include
  tests. You can run tests with `make test`.
* Make sure that your changes will work on Lua versions 5.1, 5.2, 5.3, 5.4, and
  LuaJIT. Making fennel require LuaJIT or 5.2+ specific features is a
  non-goal of the project. In general, this means target Lua 5.1, but provide
  shims for where functionality is different in newer Lua versions. Running
  `make testall` will test against all supported versions, assuming they're
  installed. If you don't want to install every supported version of
  Lua, you can rely on the CI suite to test your patches.
* Be consistent with the style of the project. Please try to code moderately
  tersely; code is a liability, so the less of it there is, the better.
* For user-visible changes, include a description of the change in
  `changelog.md`. Changes that affect the compiler API should update `api.md`
  while changes to the built-in forms will usually need to update
  `reference.md` to reflect the new behavior.

If all goes well, we should merge your changes fairly quickly.

## Suggesting Changes

Informal discussion of changes is easiest on the IRC/Matrix channel, but the
mailing list can also be good for this. More serious proposals should go on the
mailing list or issue tracker. There is a possibility that there is already a
solution for your problems so be sure that there is a good use case for your
changes before opening an issue.

* Include a good description of the problem that is being solved.
* Include descriptions of potential solutions if you have some in mind.
* Add the appropriate labels to the issue. For new features, add `enhancement`.

[1]: https://man.sr.ht/git.sr.ht/send-email.md
[2]: https://lists.sr.ht/%7Etechnomancy/fennel
