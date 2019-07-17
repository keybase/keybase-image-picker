# Keybase fork specifics

This is from a git subtree. See [keybase/expo](https://github.com/keybase/expo) for the source repo.

### How do I update this?

Some important points:

- keybase/expo#master is a full fork of expo/expo.
- keybase/expo#keybase-image-picker is a subtree of the packages/expo-image-picker
- keybase/keybase-image-picker is a repo that is basically just the keybase/expo#keybase-image-picker branch
  - Keeping this as another repo lets lets our downloads stay small when we run `yarn`

The Update flow:

1. Update `keybase/expo#keybase-image-picker-full` as you normally would.
1. Inside `keybase/expo#keybase-image-picker-full`, run `git remote add keybase-image-picker git@github.com:keybase/keybase-image-picker.git`.
1. Inside `keybase/expo#keybase-image-picker-full`, run `git subtree push --prefix=packages/expo-image-picker keybase-image-picker master`. This pushes the changes in the expo repo to the keybase-image-picker sub tree repo to the given `<feature-branch>`

### Useful links

https://git-memo.readthedocs.io/en/latest/subtree.html
