git-squash(1) -- squash N last changes up to a ref'ed commit
=============================================

## SYNOPSIS

`git-squash` [&lt;--squash-messages&gt;] &lt;source-branch|commit ref&gt; [&lt;commit-message&gt;]

## DESCRIPTION

  Produce the working after the squash has happened

## OPTIONS

  &lt;source-branch&gt;

  Branch to squash on the current branch.

  &lt;commit reference&gt;
  A commit reference (has to be from the current branch) can also be used as the
  first argument. A range of commits <sha>..HEAD will be squashed.

  &lt;--squash-msg&gt;

  Commit the squash result with the concatenated squashed committed messages.
  This option can not be used together with &lt;commit-message&gt;.

  &lt;commit-message&gt;

  If commit-message is given, commit the squash result, otherwise the squash remains just added to the index and is not committed.

## EXAMPLES

    $ git squash my-other-branch
    Updating a2740f5..533b19c
    Fast-forward
    Squash commit -- not updating HEAD
     my-changed-file | 1 +
     1 file changed, 1 insertion(+)
    $ git commit -m "New commit without a real merge"

    $ git squash HEAD~3 "Commit message"
    $ git squash --squash-msg @~3

## AUTHOR

Written by Jesús Espino &lt;<jespinog@gmail.com>&gt;

## REPORTING BUGS

&lt;<https://github.com/tj/git-extras/issues>&gt;

## SEE ALSO

&lt;<https://github.com/tj/git-extras>&gt;
