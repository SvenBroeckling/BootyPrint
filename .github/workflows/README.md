# GitHub Actions Workflows

To create a new release:

1. Update the version number in `package.json`
2. Update the `CHANGELOG.md` with the changes for the new version
3. Commit these changes
4. Create and push a tag for the release:

```bash
git tag v1.0.1
git push origin v1.0.1
```
