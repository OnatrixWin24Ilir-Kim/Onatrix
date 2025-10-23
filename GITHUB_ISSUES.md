# GitHub Issues for Onatrix Project

## Issue 1: Implement Responsive Design for All Pages

**Priority:** High  
**Labels:** enhancement, responsive, VG-requirement

### Description

Make the website responsive across all pages following the Figma design specifications (VG requirement).

### Tasks

- [ ] Make homepage responsive (mobile, tablet, desktop)
- [ ] Make about page responsive
- [ ] Make services page responsive
- [ ] Make contact page responsive
- [ ] Make project details pages responsive
- [ ] Test navigation on mobile devices
- [ ] Implement responsive images with appropriate sizing

### Acceptance Criteria

- [ ] All pages display correctly on mobile (320px - 767px)
- [ ] All pages display correctly on tablet (768px - 1024px)
- [ ] All pages display correctly on desktop (1025px+)
- [ ] Navigation collapses to hamburger menu on mobile
- [ ] Images scale appropriately without distortion
- [ ] Text is readable at all breakpoints
- [ ] No horizontal scrolling on any device

### Testing

1. Test on Chrome DevTools with different device presets
2. Test on actual mobile device (iOS/Android)
3. Test on tablet device
4. Verify all interactive elements work on touch devices
5. Check that forms are usable on mobile devices

### Related to

VG Criteria - Responsive design requirement

---

## Issue 2: Implement Functional Contact Forms with Validation and Email Confirmation

**Priority:** High  
**Labels:** feature, forms, VG-requirement

### Description

Create fully functional contact forms that validate input, save submissions to Umbraco backoffice, and send email confirmations (VG requirement).

### Tasks

- [ ] Set up Umbraco Forms or custom form handling
- [ ] Implement client-side validation (required fields, email format, phone format)
- [ ] Implement server-side validation
- [ ] Configure form submission storage in backoffice
- [ ] Set up SMTP configuration for email sending
- [ ] Create email template for confirmation emails
- [ ] Test form submission workflow
- [ ] Add success/error messages to user

### Acceptance Criteria

- [ ] All required fields are validated before submission
- [ ] Email addresses are validated with correct format
- [ ] Phone numbers follow correct format
- [ ] Form submissions are saved in Umbraco backoffice
- [ ] Confirmation email is sent to the submitted email address
- [ ] User receives success message after successful submission
- [ ] User receives clear error messages for invalid inputs
- [ ] Form cannot be submitted with invalid data

### Testing

1. Submit form with all valid data - should save and send email
2. Submit form with missing required fields - should show validation errors
3. Submit form with invalid email - should show email format error
4. Check backoffice for saved submission
5. Check inbox for confirmation email
6. Test with special characters in text fields
7. Test maximum length validation

### Related to

VG Criteria - Functional forms requirement

---

## Issue 3: Set Up Site Settings for Global Content Management

**Priority:** High  
**Labels:** feature, configuration, VG-requirement

### Description

Create a Site Settings document type to manage global values like logo, contact information, and social media links from the Umbraco backoffice (VG requirement).

### Tasks

- [ ] Create Site Settings document type
- [ ] Add fields for logo (Media Picker)
- [ ] Add fields for contact information (email, phone, address)
- [ ] Add fields for social media links (Facebook, Twitter, LinkedIn)
- [ ] Add fields for footer content
- [ ] Add fields for company information
- [ ] Create Site Settings content node
- [ ] Update all views to pull from Site Settings instead of hardcoded values
- [ ] Test that changes in backoffice reflect on frontend

### Acceptance Criteria

- [ ] Site Settings document type exists with all necessary fields
- [ ] Logo can be changed from backoffice and updates on all pages
- [ ] Contact information can be updated from backoffice
- [ ] Social media links can be managed from backoffice
- [ ] Footer content is editable from backoffice
- [ ] No hardcoded global content remains in views
- [ ] Changes in Site Settings immediately reflect on frontend
- [ ] Site Settings is accessible from Umbraco root

### Testing

1. Change logo in Site Settings - verify it updates on all pages
2. Update contact email - verify it updates in header/footer
3. Change social media links - verify links work correctly
4. Update address - verify it displays correctly
5. Test with missing optional fields - site should not break
6. Verify Site Settings is only creatable once (use element type if needed)

### Related to

VG Criteria - Site Settings requirement

---

## Issue 4: Implement Compositions for Reusable Content Fields

**Priority:** Medium  
**Labels:** feature, architecture, VG-requirement

### Description

Create and implement compositions for common fields that can be reused across multiple document types (e.g., SEO fields, page headers).

### Tasks

- [ ] Create SEO Composition with meta title, meta description, meta keywords
- [ ] Create Page Header Composition with page title, subtitle, background image
- [ ] Apply SEO Composition to all page document types
- [ ] Apply Page Header Composition to relevant page types
- [ ] Update views to use composition fields
- [ ] Test that composition fields appear in backoffice
- [ ] Verify SEO meta tags render correctly in HTML

### Acceptance Criteria

- [ ] SEO Composition exists with all necessary fields
- [ ] Page Header Composition exists with configurable fields
- [ ] All page types use SEO Composition
- [ ] Relevant pages use Page Header Composition
- [ ] Fields from compositions are editable in backoffice
- [ ] SEO meta tags render in `<head>` section
- [ ] Page headers display correctly on frontend
- [ ] No duplicate field definitions across document types

### Testing

1. Edit SEO fields on a page - verify meta tags in page source
2. Edit page header fields - verify changes on frontend
3. Create new page - verify composition fields are available
4. Test with missing optional composition fields
5. Verify Google search preview with SEO fields
6. Check HTML validation for proper meta tag structure

### Related to

VG Criteria - Compositions requirement

---

## Issue 5: Set Up Projects/Services as Child Pages with List View

**Priority:** Medium  
**Labels:** feature, content-structure, VG-requirement

### Description

Configure projects and services as child pages under their parent pages and implement List View in backoffice for better content management.

### Tasks

- [ ] Create Service Item document type
- [ ] Create Project Item document type
- [ ] Configure Services page to allow Service Item children
- [ ] Configure Projects page to allow Project Item children
- [ ] Enable List View for Service Items
- [ ] Enable List View for Project Items
- [ ] Add appropriate fields to list view (title, date, status)
- [ ] Test creating/editing child pages through list view
- [ ] Implement dynamic listing on parent pages

### Acceptance Criteria

- [ ] Services page shows child service items in List View
- [ ] Projects page shows child project items in List View
- [ ] List View shows relevant columns (title, publish date, etc.)
- [ ] Child pages can be created directly from List View
- [ ] Child pages can be edited from List View
- [ ] Parent pages dynamically display their children on frontend
- [ ] Child pages have proper URLs (parent/child-slug)
- [ ] Sorting and filtering works in List View

### Testing

1. Create new service item - verify it appears in List View
2. Edit service item from List View - verify changes save
3. Create new project item - verify it appears in List View
4. Test sorting by different columns
5. Test filtering in List View
6. Verify child pages display on frontend parent page
7. Check URL structure for child pages
8. Test with 10+ child items for pagination

### Related to

VG Criteria - Child pages with List View requirement
