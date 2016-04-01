# git-hook-scripts

This is just a repository of useful `git` hook scripts that I've found and / or modified for use in various projects.

## Installation
Other (better) folks than I have written better documentation about installing a `git` hook than I.  Check out [the git documentation on git hooks](https://git-scm.com/book/en/v2/Customizing-Git-Git-Hooks) for more details.

### Hooks
1. pre-commit-reject-forbidden-code

   This bash script hook checks for the presence of certain undesirable code snippets in the code being checked in and
   rejects the commit if it contains any of the following:
   * console methods - the assumption is you should be using something else to handle logging,
     personally I like  [Bunyan](https://www.npmjs.com/package/bunyan "Bunyan npm page")
     * `console.log`
     * `console.warn`
     * `console.info`
     * `console.error`
   * `debugger`
   * `var_dump`
   * `print_r`
   * `fdescribe`
   * `ddescribe`
   * `fit`
   * `iit`