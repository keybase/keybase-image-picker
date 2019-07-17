# Keybase fork specifics

This is from a git subtree. See [keybase/expo](https://github.com/keybase/expo) for the source repo.

### How do I update this?

Some important points:

- keybase/expo#master is a full fork of expo/expo.
- keybase/expo#keybase-image-picker is a subtree of the packages/expo-image-picker
- keybase/keybase-image-picker is a repo that is basically just the keybase/expo#keybase-image-picker branch
  - Keeping this as another repo lets lets our downloads stay small when we run `yarn`

The Update flow:

1. Update `keybase/expo` as you normally would.
1. Inside `keybase/keybase-image-picker`, set `git remote add upstream git@github.com:keybase/expo.git`
1. Inside `keybase/keybase-image-picker`, run `git pull upstream keybase-image-picker:master`

### Useful links

https://git-memo.readthedocs.io/en/latest/subtree.html
