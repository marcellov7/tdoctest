---
title: 'Authentication Methods'
description: 'Setting up secure authentication for your TetiAI app'
---

# Authentication Methods

Proper authentication is critical for secure access to external services through your TetiAI app. This guide explains the supported authentication methods and how to implement them.

## Supported Authentication Methods

TetiAI supports two primary authentication methods:

<CardGroup cols={2}>
  <Card title="OAuth 2.0" icon="key">
    Industry-standard protocol for authorization
  </Card>
  <Card title="API Keys" icon="lock">
    Simple key-based authentication
  </Card>
</CardGroup>

## Choosing an Authentication Method

When deciding which authentication method to use:

- **Use OAuth 2.0** for apps that:
  - Connect to established services (Google, Microsoft, etc.)
  - Need to access user-specific data
  - Require fine-grained permissions
  - Support delegated access

- **Use API Keys** for apps that:
  - Have simpler authentication requirements
  - Connect to services without OAuth support
  - Use developer-specific credentials
  - Have minimal permission requirements

## OAuth 2.0 Authentication

OAuth 2.0 is the recommended authentication method for most apps. It provides a secure way for users to grant limited access to their data without sharing their credentials.

### OAuth 2.0 Configuration

To implement OAuth 2.0, add a `security_schemes` object to your `config.json` file:

```json
"security_schemes": {
  "oauth2": {
    "location": "header",
    "name": "Authorization",
    "prefix": "Bearer",
    "client_id": "your-oauth-client-id",
    "client_secret": "your-oauth-client-secret",
    "scope": "scope1 scope2 scope3",
    "authorize_url": "https://service.com/oauth2/authorize",
    "access_token_url": "https://service.com/oauth2/token",
    "refresh_token_url": "https://service.com/oauth2/token",
    "access_type": "offline",
    "prompt": "consent",
    "response_type": "code"
  }
}
```

### OAuth 2.0 Properties

| Property | Description | Required |
|----------|-------------|----------|
| `location` | Where to place the token (usually "header") | Yes |
| `name` | Name of the header/parameter (usually "Authorization") | Yes |
| `prefix` | Token prefix (usually "Bearer") | Yes |
| `client_id` | OAuth client ID from service provider | Yes |
| `client_secret` | OAuth client secret from service provider | Yes |
| `scope` | Space-separated list of requested permissions | Yes |
| `authorize_url` | URL for the authorization endpoint | Yes |
| `access_token_url` | URL for the token endpoint | Yes |
| `refresh_token_url` | URL for the token refresh endpoint | Yes |
| `access_type` | Indicates the desired access type (online/offline) | No |
| `prompt` | Controls the authorization server's prompts to the user | No |
| `response_type` | Response type (usually "code") | No |

### Obtaining OAuth Credentials

To get the necessary OAuth credentials:

1. Register your app with the service provider (Google, Microsoft, etc.)
2. Specify redirect URL as: `https://app.teti.ai/api/oauth/callback`
3. Request the appropriate scopes for your app's functionality
4. Note the client ID and client secret provided

### OAuth Flow in TetiAI

When a user connects your app:

1. TetiAI redirects to the `authorize_url` with your client ID and requested scopes
2. User authorizes access on the service provider's page
3. Service redirects back to TetiAI with an authorization code
4. TetiAI exchanges the code for access and refresh tokens
5. TetiAI securely stores the tokens and uses them for API requests

## API Key Authentication

API key authentication is simpler but places more responsibility on the user to provide credentials.

### API Key Configuration

To implement API key authentication, add a `security_schemes` object to your `config.json` file:

```json
"security_schemes": {
  "api_key": {
    "location": "header",
    "name": "X-API-Key",
    "prefix": "",
    "fields": [
      {
        "name": "api_key",
        "display_name": "API Key",
        "type": "password",
        "required": true,
        "description": "Your API key from the service dashboard"
      }
    ]
  }
}
```

### API Key Properties

| Property | Description | Required |
|----------|-------------|----------|
| `location` | Where to place the key ("header", "query", "cookie") | Yes |
| `name` | Name of the header/parameter/cookie | Yes |
| `prefix` | Prefix for the key value (often empty) | Yes |
| `fields` | Array of fields to collect from the user | Yes |

### Fields Array

