# Izzy Client Management System

A comprehensive web application for managing client profile information for US-based customers with full CRUD capabilities and data persistence. This application will persist all changes that are made to the customer records. All new records that are added will be persisted. All edits and deletes will also be persisted.

**Experience Qualities**:
1. **Professional** - Clean, business-focused interface that inspires confidence in data management
2. **Efficient** - Streamlined workflows that minimize clicks and form completion time
3. **Reliable** - Clear feedback and validation that ensures data integrity

**Complexity Level**: Light Application (multiple features with basic state)
This application manages customer records with create, read, update, delete operations across multiple views, requiring structured state management and form handling.

## Essential Features

### Customer Creation
- **Functionality**: Capture new customer profile data through validated form
- **Purpose**: Enable rapid onboarding of new customers with data quality assurance
- **Trigger**: "Add New Customer" button from main dashboard
- **Progression**: Click Add → Fill form with validation → Submit → Success confirmation → Return to list
- **Success criteria**: Customer appears in list with generated ID, all required fields validated

### Customer List View
- **Functionality**: Display paginated table of customers with key information
- **Purpose**: Provide quick overview and access point for customer management
- **Trigger**: Default landing page or "View All Customers" navigation
- **Progression**: Load page → Display table → Click customer → View details/edit
- **Success criteria**: All customers displayed with correct data, actions work properly

### Customer Details View
- **Functionality**: Show complete customer profile in read-only format
- **Purpose**: Allow users to review full customer information without edit risk
- **Trigger**: Click customer ID or name from list
- **Progression**: Click customer → Load details → Review data → Edit or return to list
- **Success criteria**: All customer data displayed accurately with navigation options

### Customer Editing
- **Functionality**: Modify existing customer data through pre-populated form
- **Purpose**: Maintain up-to-date customer information
- **Trigger**: "Edit" button from details view or list
- **Progression**: Click edit → Form loads with data → Modify fields → Save → Confirmation → Updated data shown
- **Success criteria**: Changes persist and are reflected across all views

### Customer Deletion
- **Functionality**: Remove customer records with confirmation
- **Purpose**: Clean up database and remove outdated records
- **Trigger**: "Delete" button with confirmation dialog
- **Progression**: Click delete → Confirmation dialog → Confirm → Record removed → List updated
- **Success criteria**: Customer no longer appears in system, confirmation shown

## Edge Case Handling
- **Duplicate Email Prevention**: Real-time validation prevents duplicate email addresses
- **Invalid Phone Format**: E.123 format validation with helpful format examples
- **Invalid Zipcode**: 5-digit US zipcode validation with error messaging
- **Empty State Handling**: Friendly empty state when no customers exist
- **Form Abandonment**: Unsaved changes warning when navigating away
- **Network Errors**: Graceful handling of failed operations with retry options
- **Data Persistence**: This application will persist all changes that are made to the customer records. All new records that are added will be persisted. All edits and deletes will also be persisted

## Design Direction
The design should feel professional and trustworthy, similar to enterprise CRM systems but with modern, clean aesthetics. Minimal interface approach serves the data-focused nature while maintaining visual hierarchy for efficient scanning.

## Color Selection
Complementary (blue/orange) scheme to create trust through blue primary with orange accents for actions.

- **Primary Color**: Deep Blue (oklch(0.45 0.15 250)) - Communicates trust, professionalism, and reliability
- **Secondary Colors**: Light Gray (oklch(0.95 0.01 250)) for backgrounds, Medium Gray (oklch(0.65 0.02 250)) for borders
- **Accent Color**: Warm Orange (oklch(0.70 0.15 45)) - Attention-grabbing for CTAs and important actions
- **Foreground/Background Pairings**:
  - Background (Light Gray oklch(0.98 0.01 250)): Dark Text (oklch(0.2 0.02 250)) - Ratio 12.1:1 ✓
  - Card (White oklch(1 0 0)): Dark Text (oklch(0.2 0.02 250)) - Ratio 15.8:1 ✓
  - Primary (Deep Blue oklch(0.45 0.15 250)): White Text (oklch(1 0 0)) - Ratio 8.2:1 ✓
  - Secondary (Light Gray oklch(0.95 0.01 250)): Dark Text (oklch(0.2 0.02 250)) - Ratio 11.1:1 ✓
  - Accent (Warm Orange oklch(0.70 0.15 45)): White Text (oklch(1 0 0)) - Ratio 4.8:1 ✓

## Font Selection
Typography should convey professionalism and excellent readability for data-heavy interfaces, using Inter for its superior legibility in forms and tables.

- **Typographic Hierarchy**:
  - H1 (Page Titles): Inter Bold/32px/tight letter spacing
  - H2 (Section Headers): Inter Semibold/24px/normal spacing
  - H3 (Card Titles): Inter Medium/18px/normal spacing
  - Body (Form Labels/Table Data): Inter Regular/16px/normal spacing
  - Small (Helper Text): Inter Regular/14px/wide spacing

## Animations
Subtle and purposeful animations that enhance workflow efficiency without creating delays, focusing on state transitions and form feedback.

- **Purposeful Meaning**: Smooth transitions communicate system responsiveness and guide attention to important changes
- **Hierarchy of Movement**: Form validation gets immediate feedback, navigation transitions are smooth but quick, loading states are clear

## Component Selection
- **Components**: Cards for customer details, Tables for listings, Forms with proper validation, Dialogs for confirmations, Buttons with clear action hierarchy, Inputs with validation states
- **Customizations**: Customer table with sortable columns, Multi-step form with progress indication, Confirmation dialogs with action preview
- **States**: Buttons show loading/success/error states, Form inputs show validation feedback, Table rows highlight on hover
- **Icon Selection**: Plus for add actions, Pencil for edit, Eye for view, Trash for delete, Phone/Email/Address icons for contact info
- **Spacing**: Consistent 16px base spacing with 8px micro-spacing and 32px section separation
- **Mobile**: Stack form fields vertically, convert table to cards, collapsible sections for details, thumb-friendly button sizes
