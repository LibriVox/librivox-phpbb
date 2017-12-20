# phpBB with LibriVox modifications

This is the code powering the [LibriVox forums](https://forum.librivox.org).
The legacy branch contains the old 3.0 version, in which official phpBB code
and LibriVox modifications were mixed into an unknowable mess. Master contains
the LibriVox changes on top of the latest phpBB release. It is periodically
rebased on top of the latest phpBB release. For example, to update from 3.2.0
to 3.2.1 while still keeping all the LibriVox commits at the top:

```bash
git rebase --onto release-3.2.1 release-3.2.0 master
git push -f
```

This assumes the [official phpBB remote](https://github.com/phpbb/phpbb) is
configured in your local git repository. It also means pulls from this
repository aren't always possible if a phpBB release rebase has been done
between two pulls. One should use `git reset --hard origin/master` instead.