The `fields` array defines what information to collect from the user:

```json
"fields": [
  {
    "name": "api_key",
    "display_name": "API Key",
    "type": "password",
    "required": true,
    "description": "Your API key from the service dashboard"
  },
  {
    "name": "account_id",
    "display_name": "Account ID",
    "type": "text",
    "required": true,
    "description": "Your account ID from the service dashboard"
  }
]
```

Each field can have these properties:

| Property | Description | Required |
|----------|-------------|----------|
| `name` | Internal identifier for the field | Yes |
| `display_name` | User-facing label | Yes |
| `type` | Input type ("text", "password", "number", etc.) | Yes |
| `required` | Whether the field is required | Yes |
| `description` | Explanation of what to enter | Yes |
| `placeholder` | Example text for the input field | No |
| `default` | Default value | No |

### API Key Flow in TetiAI

When a user connects your app:

1. TetiAI shows a form with the fields you defined
2. User enters their API key and any other required fields
3. TetiAI securely stores the credentials and uses them for API requests

## Combined Authentication

Some APIs require multiple authentication methods. TetiAI supports combining methods:

```json
"security_schemes": {
  "api_key": {
    "location": "header",
    "name": "X-API-Key",
    "prefix": "",
    "fields": [
      {
        "name": "api_key",
        "display_name": "API Key",
        "type": "password",
        "required": true,
        "description": "Your API key"
      }
    ]
  },
  "project_id": {
    "location": "query",
    "name": "project",
    "prefix": "",
    "fields": [
      {
        "name": "project_id",
        "display_name": "Project ID",
        "type": "text",
        "required": true,
        "description": "Your project ID"
      }
    ]
  }
}
```

## Authentication Security Best Practices

Follow these security best practices:

### For OAuth 2.0

1. **Request Minimal Scopes**: Only request permissions your app actually needs
2. **Use PKCE**: For public clients, implement PKCE for additional security
3. **Handle Refresh Tokens**: Implement proper token refresh logic
4. **Validate Tokens**: Verify token validity before using
5. **Error Handling**: Implement graceful handling of authentication errors

### For API Keys

1. **Use Password Field Type**: Always use the `"type": "password"` for API keys
2. **Clear Instructions**: Provide clear guidance on where to find the key
3. **Separate Keys**: Use separate API keys for development and production
4. **Encryption**: Ensure keys are encrypted in transit and at rest
5. **Revocation Plan**: Document how users can revoke keys if compromised

## Authentication Implementation Examples

### Google OAuth Example

```json
"security_schemes": {
  "oauth2": {
    "location": "header",
    "name": "Authorization",
    "prefix": "Bearer",
    "client_id": "497832325649-p5s36a4sar97bfolosfdulj0gtjian8u.apps.googleusercontent.com",
    "client_secret": "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",
    "scope": "https://www.googleapis.com/auth/gmail.send https://www.googleapis.com/auth/gmail.readonly",
    "authorize_url": "https://accounts.google.com/o/oauth2/auth",
    "access_token_url": "https://oauth2.googleapis.com/token",
    "refresh_token_url": "https://oauth2.googleapis.com/token",
    "access_type": "offline",
    "prompt": "consent",
    "response_type": "code"
  }
}
```

### Weather API Key Example

```json
"security_schemes": {
  "api_key": {
    "location": "header",
    "name": "X-API-Key",
    "prefix": "",
    "fields": [
      {
        "name": "api_key",
        "display_name": "API Key",
        "type": "password",
        "required": true,
        "description": "Enter your Weather API key from your account dashboard"
      }
    ]
  }
}
```

## Troubleshooting Authentication

Common authentication issues and solutions:

| Issue | Solution |
|-------|----------|
| "Invalid client" error | Check client ID and secret for typos |
| "Invalid redirect URI" | Ensure redirect URI matches registered value |
| "Insufficient scope" | Request additional permissions |
| "Invalid token" | Implement proper token refresh |
| "Rate limit exceeded" | Implement rate limiting and backoff |

## Next Steps

Now that you've set up authentication, learn about:

- [Testing your app](/app-development/testing) before submission
- [Submitting your app](/app-development/submission) to the TetiAI marketplace
- [Example apps](/app-development/examples/gmail) to see complete implementations