# Laptop Request Catalog Item - ServiceNow

## Overview
This project provides a ServiceNow Service Catalog Item that enables employees to request laptops in a streamlined, user-friendly, and dynamic way. It replaces outdated manual processes with a modern, automated solution that ensures accurate data collection and improved user experience.

## Features
- Dynamic form behavior using Catalog UI Policies
- Reset form functionality using a client-side UI Action
- Clear, guided form instructions for users
- Exportable update set for deployment to other ServiceNow instances
- Fully tested in a separate instance to ensure smooth deployment

## Variables Included
- Laptop Model
- Justification
- Additional Accessories (checkbox/dropdown)
- Accessories Details (shown conditionally)

## Dynamic Form Behavior
Implemented using Catalog UI Policies:
- Show/Hide `Accessories Details` field based on selection of `Additional Accessories`
- Set `Accessories Details` as mandatory if `Additional Accessories` is selected

## Reset Form Functionality
A client-side UI Action is included to allow users to reset the form.

**UI Action Details:**
- **Table**: `sc_cart`
- **Action Name**: Reset Form
- **Order**: 100
- **Client**: Checked
- **Script**:
```javascript
function resetForm() {
  g_form.clearForm(); // Clears all fields in the form
  alert("The form has been reset.");
}



## Conclusion

The Laptop Request Catalog Item significantly improves the employee experience by providing a faster, more intuitive way to request laptops through ServiceNow. With dynamic field behavior, a reset functionality, and easy deployment via update sets, this solution reduces manual effort, eliminates common errors, and supports scalable IT service management. It is a practical step toward automating hardware provisioning within your organization.

