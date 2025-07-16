# Schedule by Aligent - User Guide

## Table of Contents

1. [Getting Started](#getting-started)
2. [Core Features](#core-features)
3. [Creating Scheduled Updates](#creating-scheduled-updates)
4. [Managing Scheduled Updates](#managing-scheduled-updates)
5. [Action Types Explained](#action-types-explained)
6. [Advanced Features](#advanced-features)
7. [Best Practices](#best-practices)
8. [Troubleshooting](#troubleshooting)
9. [FAQ](#frequently-asked-questions)
10. [Glossary](#glossary)

---

## Getting Started

### What is Schedule by Aligent?

Schedule by Aligent is a powerful BigCommerce app that automates pricing changes, product visibility updates, and other e-commerce operations based on your store's timezone. It eliminates the need for manual updates at specific times, allowing you to plan and schedule changes in advance.

### Installation

1. **Install from BigCommerce App Marketplace**
   - Navigate to the BigCommerce App Marketplace
   - Search for "Schedule by Aligent"
   - Click "Install" and follow the prompts
   - The app will automatically configure required permissions

2. **Initial Setup**
   - Upon first launch, the app syncs your store data:
     - Customer Groups
     - Price Lists
     - Products
     - Categories
   - This process may take a few minutes depending on your catalog size

3. **Verify Timezone Settings**
   - Check your store timezone: **Store Settings → Date & Time**
   - All scheduled times use this timezone
   - Ensure it's correct before creating schedules

### Required Permissions

The app requires these BigCommerce permissions:
- **Products Read/Write**: For managing price lists and sale prices
- **Customers Read**: For accessing customer groups
- **Information and Settings Read**: For timezone configuration

---

## Core Features

### 1. Schedule Price List Assignments
Automatically assign different price lists to customer groups at specified times. Perfect for:
- VIP customer promotions
- Wholesale pricing schedules
- Regional pricing strategies

### 2. Product Sale Pricing
Set sale prices on products either directly or within specific price lists:
- Direct sale prices apply to all customers
- Price list sale prices apply only to customers in that group
- Multi-currency support for international stores

### 3. Visibility Management
Control when products or categories appear in your store:
- Launch new products at midnight
- Hide seasonal items automatically
- Create "coming soon" campaigns

### 4. Category Discounts
Apply percentage discounts to entire categories:
- Clearance sales
- Department-wide promotions
- Seasonal markdowns

### 5. Product Name Changes
Temporarily modify product names:
- Add promotional prefixes ("SALE:", "LIMITED:")
- Update naming conventions
- Seasonal product labeling

### 6. Temporary Changes
Create changes that automatically revert:
- Weekend flash sales
- Limited-time offers
- Holiday promotions

---

## Creating Scheduled Updates

### Quick Schedule (Simple Price List Assignment)

1. Click **"Quick Schedule"** from the main dashboard
2. Fill in the required fields:
   - **Description**: A meaningful name for this schedule
   - **Customer Group**: Select target customer group
   - **Price List**: Choose the price list to assign
   - **Scheduled Time**: Set date and time for the change
3. Click **"Create"** to save

### New Schedule (Full Feature Access)

1. Click **"New Schedule"** from the main dashboard
2. **Step 1: Schedule Details**
   - Enter a descriptive name
   - Set the scheduled date and time
   - Optional: Enable temporary change and set end time
3. **Step 2: Add Actions**
   - Click **"Add Action"**
   - Select action type from dropdown
   - Fill in action-specific fields
   - Add multiple actions as needed
4. **Step 3: Review**
   - Verify all details
   - Check scheduled time
   - Review all actions
5. Click **"Create"** to save

### Understanding Temporary Changes

When you enable "Make this change temporary":
- An end date/time field appears
- The duration is displayed (e.g., "2 days, 4 hours")
- A revert action is automatically created
- Both the change and revert appear in your schedule list

---

## Managing Scheduled Updates

### Viewing Scheduled Updates

The main dashboard displays two sections:

**Scheduled Updates** (Pending)
- Shows all future updates
- Displays scheduled time, description, and actions
- Color-coded action badges for easy identification
- Action buttons: Edit, Copy, Delete

**Event History** (Completed)
- Shows executed updates from the last 30+ days
- Includes execution status and timestamp
- Useful for auditing and troubleshooting

### Editing Scheduled Updates

1. Click the **Edit** (pencil) icon for any pending update
2. Navigate through the 3-step editor:
   
   **Step 1: Update Details**
   - Modify description or scheduled time
   - Change temporary status
   - Adjust end time for temporary changes
   
   **Step 2: Edit Actions**
   - Add new actions with "Add Action"
   - Edit existing actions (click action card)
   - Remove actions (click delete icon)
   - Visual indicators show changes:
     - **New** badge for added actions
     - **Changed** badge for modified actions
   
   **Step 3: Review & Save**
   - Review all changes with clear indicators
   - Removed actions shown separately
   - Click "Save Changes" to apply

### Copying Scheduled Updates

Perfect for recurring promotions:

1. Click the **Copy** icon between Edit and Delete
2. In the modal:
   - Update the description (pre-filled with "Copy of...")
   - Set new scheduled time
   - Review actions to be copied
3. Click **"Create Copy"**

**Note**: Temporary settings are not copied - set these manually if needed

### Deleting Scheduled Updates

1. Click the **Delete** (trash) icon
2. Confirm in the modal
3. For temporary changes, both the change and its revert are deleted

---

## Action Types Explained

### Assign Price List
- **Purpose**: Change which price list applies to a customer group
- **Use Cases**: VIP sales, wholesale pricing, regional pricing
- **Fields**:
  - Customer Group (required)
  - Price List (required)

### Set Sale Price
- **Purpose**: Apply a sale price directly to a product
- **Use Cases**: Product-specific promotions, clearance items
- **Fields**:
  - Product selection (required)
  - Sale price amount (required)
- **Note**: Currently supports simple products only

### Set Sale Price in Price List
- **Purpose**: Set sale prices within specific price lists with currency support
- **Use Cases**: Multi-currency stores, region-specific sales
- **Fields**:
  - Price List (required)
  - Product selection (required)
  - Sale price amount (required)
  - Currency (auto-selected based on price list)

### Update Product Visibility
- **Purpose**: Show or hide products in your storefront
- **Use Cases**: Product launches, seasonal items, inventory management
- **Fields**:
  - Product selection (required)
  - Visibility setting (Visible/Not Visible)

### Update Category Visibility
- **Purpose**: Show or hide entire categories
- **Use Cases**: Seasonal collections, coming soon sections
- **Fields**:
  - Category selection (required)
  - Visibility setting (Visible/Not Visible)

### Discount Category
- **Purpose**: Apply percentage discount to all products in a category
- **Use Cases**: Department sales, clearance events
- **Fields**:
  - Category selection (required)
  - Discount percentage (1-99%)
- **Note**: Creates sale prices on individual products

### Change Product Name
- **Purpose**: Temporarily modify product names
- **Use Cases**: Promotional labeling, seasonal updates
- **Fields**:
  - Product selection (required)
  - New product name (required)

---

## Advanced Features

### App Extension - Product Panel Integration

The Schedule app adds a panel directly to your BigCommerce product pages:

1. **Automatic Installation**: Enabled when you install the app
2. **Access**: Edit any product in BigCommerce admin
3. **View**: "Scheduled Updates" panel shows:
   - Direct product updates (price, visibility, name)
   - Category-based updates affecting the product
   - Scheduled times in your store timezone
   - Temporary change indicators

### Bulk Operations Tips

For large-scale updates:

1. **Category Discounts**: Use for store-wide sales instead of individual product updates
2. **Copy Feature**: Create templates for recurring promotions
3. **Multiple Actions**: Add many actions to a single scheduled update
4. **Staggered Timing**: Schedule updates minutes apart to avoid conflicts

### Integration with BigCommerce Features

- **Customer Groups**: Sync automatically, including new groups
- **Price Lists**: Updates when you create or modify lists
- **Products**: New products appear after sync
- **Categories**: Hierarchy maintained for easy selection

---

## Best Practices

### Planning Your Schedules

1. **Test First**: Create test schedules during off-peak hours
2. **Document Changes**: Use descriptive names for easy tracking
3. **Avoid Conflicts**: Check existing schedules before creating new ones
4. **Time Buffers**: Allow time between major updates

### Pricing Strategy Tips

1. **Gradual Rollouts**: Test prices with specific customer groups first
2. **Temporary Sales**: Use temporary changes for all limited-time offers
3. **Regional Pricing**: Leverage multi-currency price lists effectively

### Performance Optimization

1. **Batch Updates**: Combine related changes in single schedules
2. **Off-Peak Scheduling**: Run major updates during low-traffic times
3. **Category vs. Product**: Use category updates for bulk changes

### Security Recommendations

1. **Access Control**: Limit app access to authorized staff
2. **Audit History**: Regularly review event history
3. **Change Validation**: Double-check prices before scheduling

---

## Troubleshooting

### Common Issues and Solutions

**Schedule didn't execute**
- Verify the scheduled time hasn't passed
- Check your store's timezone settings
- Ensure the app has required permissions
- Contact support if the issue persists

**Products not appearing in selection**
- Sync may be needed - products sync periodically
- Check if products are published in BigCommerce
- Verify product type (simple vs. variant)

**Price changes not visible**
- Clear store cache
- Check customer group assignment
- Verify price list is active
- Review BigCommerce price list priority

**Temporary changes not reverting**
- Check both original and revert schedules
- Verify end time was set correctly
- Look for execution errors in history

### Error Messages

**"Failed to update price"**
- Product may have been deleted
- Price list might be inactive
- API rate limit may be reached

**"Invalid scheduled time"**
- Time must be in the future
- Check timezone settings
- Verify date format

### Getting Help

For technical support:
1. Note your store URL and timezone
2. Capture any error messages
3. Check event history for details
4. Contact: support@aligent.com.au

---

## Frequently Asked Questions

### General Questions

**Q: What timezone does the app use?**
A: The app uses your BigCommerce store's timezone (Store Settings → Date & Time)

**Q: Can I schedule updates months in advance?**
A: Yes, there's no limit on how far in advance you can schedule

**Q: Do schedules work if the app is uninstalled?**
A: No, the app must remain installed for schedules to execute

**Q: What happens to schedules during maintenance?**
A: Schedules are queued and execute when service resumes

### Pricing Questions

**Q: Can I set different prices for different currencies?**
A: Yes, use "Set Sale Price in Price List" with currency-specific lists

**Q: Do sale prices override regular prices?**
A: Yes, sale prices take precedence when active

**Q: Can I schedule percentage discounts on individual products?**
A: Use category discounts or calculate sale prices manually

### Feature Questions

**Q: Why can't I set sale prices on products with variants?**
A: Currently limited to simple products; variant support is planned

**Q: Can I schedule inventory changes?**
A: No, only pricing and visibility changes are supported

**Q: Is there an API for external integration?**
A: Not currently; contact support for integration needs

### Technical Questions

**Q: How often does product data sync?**
A: Initial sync on install, then periodic updates

**Q: What's the execution accuracy?**
A: Schedules execute within seconds of scheduled time

**Q: Are there usage limits?**
A: No hard limits, but extremely large updates may take time

---

## Glossary

**Action**: A specific change to be executed (e.g., set sale price, hide product)

**Customer Group**: BigCommerce's way of categorizing customers for special pricing

**Event History**: Log of all executed schedules with timestamps and status

**Price List**: A collection of product prices, potentially in different currencies

**Revert Action**: Automatically created action that undoes a temporary change

**Sale Price**: A promotional price that overrides the regular price

**Scheduled Update**: A collection of actions set to execute at a specific time

**Simple Product**: A product without variants (size, color options)

**Temporary Change**: A scheduled update that automatically reverts after a set time

**Timezone**: The time zone used for all scheduling (from store settings)

**Visibility**: Whether a product or category appears in your storefront

---

## Additional Resources

- **Technical Documentation**: See `/docs/GADGET.md` for platform details
- **Terms of Service**: Review `/docs/TERMS_OF_SERVICE.md`
- **Support**: Email support@aligent.com.au
- **BigCommerce Help**: https://support.bigcommerce.com

---

*Last Updated: January 14, 2025*

© 2025 Aligent. All rights reserved.