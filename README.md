# JSON-Based Dynamic Form Editor

This project is a split-screen interface that allows users to edit a JSON schema in real time and view a dynamically generated form based on the schema. The form supports various field types, validation, and displays a success message upon submission.

## Features
- **Split-Screen Interface**:
  - **Left Side**: JSON editor with syntax highlighting and real-time validation.
  - **Right Side**: Form preview dynamically updated as JSON is edited.
- **Real-Time Validation**: Displays errors for invalid JSON input.
- **Dynamic Form Rendering**: Supports text, email, select, radio, checkbox, and textarea fields.
- **Success Message**: Displays a success message when the form is submitted.

---

## Setup Instructions

### Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/json-form-editor.git
   cd json-form-editor
2.Install dependencies:
   npm install
3.Start the development server:
   npm start

#Example JSON Schema
Below is a sample JSON schema used to generate a form:

{
  "page_label": "Project Requirements Survey",
  "fields": [
    {
      "field_id": "name",
      "field_label": "Full Name",
      "field_mandatory": "yes",
      "field_placeholder": "Enter your full name",
      "field_type": "text",
      "field_value": ""
    },
    {
      "field_id": "email",
      "field_label": "Email Address",
      "field_mandatory": "yes",
      "field_placeholder": "you@example.com",
      "field_type": "email",
      "validation": {
        "pattern": "^[^\\s@]+@[^\\s@]+\\.[^\\s@]+$",
        "message": "Please enter a valid email address"
      }
    },
    {
      "field_id": "comments",
      "field_label": "Additional Comments",
      "field_mandatory": "no",
      "field_type": "textarea",
      "field_placeholder": "Any other details you'd like to share..."
    }
  ]
}

You can modify the schema in the JSON Editor pane to add/remove fields or change properties.

# Key Dependencies
React: JavaScript library for building the user interface.
Ace Editor: Used for real-time JSON editing.
TailwindCSS: For styling the UI components.

# Running Locally
Make changes to the JSON schema in formElement.json or directly in the JSON editor.
Preview the form on the right pane as you edit the JSON.
Modify App.js or Element.js to add new features or support additional field types.
