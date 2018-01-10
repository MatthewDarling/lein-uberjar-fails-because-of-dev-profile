# `lein uberjar` fails because of `:dev` profile

This project has
a
[snapshot dependency in the `:dev` profile](https://github.com/MatthewDarling/lein-uberjar-fails-because-of-dev-profile/blob/master/project.clj#L7). When
trying to create an uberjar, Leiningen exits because of that snapshot
dependency:

```
$ lein uberjar
Release versions may not depend upon snapshots.
Freeze snapshots to dated versions or set the LEIN_SNAPSHOTS_IN_RELEASE environment variable to override.
```

The
[documentation for Leiningen profiles](https://github.com/technomancy/leiningen/blob/master/doc/PROFILES.md#debugging) says
that uberjar should remove default profiles like `:dev`. However, here
we see that isn't entirely the case.

## License

Copyright © 2018 FIXME

Distributed under the Eclipse Public License either version 1.0 or (at
your option) any later version.
