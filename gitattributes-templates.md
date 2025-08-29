# .gitattributes Templates for Repository Creation

## Summary
Add `.gitattributes` templates to GitHub's repository initialization process, similar to existing `.gitignore` and LICENSE templates.

## Current State
Currently, GitHub provides templates for:
- `.gitignore` (language/framework specific)
- `LICENSE` (various license types)
- `CODE_OF_CONDUCT` (community guidelines)

Missing: `.gitattributes` templates

## Proposed Feature

### .gitattributes Template System
Add `.gitattributes` templates with options for:
- **Language-specific templates**: Python, JavaScript, Java, C#, etc.
- **Framework-specific templates**: React, Django, Spring Boot, etc.
- **Platform-specific templates**: Windows, macOS, Linux
- **Tool-specific templates**: Git LFS, Docker, IDE configurations
- **Documentation templates**: Markdown, Sphinx, GitBook

### Example Templates

**Python:**
```
*.py text eol=lf
*.ipynb filter=lfs diff=lfs merge=lfs
```

**Web Development:**
```
*.js text eol=lf
*.css text eol=lf
*.html text eol=lf
```

**Git LFS:**
```
*.png filter=lfs diff=lfs merge=lfs -text
*.jpg filter=lfs diff=lfs merge=lfs -text
```

**Markdown:**
```
# Markdown files
*.md text eol=lf
*.markdown text eol=lf
*.mdown text eol=lf
*.mkd text eol=lf
*.mkdn text eol=lf
*.mdx text eol=lf
*.md linguist-language=Markdown linguist-detectable=true

# Documentation assets
*.svg text
docs/**/*.png filter=lfs diff=lfs merge=lfs -text
docs/**/*.jpg filter=lfs diff=lfs merge=lfs -text
assets/**/*.gif filter=lfs diff=lfs merge=lfs -text
```

## Use Cases

- New developers don't know which attributes to set for their language/framework
- Consistent line ending handling across teams
- Proper Git LFS configuration for binary files
- Standardized diff and merge behavior
- **Documentation projects**: proper handling of Markdown files and media content

## Documentation Project Benefits

**Applicable to:**
- Wiki projects
- GitHub Pages sites
- Books and tutorials
- API documentation
- Static site generator blogs (Jekyll, Hugo, Gatsby)

**Benefits:**
- Correct diff display for Markdown files
- Proper line ending handling across platforms
- Automatic Git LFS setup for documentation images
- Improved handling of media files in docs/ and assets/ folders

## Implementation Suggestion

**Template Management:**
- Store templates in a public repository (like github/gitignore)
- Community contributions via pull requests
- Versioning and maintenance by GitHub team

## Benefits
- **Reduces setup time** for new repositories
- **Improves repository quality** with proper Git configuration
- **Educational value** for developers learning Git attributes
- **Consistency** across projects and teams
- **Support for documentation projects** on par with code projects
