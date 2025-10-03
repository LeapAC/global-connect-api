# Global Connect API Documentation

This repository contains the documentation for the **Global Connect API**, a session-based customer onboarding platform for energy grid services programs.

## About Global Connect

Global Connect is a RESTful API that enables partners to create dynamic, multi-step onboarding flows for customers enrolling in energy grid services programs. The API automatically generates appropriate onboarding steps based on transmission region, customer classification, and program requirements.

### Key Features

- **Dynamic Flow Generation**: Onboarding flows automatically adapt based on transmission region (PJM, ERCOT, CAISO, etc.), customer type (residential/commercial), and program requirements
- **Session-Based State Management**: Each customer onboarding creates a unique session that tracks progress and accumulates data throughout the enrollment process
- **Step-by-Step Validation**: Validates customer input at each step with detailed error messages before advancing
- **Agreement Management**: Handles customer agreements including e-signature workflows via integrated providers
- **Utility Authorization**: OAuth flows for connecting utility accounts with support for multiple transmission regions
- **Template Support**: Pre-configure default field values for specific partners, regions, and programs

### How It Works

1. **Create a session** with transmission region, customer classification, and optional program identifier
2. **Collect customer data** by updating the session context with field values
3. **Validate each step** to ensure all requirements are met before advancing
4. **Advance through steps** - the API automatically skips steps with pre-populated fields
5. **Track completion** - query connection status after enrollment is finished

## About This Documentation Project

This documentation is built with [Mintlify](https://mintlify.com), a modern documentation framework that provides:

- Interactive API reference generated from OpenAPI specifications
- Rich markdown support with custom components
- Built-in search functionality
- Responsive design for desktop and mobile
- Code examples and syntax highlighting

### Documentation Structure

```
.
├── index.mdx                    # Home page and overview
├── quickstart.mdx              # Getting started guide
├── development.mdx             # Development setup
├── api-reference/
│   ├── introduction.mdx        # API overview and authentication
│   ├── openapi.json           # OpenAPI specification
│   └── endpoint/              # Individual endpoint documentation
├── ai-tools/                   # AI-assisted development guides
└── docs.json                   # Mintlify configuration
```

### Local Development

Install the [Mintlify CLI](https://www.npmjs.com/package/mintlify) to preview changes locally:

```bash
npm i -g mintlify
```

Run the development server:

```bash
mintlify dev
```

The documentation will be available at `http://localhost:3000`.

### Making Changes

1. Edit `.mdx` files for content pages
2. Update `api-reference/openapi.json` for API reference changes
3. Modify `docs.json` for navigation and configuration
4. Preview changes locally before committing
5. Changes pushed to the main branch will automatically deploy

### OpenAPI Specification

The API reference is automatically generated from the OpenAPI specification located at `api-reference/openapi.json`. To update the API documentation:

1. Edit the OpenAPI JSON file directly, or
2. Generate it from your API server's OpenAPI endpoint
3. Validate the specification using tools like [Swagger Editor](https://editor.swagger.io/)

### Resources

- [Global Connect API Documentation](https://docs.leap.energy)
- [Mintlify Documentation](https://mintlify.com/docs)
- [OpenAPI Specification](https://swagger.io/specification/)

## Support

For API integration support or questions about Global Connect, contact your Leap Energy integration team.

For documentation issues or suggestions, please open an issue in this repository.
