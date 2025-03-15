# Ctrlplane Documentation Guidelines

## Project Information
- Documentation platform: Mintlify
- Primary content: MDX files for API documentation and concept guides

## Documentation Structure
- API endpoints follow OpenAPI spec format with `---` frontmatter
- Concept pages use descriptive titles and clear structure
- Use tables for comparing capabilities
- Group related documentation in directories by category

## Styling Guidelines
- Frontmatter should include title and description
- Use h2 (##) for main sections, h3 (###) for subsections
- Tables should include clear headers with alignment (: syntax)
- Components like `<CardGroup>` and `<Card>` for navigation elements
- Code blocks should specify language when applicable
- Images should be placed in `/images/` organized by feature area

## Documentation Commands
- Preview: npx mintlify dev
- Build: npx mintlify build
- Deploy: npx mintlify deploy

## Content Best Practices
- Keep descriptions concise and action-oriented
- Use consistent terminology throughout documentation
- Link related concepts for better navigation
- Example code should be complete and tested
- Maintain OpenAPI reference in sync with API implementation