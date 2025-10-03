---
title: 'Functions File Reference'
description: 'Detailed guide to creating the functions.json file for your TetiAI app'
---

# Functions File Reference

The `functions.json` file defines the specific capabilities of your TetiAI app by specifying the functions that TetiAI can call. This document provides a comprehensive reference for creating effective function definitions.

## Basic Structure

The `functions.json` file is an array of function objects, each defining a specific capability:

```json
[
  {
    "name": "APP_NAME__FUNCTION_NAME",
    "description": "Description of what this function does",
    "tags": ["tag1", "tag2"],
    "visibility": "public",
    "active": true,
    "protocol": "rest",
    "protocol_data": {
      // Protocol-specific configuration
    },
    "parameters": {
      // Parameter definitions
    }
  },
  // Additional function definitions...
]
```

## Function Object Properties

Each function in the array must include these properties:

### name (Required)

The unique identifier for the function:

```json
"name": "GMAIL__SEND_EMAIL"
```

Guidelines:
- Follow the format: `APP_NAME__FUNCTION_NAME` (with double underscore)
- Use UPPERCASE with underscores
- Make names descriptive and action-oriented
- Ensure each name is unique within your app

### description (Required)

A concise explanation of what the function does:

```json
"description": "Sends an email on behalf of the user"
```

Guidelines:
- Begin with a verb (Sends, Creates, Gets, Lists, etc.)
- Focus on the outcome or purpose
- Keep under 100 characters
- Be specific about what the function accomplishes

### tags

Categories or labels that help TetiAI understand when to use this function:

```json
"tags": ["email", "communication"]
```

Guidelines:
- Use lowercase words
- Include both general categories and specific capabilities
- Limit to 5 tags per function
- Be consistent across related functions

### visibility

Specifies who can see and use this function:

```json
"visibility": "public"
```

Options:
- `"public"`: Available to all users
- `"private"`: Available only to the developer and specified users
- `"internal"`: Used internally by other functions (not directly callable)

### active

Indicates whether the function is currently available:

```json
"active": true
```

Set to `false` to temporarily disable a function without removing it.

### protocol (Required)

Specifies how TetiAI should interact with this function:

```json
"protocol": "rest"
```

Options:
- `"rest"`: Standard REST API calls
- `"connector"`: Custom connector for complex operations
- `"websocket"`: WebSocket-based communication
- `"graphql"`: GraphQL API calls

### protocol_data

Configuration specific to the chosen protocol:

#### For REST protocol:

```json
"protocol_data": {
  "method": "POST",
  "path": "/users/me/messages/send",
  "server_url": "https://gmail.googleapis.com/gmail/v1"
}
```

Required fields for REST:
- `method`: HTTP method (GET, POST, PUT, DELETE, etc.)
- `path`: API endpoint path, can include path parameters
- `server_url`: Base URL for the API

#### For connector protocol:

```json
"protocol_data": {}
```

Connectors use custom logic implemented by TetiAI, so no additional configuration is needed here.

## Parameters Object

The parameters object defines the inputs required by the function:

```json
"parameters": {
  "type": "object",
  "properties": {
    // Property definitions
  },
  "required": ["property1", "property2"],
  "visible": ["property1", "property2", "property3"],
  "additionalProperties": false
}
```

### properties

Defines each parameter the function accepts:

```json
"properties": {
  "recipient": {
    "type": "string",
    "description": "The email address of the recipient",
    "format": "email"
  },
  "subject": {
    "type": "string",
    "description": "The subject of the email"
  },
  "body": {
    "type": "string",
    "description": "The body content of the email"
  }
}
```

Each property can include:
- `type`: Data type (string, number, boolean, array, object)
- `description`: Explanation of the parameter
- `format`: Specific format for the type (email, date-time, uri, etc.)
- `default`: Default value if not provided
- `enum`: List of allowed values
- Additional type-specific validations

### required

Array of required property names:

```json
"required": ["recipient", "body"]
```

Properties listed here must be provided for the function to work.

### visible

Array of property names that should be visible to users:

```json
"visible": ["recipient", "subject", "body"]
```

Properties not listed here may still be used but won't be directly exposed.

### additionalProperties

Controls whether properties not defined can be passed:

```json
"additionalProperties": false
```

Usually set to `false` to enforce strict parameter validation.

## Parameter Types and Formats

### String Parameters

```json
"recipient": {
  "type": "string",
  "description": "The email address of the recipient",
  "format": "email",
  "minLength": 5,
  "maxLength": 100
}
```

Common string formats:
- `email`: Email address
- `date-time`: ISO 8601 date and time
- `date`: ISO 8601 date
- `uri`: URI/URL
- `uuid`: UUID

### Number Parameters

```json
"count": {
  "type": "integer",
  "description": "Number of results to return",
  "minimum": 1,
  "maximum": 100,
  "default": 10
}
```

Numeric types:
- `integer`: Whole numbers
- `number`: Any numeric value (including decimals)

### Boolean Parameters

```json
"includeAttachments": {
  "type": "boolean",
  "description": "Whether to include attachments",
  "default": false
}
```

### Array Parameters

```json
"labels": {
  "type": "array",
  "description": "Labels to apply to the email",
  "items": {
    "type": "string"
  },
  "minItems": 0,
  "maxItems": 10
}
```

The `items` property defines the type of elements in the array.

### Object Parameters

