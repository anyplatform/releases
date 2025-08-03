# AnyPlatform Releases

This repository hosts the distribution packages for AnyPlatform projects.

## Purpose

Since our main repositories are private, this public repository serves as a distribution point for our packages, allowing users to install them directly via `npx` or `npm`.

## Available Packages

### Platform CLI
The main AnyPlatform CLI tool for creating and managing projects.

**Latest version**: Check the [releases page](https://github.com/anyplatform/releases/releases)

**Installation**:
```bash
# Use with npx (recommended) - always gets the latest version
npx https://github.com/anyplatform/releases/releases/latest/download/anyplatform-platform.tgz create my-app

# Or install globally
npm install -g https://github.com/anyplatform/releases/releases/latest/download/anyplatform-platform.tgz
```

**Specific version**:
```bash
# Use a specific version if needed
npx https://github.com/anyplatform/releases/releases/download/platform-v0.0.6/anyplatform-platform-0.0.6.tgz create my-app
```

## Release Structure

Releases are tagged with the pattern: `{package}-v{version}`
- `platform-v0.0.6` - Platform CLI version 0.0.6
- `components-v1.0.0` - Components package version 1.0.0 (future)

## Source Code

The source code for these packages is maintained in private repositories. This repository only contains the built distributions.

## Support

For issues, questions, or contributions, please contact the AnyPlatform team.

## License

See the individual package licenses in their respective tarballs.

---

*This repository is automatically updated by our CI/CD pipeline.*
