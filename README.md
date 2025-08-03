# Release Instructions

## Creating Your First Release

Since there's no release yet, you need to create one first. Here are your options:

## Option 1: Quick Manual Release (Recommended for first release)

```bash
# 1. Commit all your changes
git add .
git commit -m "feat: initial CLI implementation"
git push origin main

# 2. Create and push a tag
git tag v0.0.1
git push origin v0.0.1
```

The GitHub Action will automatically:
- Build the TypeScript code
- Create the npm package (.tgz file)
- Create a GitHub release with the package attached

## Option 2: Using GitHub UI

1. Go to your repository on GitHub
2. Click on "Releases" (right side of the page)
3. Click "Create a new release"
4. Click "Choose a tag" and type `v0.0.1`
5. Select "Create new tag: v0.0.1 on publish"
6. Fill in release title: "v0.0.1"
7. Add release notes
8. Click "Publish release"

This will trigger the workflow to build and attach the package.

## Option 3: Using GitHub Actions

1. Go to the Actions tab in your repository
2. Select "Build and Release" workflow
3. Click "Run workflow"
4. Select the branch (main)
5. Choose bump type (patch/minor/major)
6. Click "Run workflow"

## After Release is Created

Once the release is created, external developers can use:

```bash
# Direct download from release
npx https://github.com/anyplatform/platform/releases/download/v0.0.1/anyplatform-platform-0.0.1.tgz create my-app
```

## Important Notes

1. The `/latest/` URL pattern only works after at least one release is marked as "Latest release" on GitHub
2. For the first release, always use the specific version URL
3. The package file will be named exactly: `anyplatform-platform-0.0.1.tgz`

## Verifying the Release

After creating the release, check:

1. Go to https://github.com/anyplatform/platform/releases
2. You should see your release with the .tgz file attached
3. Click on the .tgz file to verify it downloads
4. The download URL should be:
   ```
   https://github.com/anyplatform/platform/releases/download/v0.0.1/anyplatform-platform-0.0.1.tgz
   ```

## Troubleshooting

### Error: 404 Not Found
- The release doesn't exist yet - create it first using one of the methods above
- Check the exact URL and version number
- Verify the .tgz file is attached to the release

### Package name not valid
- Make sure you're using the full URL to the .tgz file
- Don't use `/latest/` until you have a release marked as latest

### Workflow didn't create release
- Check Actions tab for any errors
- Ensure the tag starts with 'v' (e.g., v0.0.1)
- Verify package.json has the correct version (0.0.1)
