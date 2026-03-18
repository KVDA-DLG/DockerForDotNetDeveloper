# How to Work with CODEOWNERS

## What is CODEOWNERS?

The CODEOWNERS file is a GitHub feature that allows you to define individuals or teams that are responsible for code in a repository. When someone opens a pull request that modifies code that has an owner, that owner will be automatically requested for review.

## Location

The CODEOWNERS file is located at: `.github/CODEOWNERS`

## How It Works

1. **Automatic Review Requests**: When a pull request is opened that changes files matching patterns in CODEOWNERS, the specified owners are automatically requested as reviewers.

2. **Pattern Matching**: The CODEOWNERS file uses gitignore-style patterns to match files:
   - `*` matches everything in the repository
   - `*.md` matches all Markdown files
   - `Dockerfile*` matches all files starting with "Dockerfile"
   - `/path/to/file.txt` matches a specific file

3. **Order Matters**: The last matching pattern takes precedence. Patterns are evaluated from top to bottom.

## Current Ownership Structure

- **All files** (`*`): @KVDA-DLG
- **Documentation files** (`*.md`): @KVDA-DLG
- **Docker configurations** (`Dockerfile*`, `docker-compose*.yml`, `.dockerignore`): @KVDA-DLG

## How to Update CODEOWNERS

1. Edit the `.github/CODEOWNERS` file
2. Add or modify patterns and owners:
   ```
   # Pattern followed by one or more owners
   /path/to/directory/ @username
   *.js @frontend-team
   ```
3. Commit and push your changes
4. The new ownership rules will take effect immediately for new pull requests

## Tips

- Use GitHub usernames or team names (e.g., `@username` or `@org/team-name`)
- Comment your patterns to make them easier to understand
- Test your patterns by opening a test pull request
- More specific patterns should come after general patterns

## References

- [GitHub CODEOWNERS Documentation](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners)
- [CODEOWNERS Syntax](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners#codeowners-syntax)
