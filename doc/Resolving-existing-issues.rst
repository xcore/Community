Resolving existing issues
=========================

As a next step beyond reporting issues, you can help the community resolve existing issues. If you check the open issues list in any repository, you’ll likely find issues already requiring attention. What can you do for these? Quite a bit, actually:
 
Verifying Issue Reports
-----------------------

For starters, it helps to just verify issue reports. Can you reproduce the reported issue on your own computer? If so, you can add a comment to the ticket saying that you’re seeing the same thing.  If something is very vague, can you help squish it down into something specific? Maybe you can provide additional information to help reproduce a issue, or eliminate needless steps that aren’t required to help demonstrate the problem.

If you find an issue report without a test, it’s very useful to contribute a failing test. This is also a great way to get started exploring the source code: looking at the existing test files will teach you how to write more tests. New tests are contributed like any other piece of code - see :doc:`Contributing-to-the-codebase`.

Anything you can do to make issue reports more succinct or easier to reproduce is a help to folks trying to write code to fix those issues – whether you end up writing the code yourself or not.

Fixing Other Peoples Code
-------------------------

To fix code in a repo you don't have push access to, you can simply fork it, fix it and then submit an issue with a link to the fork. If the fix looks good, you can then submit a pull request to the origin repo.

Some things to think about when submitting fixes:

*	Does the fix actually work?
*	Are you happy with the tests? Can you follow what they’re testing? Are there any tests missing?
*	Does the documentation still seem right to you?
*	Do you like the implementation? Can you think of a nicer or faster way to implement a part of their change?
*	Once you’re happy that the fix contains a good change, comment on the issue indicating your approval. Your comment should indicate that you like the change and what you like about it. Something like:

               I like the way you’ve restructured that code in uart_rx_impl.xc, much nicer. The tests look good too.

If your comment simply says “+1”, then odds are that other reviewers aren’t going to take it too seriously. Show that you took the time to review the fix.