```json
"query": {
  "type": "object",
  "description": "Query parameters",
  "properties": {
    "maxResults": {
      "type": "integer",
      "description": "Maximum number of results to return",
      "default": 10
    },
    "q": {
      "type": "string",
      "description": "Search query"
    }
  }
}
```

### Nested Structures

For REST APIs, it's common to organize parameters into `path`, `query`, and `body` objects:

```json
"parameters": {
  "type": "object",
  "properties": {
    "path": {
      "type": "object",
      "description": "Path parameters",
      "properties": {
        "id": {
          "type": "string",
          "description": "The ID of the resource"
        }
      },
      "required": ["id"]
    },
    "query": {
      "type": "object",
      "description": "Query parameters",
      "properties": {
        "fields": {
          "type": "string",
          "description": "Fields to include in the response"
        }
      }
    },
    "body": {
      "type": "object",
      "description": "Request body",
      "properties": {
        "name": {
          "type": "string",
          "description": "Name of the resource"
        }
      }
    }
  },
  "required": ["path"],
  "visible": ["path", "query", "body"]
}
```

## Complete Function Example

Here's a complete example of a function definition for sending an email:

```json
{
  "name": "GMAIL__SEND_EMAIL",
  "description": "Sends an email on behalf of the user",
  "tags": ["email"],
  "visibility": "public",
  "active": true,
  "protocol": "connector",
  "protocol_data": {},
  "parameters": {
    "type": "object",
    "properties": {
      "sender": {
        "type": "string",
        "description": "The user's email address where the email will be sent from. The special value me can be used to indicate the authenticated user.",
        "default": "me"
      },
      "recipient": {
        "type": "string",
        "description": "The email address of the recipient.",
        "format": "email"
      },
      "body": {
        "type": "string",
        "description": "The body content of the email, for now only plain text is supported."
      },
      "subject": {
        "type": "string",
        "description": "The subject of the email."
      },
      "cc": {
        "type": ["array"],
        "items": {
          "type": "string",
          "format": "email"
        },
        "description": "The email addresses of the cc recipients."
      },
      "bcc": {
        "type": ["array"],
        "items": {
          "type": "string",
          "format": "email"
        },
        "description": "The email addresses of the bcc recipients."
      }
    },
    "required": ["sender", "recipient", "body"],
    "visible": ["sender", "recipient", "subject", "body", "cc", "bcc"],
    "additionalProperties": false
  }
}
```

## REST API Example

Here's a function definition for a REST API endpoint:

```json
{
  "name": "GMAIL__MESSAGES_LIST",
  "description": "Lists the messages in the user's mailbox",
  "tags": ["email", "messages"],
  "visibility": "public",
  "active": true,
  "protocol": "rest",
  "protocol_data": {
    "method": "GET",
    "path": "/users/me/messages",
    "server_url": "https://gmail.googleapis.com/gmail/v1"
  },
  "parameters": {
    "type": "object",
    "properties": {
      "query": {
        "type": "object",
        "description": "Query parameters",
        "properties": {
          "maxResults": {
            "type": "integer",
            "description": "Maximum number of messages to return. Default is 100.",
            "maximum": 500,
            "default": 100
          },
          "pageToken": {
            "type": "string",
            "description": "Page token to retrieve a specific page of results",
            "default": null
          },
          "q": {
            "type": "string",
            "description": "Only return messages matching the specified query."
          },
          "labelIds": {
            "type": "array",
            "description": "Only return messages with labels that match all of the specified label IDs.",
            "items": {
              "type": "string"
            }
          },
          "includeSpamTrash": {
            "type": "boolean",
            "description": "Include messages from SPAM and TRASH in the results.",
            "default": false
          }
        },
        "required": [],
        "visible": ["maxResults", "pageToken", "q", "labelIds", "includeSpamTrash"],
        "additionalProperties": false
      }
    },
    "required": [],
    "visible": ["query"],
    "additionalProperties": false
  }
}
```

## Function Design Best Practices

When designing your app's functions, follow these best practices:

### 1. Focus on Atomic Operations

Design each function to do one specific thing well:
- **Good**: `CALENDAR__CREATE_EVENT`, `CALENDAR__GET_EVENT`
- **Avoid**: `CALENDAR__MANAGE_EVENTS` (too broad)

### 2. Use Consistent Naming

Follow a consistent pattern for function names:
- **Verbs**: Get, List, Create, Update, Delete, Search
- **Resources**: Event, Message, Contact, File
- **Format**: APP_NAME__VERB_RESOURCE

### 3. Provide Clear Parameter Descriptions

Each parameter should have a clear, concise description:
- Explain what the parameter does
- Include format requirements
- Mention any constraints
- Provide examples if helpful

### 4. Set Sensible Defaults

Where possible, provide default values to make functions easier to use:
- Default counts and limits
- Common configurations
- Sensible starting points

### 5. Validate Inputs Properly

Use the JSON Schema features to validate inputs:
- Set appropriate `minLength`/`maxLength` for strings
- Use `minimum`/`maximum` for numbers
- Apply `format` for special types like email
- Mark required parameters
- Set `additionalProperties` to false

## Next Steps

After defining your app's functions, learn about:

- [Authentication methods](/app-development/authentication) for your app
- [Testing your app](/app-development/testing) before submission
- [Submitting your app](/app-development/submission) to the TetiAI marketplace