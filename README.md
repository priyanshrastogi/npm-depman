# npm-depman

A guide to manage internal dependencies across different environments.

---

Use the following command to publish internal package

```
npm version prerelease --preid=env
npm publish --tag env
```

To use this internal dependency in the app, add this in package.json

```
"@priyanshrastogi/npm-depman-config": "env"
```

Replace `env` with either of `develop`, `staging` or `latest`.

The value of `env` can change based on the branch.

Caveat: You will have to delete package-lock.json/yarn-lock.json every time before installing the dependencies.
