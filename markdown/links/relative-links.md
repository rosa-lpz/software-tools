# Relative Links

## What Are Relative Links?

Relative links are hyperlinks that point to another file or location within the same repository. Unlike absolute links, which use the full URL, relative links are based on the current location of the file. This makes them more flexible and portable, especially when working with different branches or cloning repositories.

### Example:

```cmd
- Absolute Link -
C:/main_folder/project_1/docs/readME.md

- Relative Link -
docs/readME.md
```

## Why Use Relative Links?

    Portability: Since relative links don't rely on the full URL, they remain valid regardless of where the repository is hosted.
    Branch Independence: Relative links work seamlessly across different branches, making it easier to maintain consistent documentation.
    Ease of Maintenance: Updating file structures or moving files doesn't break relative links as long as the relative paths remain the same.

# References

https://www.geeksforgeeks.org/git/github-relative-link-in-markdown-file/