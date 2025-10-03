# AutoPrint Mobile-First UI/UX Design Specification

## Table of Contents
1. [Design System Foundation](#design-system-foundation)
2. [User Authentication & Profile](#user-authentication--profile)
3. [File Upload & Configuration](#file-upload--configuration)
4. [Print Job Configuration](#print-job-configuration)
5. [Real-Time Pricing & Cost Calculation](#real-time-pricing--cost-calculation)
6. [Checkout & Payment](#checkout--payment)
7. [Post-Payment & Pickup](#post-payment--pickup)
8. [Additional Features](#additional-features)
9. [Design System Summary](#design-system-summary)

---

## Design System Foundation

### Color Palette
- **Primary Blue**: `#0066FF` (vibrant, trustworthy blue)
- **Primary Blue Hover**: `#0052CC` (darker for interactions)
- **Primary Blue Light**: `#E6F0FF` (backgrounds, subtle highlights)
- **White**: `#FFFFFF` (backgrounds, cards)
- **Neutral Gray 900**: `#1A1A1A` (primary text)
- **Neutral Gray 600**: `#666666` (secondary text)
- **Neutral Gray 200**: `#E5E5E5` (borders, dividers)
- **Success Green**: `#00C853` (confirmations, success states)
- **Error Red**: `#FF3B30` (errors, warnings)

### Typography
- **Heading Font**: Inter Bold (weights: 600, 700)
- **Body Font**: Inter Regular (weights: 400, 500)
- **Mobile Scale**:
  - H1: 28px / Bold / Line-height 1.2
  - H2: 22px / Bold / Line-height 1.3
  - H3: 18px / Semibold / Line-height 1.4
  - Body Large: 16px / Regular / Line-height 1.5
  - Body: 14px / Regular / Line-height 1.6
  - Caption: 12px / Regular / Line-height 1.5

### Spacing System
- Base unit: 4px
- Common spacing: 8px, 12px, 16px, 24px, 32px, 48px

### Border Radius
- Small (buttons, inputs): 8px
- Medium (cards): 12px
- Large (modals): 16px

---

## User Authentication & Profile

### 1.1 Sign-Up / Login Screen

**Layout (Mobile-First)**
\`\`\`
┌─────────────────────────┐
│                         │
│    [AutoPrint Logo]     │ ← 48px height, centered
│                         │
│   "Welcome to           │ ← H1, Gray 900
│    AutoPrint"           │
│                         │
│   "Print instantly,     │ ← Body, Gray 600
│    pick up anywhere"    │
│                         │
│  ┌───────────────────┐  │
│  │ 📧 Email          │  │ ← Input field, 48px height
│  └───────────────────┘  │
│                         │
│  ┌───────────────────┐  │
│  │ 🔒 Password       │  │
│  └───────────────────┘  │
│                         │
│  ┌───────────────────┐  │
│  │   Sign In         │  │ ← Primary button, Blue
│  └───────────────────┘  │
│                         │
│  ────── OR ──────       │ ← Divider with text
│                         │
│  ┌───────────────────┐  │
│  │ 🔵 Google Sign In │  │ ← Secondary button, White
│  └───────────────────┘  │
│                         │
│  ┌───────────────────┐  │
│  │ 🎓 University SSO │  │
│  └───────────────────┘  │
│                         │
│  "Don't have account?   │ ← Caption, centered
│   Sign Up"              │    Link in Blue
│                         │
└─────────────────────────┘
\`\`\`

**Design Details**:
- **Background**: White with subtle blue gradient overlay at top (10% opacity)
- **Logo**: Blue icon with wordmark, positioned 32px from top
- **Input Fields**: 
  - White background with Gray 200 border (1px)
  - Focus state: Blue border (2px) with blue glow
  - Icons: Gray 600, positioned left (16px padding)
  - Text: Gray 900, 16px
  - Placeholder: Gray 600, 14px
- **Primary Button**: 
  - Blue background, white text, 48px height
  - Hover: Darker blue with subtle lift shadow
  - Active: Pressed state with scale 0.98
- **Social Buttons**: 
  - White background, Gray 900 text, Gray 200 border
  - Icons: Brand colors (Google blue, etc.)
  - 48px height, 16px padding

**Interaction**:
- Smooth transitions (200ms ease)
- Error states: Red border + error message below field
- Loading state: Button shows spinner, disabled state

---

### 1.2 User Dashboard

**Layout (Mobile-First)**
\`\`\`
┌─────────────────────────┐
│ ☰  AutoPrint      👤    │ ← Header: 56px height
├─────────────────────────┤
│                         │
│  Hi, John! 👋           │ ← H2, Gray 900
│                         │
│  ┌───────────────────┐  │
│  │ 📄 New Print Job  │  │ ← Large CTA card
│  │                   │  │   Blue background
│  │ Upload & Print →  │  │   White text
│  └───────────────────┘  │
│                         │
│  Quick Stats            │ ← H3, Gray 900
│  ┌─────┐  ┌─────┐      │
│  │  5  │  │ ₦450│      │ ← Stat cards
│  │Jobs │  │Spent│      │   White, bordered
│  └─────┘  └─────┘      │
│                         │
│  Recent Orders          │ ← H3, Gray 900
│  ┌───────────────────┐  │
│  │ 📄 Assignment.pdf │  │ ← Order card
│  │ Ready for Pickup  │  │   White background
│  │ Stand A • ₦120    │  │   Green status badge
│  │ 2 hours ago       │  │
│  └───────────────────┘  │
│                         │
│  ┌───────────────────┐  │
│  │ 📄 Notes.pdf      │  │
│  │ Completed ✓       │  │
│  │ Stand B • ₦80     │  │
│  │ Yesterday         │  │
│  └───────────────────┘  │
│                         │
│  [View All Orders →]    │ ← Text link, Blue
│                         │
└─────────────────────────┘
\`\`\`

**Design Details**:
- **Header**: 
  - White background, subtle shadow
  - Hamburger menu (left): Opens navigation drawer
  - Profile icon (right): Opens account menu
  - Height: 56px, padding: 16px
- **CTA Card**: 
  - Blue gradient background
  - White text, 24px heading
  - 120px height, 16px padding
  - Rounded corners (12px)
  - Subtle shadow for depth
- **Stat Cards**: 
  - White background, Gray 200 border
  - Large number (32px, Bold, Blue)
  - Label (12px, Gray 600)
  - 80px width, 80px height
  - 12px gap between cards
- **Order Cards**: 
  - White background, Gray 200 border
  - 16px padding
  - Status badge: Pill shape, colored background
    - Ready: Green background, white text
    - Printing: Blue background, white text
    - Completed: Gray background, white text
  - Document icon: 24px, Gray 600
  - Title: 16px, Bold, Gray 900
  - Details: 14px, Gray 600
  - Timestamp: 12px, Gray 600

**Interaction**:
- Pull-to-refresh for order updates
- Tap order card: Navigate to order details
- Swipe order card: Quick actions (view, reorder)

---

## File Upload & Configuration

### 2.1 File Upload Screen

**Layout (Mobile-First)**
\`\`\`
┌─────────────────────────┐
│ ← AutoPrint             │ ← Header with back button
├─────────────────────────┤
│                         │
│  Upload Document        │ ← H2, Gray 900
│  Step 1 of 4            │ ← Caption, Gray 600
│                         │
│  ┌───────────────────┐  │
│  │                   │  │
│  │    📤             │  │ ← Upload zone
│  │                   │  │   Dashed border
│  │  Drag & Drop      │  │   Blue accent
│  │  or tap to browse │  │   160px height
│  │                   │  │
│  │  PDF, DOCX, PPTX  │  │
│  │  JPG, PNG         │  │
│  │  Max 50MB         │  │
│  └───────────────────┘  │
│                         │
│  ────── OR ──────       │
│                         │
│  ┌───────────────────┐  │
│  │ ☁️ Google Drive   │  │ ← Cloud service buttons
│  └───────────────────┘  │
│                         │
│  ┌───────────────────┐  │
│  │ 📦 Dropbox        │  │
│  └───────────────────┘  │
│                         │
│  Recent Files           │ ← H3, Gray 900
│  ┌───────────────────┐  │
│  │ 📄 Assignment.pdf │  │ ← Recent file card
│  │ 2.4 MB • 5 pages  │  │
│  └───────────────────┘  │
│                         │
└─────────────────────────┘
\`\`\`

**Design Details**:
- **Upload Zone**: 
  - Dashed border (2px, Blue, 8px dash spacing)
  - Blue light background (#E6F0FF)
  - Upload icon: 48px, Blue
  - Heading: 18px, Bold, Gray 900
  - Instructions: 14px, Gray 600
  - File types: 12px, Gray 600
  - Hover state: Solid blue border, darker background
  - Active (dragging): Animated border, scale 1.02
- **Cloud Buttons**: 
  - White background, Gray 200 border
  - Brand icons (left aligned)
  - 48px height, full width
  - 12px gap between buttons
- **Recent Files**: 
  - White cards, Gray 200 border
  - Document icon + filename (truncated)
  - File size and page count
  - Tap to reuse file

**Interaction**:
- Drag-over animation: Border pulses
- Upload progress: Linear progress bar (Blue)
- Success: Checkmark animation, proceed to preview
- Error: Red border, error message below zone

---

### 2.2 Document Preview Screen

**Layout (Mobile-First)**
\`\`\`
┌─────────────────────────┐
│ ← Document Preview      │ ← Header
├─────────────────────────┤
│                         │
│  Assignment.pdf         │ ← H3, Gray 900
│  5 pages • 2.4 MB       │ ← Caption, Gray 600
│                         │
│  ┌───────────────────┐  │
│  │                   │  │
│  │   [Page Preview]  │  │ ← Document preview
│  │                   │  │   White background
│  │   Page 1 of 5     │  │   Shadow for depth
│  │                   │  │   280px height
│  │   ← →             │  │   Swipe navigation
│  └───────────────────┘  │
│                         │
│  ◉ ◉ ◉ ◯ ◯             │ ← Page indicators
│                         │
│  ┌───────────────────┐  │
│  │ ✓ Looks good!     │  │ ← Confirmation message
│  │ Ready to configure│  │   Green background
│  └───────────────────┘  │
│                         │
│  ┌───────────────────┐  │
│  │ Continue →        │  │ ← Primary button
│  └───────────────────┘  │
│                         │
│  [Upload Different File]│ ← Secondary link
│                         │
└─────────────────────────┘
\`\`\`

**Design Details**:
- **Preview Container**: 
  - White background with shadow
  - Document rendered as image/canvas
  - Pinch-to-zoom enabled
  - Swipe left/right for pages
  - Page counter overlay (bottom center)
- **Page Indicators**: 
  - Dots: 8px diameter
  - Active: Blue, filled
  - Inactive: Gray 200, outlined
  - 8px gap between dots
- **Confirmation Banner**: 
  - Green light background (#E8F5E9)
  - Green text, checkmark icon
  - 16px padding, rounded corners
- **Auto-conversion Notice** (if applicable):
  \`\`\`
  ┌───────────────────┐
  │ ℹ️ Converting...  │ ← Info banner
  │ DOCX → PDF        │   Blue background
  └───────────────────┘
  \`\`\`

**Interaction**:
- Swipe gestures for page navigation
- Tap preview: Full-screen view
- Loading state: Skeleton screen while rendering
- Conversion progress: Animated progress bar

---

## Print Job Configuration

### 3.1 Stand Selection Screen

**Layout (Mobile-First)**
\`\`\`
┌─────────────────────────┐
│ ← Select Print Stand    │ ← Header
├─────────────────────────┤
│                         │
│  Choose Pickup Location │ ← H2, Gray 900
│  Step 2 of 4            │ ← Caption, Gray 600
│                         │
│  ┌───────────────────┐  │
│  │   [Map View]      │  │ ← Interactive map
│  │                   │  │   200px height
│  │   📍 📍 📍        │  │   Stand markers
│  └───────────────────┘  │
│                         │
│  [🗺️ Map] [📋 List]    │ ← Toggle view
│                         │
│  Nearby Stands          │ ← H3, Gray 900
│                         │
│  ┌───────────────────┐  │
│  │ 📍 Stand A        │  │ ← Stand card (selected)
│  │ Library Building  │  │   Blue border
│  │ 🟢 Online         │  │   Blue background
│  │ 0.2 km away       │  │
│  │ ₦10/page B&W      │  │
│  └───────────────────┘  │
│                         │
│  ┌───────────────────┐  │
│  │ 📍 Stand B        │  │ ← Stand card (available)
│  │ Student Center    │  │   White background
│  │ 🟡 Busy           │  │   Gray border
│  │ 0.5 km away       │  │
│  │ ₦12/page B&W      │  │
│  └───────────────────┘  │
│                         │
│  ┌───────────────────┐  │
│  │ 📍 Stand C        │  │ ← Stand card (offline)
│  │ Engineering Block │  │   Disabled state
│  │ 🔴 Offline        │  │   Gray background
│  │ 0.8 km away       │  │
│  └───────────────────┘  │
│                         │
│  ┌───────────────────┐  │
│  │ Continue →        │  │ ← Primary button
│  └───────────────────┘  │
│                         │
└─────────────────────────┘
\`\`\`

**Design Details**:
- **Map View**: 
  - Interactive map (Mapbox/Google Maps)
  - Custom markers: Blue pins with stand letter
  - User location: Blue dot with pulse animation
  - Tap marker: Highlight corresponding card
  - 200px height, rounded corners
- **Toggle Buttons**: 
  - Segmented control style
  - Active: Blue background, white text
  - Inactive: White background, Gray 600 text
  - 40px height, equal width
- **Stand Cards**: 
  - **Selected State**: 
    - Blue border (2px)
    - Blue light background
    - Checkmark icon (top right)
  - **Available State**: 
    - White background
    - Gray 200 border (1px)
    - Tap to select
  - **Offline State**: 
    - Gray 100 background
    - Gray 400 text
    - Disabled, no interaction
  - **Status Indicators**: 
    - Online: Green dot + "Online"
    - Busy: Yellow dot + "Busy"
    - Offline: Red dot + "Offline"
    - 8px dot, 12px text
  - **Content**: 
    - Stand name: 16px, Bold, Gray 900
    - Location: 14px, Gray 600
    - Distance: 14px, Gray 600, with location icon
    - Pricing: 14px, Gray 900, Bold

**Interaction**:
- Tap card: Select stand, update map center
- Tap map marker: Scroll to card, highlight
- Real-time status updates (WebSocket)
- Distance calculation from user location

---

### 3.2 Print Settings Screen

**Layout (Mobile-First)**
\`\`\`
┌─────────────────────────┐
│ ← Print Settings        │ ← Header
├─────────────────────────┤
│                         │
│  Configure Your Print   │ ← H2, Gray 900
│  Step 3 of 4            │ ← Caption, Gray 600
│                         │
│  ┌───────────────────┐  │
│  │ 📄 Assignment.pdf │  │ ← Document summary
│  │ 5 pages • Stand A │  │   Collapsible card
│  └───────────────────┘  │
│                         │
│  Color Mode             │ ← H3, Gray 900
│  ┌─────────┬─────────┐  │
│  │ ⚫ B&W  │ 🎨 Color│  │ ← Toggle cards
│  │ ₦10/pg  │ ₦30/pg  │  │   Selected: Blue
│  └─────────┴─────────┘  │
│                         │
│  Printing Mode          │ ← H3, Gray 900
│  ┌─────────┬─────────┐  │
│  │ Single  │ Double  │  │ ← Toggle cards
│  │ Sided   │ Sided   │  │
│  └─────────┴─────────┘  │
│                         │
│  Page Range             │ ← H3, Gray 900
│  ┌───────────────────┐  │
│  │ ◉ All pages (1-5) │  │ ← Radio options
│  └───────────────────┘  │
│  ┌───────────────────┐  │
│  │ ◯ Custom range    │  │
│  │ ┌───────────────┐ │  │
│  │ │ e.g., 1-3, 5  │ │  │ ← Input field
│  │ └───────────────┘ │  │   (appears when selected)
│  └───────────────────┘  │
│                         │
│  Number of Copies       │ ← H3, Gray 900
│  ┌───────────────────┐  │
│  │  [-]  2  [+]      │  │ ← Stepper control
│  └───────────────────┘  │
│                         │
│  Paper Size             │ ← H3, Gray 900
│  ┌───────────────────┐  │
│  │ A4 (Standard) ▼   │  │ ← Dropdown
│  └───────────────────┘  │
│                         │
│  ┌───────────────────┐  │
│  │ Continue →        │  │ ← Primary button
│  └───────────────────┘  │
│                         │
└─────────────────────────┘
\`\`\`

**Design Details**:
- **Document Summary Card**: 
  - White background, Gray 200 border
  - Collapsible (tap to expand/collapse)
  - Shows: filename, page count, selected stand
  - 16px padding
- **Toggle Cards (Color/Print Mode)**: 
  - Grid layout, 2 columns, 8px gap
  - Each card: 
    - White background, Gray 200 border
    - Selected: Blue border (2px), Blue light background
    - Icon + label + price
    - 80px height, centered content
    - Tap to toggle
- **Radio Options**: 
  - White background, Gray 200 border
  - Selected: Blue border, blue radio button
  - 48px height, 16px padding
  - Radio button: 20px, left aligned
- **Custom Range Input**: 
  - Appears with smooth slide-down animation
  - White background, Gray 200 border
  - Placeholder: "e.g., 1-3, 5"
  - Validation: Real-time check for valid format
  - Error state: Red border + helper text
- **Stepper Control**: 
  - Horizontal layout: [-] [Number] [+]
  - Buttons: 40px × 40px, Gray 200 border
  - Number: 20px, Bold, Gray 900, centered
  - Min: 1, Max: 99
  - Disabled state when at limits
- **Dropdown**: 
  - White background, Gray 200 border
  - Chevron icon (right)
  - Opens bottom sheet with options
  - Options: A4, A3 (if available)

**Interaction**:
- Real-time validation for page range
- Stepper: Tap or long-press for rapid increment
- Dropdown: Bottom sheet modal with options
- Settings persist if user goes back

---

## Real-Time Pricing & Cost Calculation

### 4.1 Price Summary (Sticky Footer)

**Layout (Mobile-First)**
\`\`\`
┌─────────────────────────┐
│                         │
│  [Print Settings Above] │
│                         │
│  ...                    │
│                         │
├─────────────────────────┤ ← Sticky divider
│  ┌───────────────────┐  │
│  │ Cost Breakdown    │  │ ← Expandable summary
│  │                   │  │   Always visible
│  │ 5 pages × 2 copies│  │   White background
│  │ B&W, Double-sided │  │   Shadow for elevation
│  │                   │  │
│  │ Total: ₦120       │  │ ← Large, Bold, Blue
│  │                   │  │
│  │ [View Details ▼]  │  │ ← Expand button
│  └───────────────────┘  │
│                         │
│  ┌───────────────────┐  │
│  │ Continue to Pay → │  │ ← Primary button
│  └───────────────────┘  │
│                         │
└─────────────────────────┘
\`\`\`

**Expanded State**:
\`\`\`
┌─────────────────────────┐
│  ┌───────────────────┐  │
│  │ Cost Breakdown ▲  │  │ ← Expanded summary
│  │                   │  │
│  │ Pages: 5 × 2      │  │ ← Line items
│  │ = 10 pages        │  │   14px, Gray 600
│  │                   │  │
│  │ B&W Rate          │  │
│  │ 10 pages × ₦10    │  │
│  │ = ₦100            │  │
│  │                   │  │
│  │ Double-sided      │  │
│  │ -₦20 (discount)   │  │ ← Green text
│  │                   │  │
│  │ Stand Fee         │  │
│  │ = ₦40             │  │
│  │ ─────────────     │  │ ← Divider
│  │ Total: ₦120       │  │ ← 20px, Bold, Blue
│  └───────────────────┘  │
│                         │
│  ┌───────────────────┐  │
│  │ Continue to Pay → │  │
│  └───────────────────┘  │
│                         │
└─────────────────────────┘
\`\`\`

**Design Details**:
- **Sticky Footer**: 
  - Fixed to bottom of screen
  - White background with top shadow
  - 16px padding
  - Stays visible while scrolling settings
- **Collapsed State**: 
  - Summary text: 14px, Gray 600
  - Total: 24px, Bold, Blue
  - Expand button: 14px, Blue, with chevron
- **Expanded State**: 
  - Smooth slide-down animation (300ms)
  - Line items: Left-aligned label, right-aligned value
  - Discounts: Green text with minus sign
  - Divider: Gray 200, 1px, 16px margin
  - Total: Emphasized with larger size and color
- **Real-Time Updates**: 
  - Price updates instantly when settings change
  - Subtle pulse animation on total when updated
  - Transition: 200ms ease

**Interaction**:
- Tap "View Details": Expand/collapse breakdown
- Price updates trigger brief highlight animation
- Scroll behavior: Footer stays fixed at bottom

---

## Checkout & Payment

### 5.1 Payment Method Selection

**Layout (Mobile-First)**
\`\`\`
┌─────────────────────────┐
│ ← Payment               │ ← Header
├─────────────────────────┤
│                         │
│  Complete Your Order    │ ← H2, Gray 900
│  Step 4 of 4            │ ← Caption, Gray 600
│                         │
│  ┌───────────────────┐  │
│  │ Order Summary     │  │ ← Summary card
│  │                   │  │   Blue light background
│  │ Assignment.pdf    │  │
│  │ 5 pages, B&W      │  │
│  │ Stand A           │  │
│  │                   │  │
│  │ Total: ₦120       │  │ ← Bold, Blue
│  └───────────────────┘  │
│                         │
│  Payment Method         │ ← H3, Gray 900
│                         │
│  ┌───────────────────┐  │
│  │ 💳 Card Payment   │  │ ← Payment option card
│  │ Visa, Mastercard  │  │   Selected: Blue border
│  │ ◉                 │  │   Radio button (right)
│  └───────────────────┘  │
│                         │
│  ┌───────────────────┐  │
│  │ 📱 Mobile Money   │  │
│  │ M-Pesa, Airtel    │  │
│  │ ◯                 │  │
│  └───────────────────┘  │
│                         │
│  ┌───────────────────┐  │
│  │ 🎓 Campus Wallet  │  │
│  │ University debit  │  │
│  │ ◯                 │  │
│  └───────────────────┘  │
│                         │
│  Saved Cards            │ ← H3, Gray 900
│  ┌───────────────────┐  │
│  │ 💳 •••• 4242      │  │ ← Saved card
│  │ Expires 12/25     │  │   Quick select
│  │ ◯                 │  │
│  └───────────────────┘  │
│                         │
│  ┌───────────────────┐  │
│  │ Pay ₦120 →        │  │ ← Primary button
│  └───────────────────┘  │
│                         │
│  🔒 Secure payment    │  ← Trust indicator
│  SSL encrypted        │    12px, Gray 600
│                         │
└─────────────────────────┘
\`\`\`

**Design Details**:
- **Order Summary Card**: 
  - Blue light background (#E6F0FF)
  - 16px padding, rounded corners
  - Document icon + details
  - Total: 20px, Bold, Blue
  - Collapsible (tap to expand for full breakdown)
- **Payment Option Cards**: 
  - White background, Gray 200 border
  - Selected: Blue border (2px), blue radio button
  - Icon (left): 32px, colored
  - Label: 16px, Bold, Gray 900
  - Description: 14px, Gray 600
  - Radio button (right): 20px
  - 72px height, 16px padding
  - Tap anywhere to select
- **Saved Cards**: 
  - Similar card style
  - Card icon + masked number
  - Expiry date below
  - Swipe left: Delete option
- **Pay Button**: 
  - Blue background, white text
  - Shows total amount
  - 48px height, full width
  - Loading state: Spinner + "Processing..."
- **Trust Indicators**: 
  - Lock icon + "Secure payment"
  - SSL badge
  - Centered, Gray 600
  - 12px text

**Interaction**:
- Tap card: Select payment method, show input form
- Smooth transition to payment form
- Auto-save card option (checkbox)

---

### 5.2 Card Payment Form

**Layout (Mobile-First)**
\`\`\`
┌─────────────────────────┐
│ ← Card Payment          │ ← Header
├─────────────────────────┤
│                         │
│  Enter Card Details     │ ← H2, Gray 900
│                         │
│  ┌───────────────────┐  │
│  │ Card Number       │  │ ← Input field
│  │ 1234 5678 9012... │  │   Auto-formatting
│  │ 💳                │  │   Card icon (right)
│  └───────────────────┘  │
│                         │
│  ┌─────────┬─────────┐  │
│  │ Expiry  │ CVV     │  │ ← Split inputs
│  │ MM/YY   │ •••     │  │   2 columns
│  └─────────┴─────────┘  │
│                         │
│  ┌───────────────────┐  │
│  │ Cardholder Name   │  │
│  │ John Doe          │  │
│  └───────────────────┘  │
│                         │
│  ☐ Save card for      │  ← Checkbox
│     future payments   │    14px, Gray 600
│                         │
│  ┌───────────────────┐  │
│  │ Pay ₦120 →        │  │ ← Primary button
│  └───────────────────┘  │
│                         │
│  🔒 Your payment is   │  ← Trust message
│  secured by Stripe    │    Centered, Gray 600
│                         │
└─────────────────────────┘
\`\`\`

**Design Details**:
- **Input Fields**: 
  - White background, Gray 200 border
  - Focus: Blue border (2px)
  - 48px height, 16px padding
  - Card number: Auto-format with spaces
  - Card icon: Detects card type (Visa, Mastercard)
  - Expiry: Auto-format MM/YY
  - CVV: Masked input, max 4 digits
  - Error state: Red border + error message below
- **Split Inputs**: 
  - Expiry (60%) + CVV (40%)
  - 8px gap between fields
- **Checkbox**: 
  - Blue when checked
  - 20px size, rounded corners
  - Label: 14px, Gray 600
- **Payment Button**: 
  - Disabled until form is valid
  - Loading state: Spinner + "Processing..."
  - Success: Checkmark animation

**Interaction**:
- Real-time validation
- Card type detection (icon changes)
- Auto-advance to next field
- Error handling: Clear, actionable messages

---

### 5.3 Payment Processing & Confirmation

**Processing State**:
\`\`\`
┌─────────────────────────┐
│                         │
│                         │
│      [Spinner]          │ ← Animated spinner
│                         │   Blue color
│   Processing Payment    │   48px size
│                         │
│   Please wait...        │ ← 14px, Gray 600
│                         │
│   Do not close this     │ ← Warning text
│   window                │   12px, Gray 600
│                         │
└─────────────────────────┘
\`\`\`

**Success State**:
\`\`\`
┌─────────────────────────┐
│                         │
│      ✓                  │ ← Success icon
│                         │   Green, 64px
│   Payment Successful!   │   Animated checkmark
│                         │
│  ┌───────────────────┐  │
│  │ Order #AP12345    │  │ ← Order details card
│  │                   │  │   White background
│  │ Assignment.pdf    │  │   Green border
│  │ Stand A           │  │
│  │ ₦120 paid         │  │
│  │                   │  │
│  │ [QR Code]         │  │ ← Pickup QR code
│  │                   │  │   120px size
│  │ Show this at      │  │
│  │ pickup            │  │
│  └───────────────────┘  │
│                         │
│  Status: In Queue       │ ← Status badge
│                         │   Blue background
│  ┌───────────────────┐  │
│  │ Track Order →     │  │ ← Primary button
│  └───────────────────┘  │
│                         │
│  [Download Receipt]     │ ← Secondary link
│  [Print Another]        │
│                         │
└─────────────────────────┘
\`\`\`

**Error State**:
\`\`\`
┌─────────────────────────┐
│                         │
│      ✕                  │ ← Error icon
│                         │   Red, 64px
│   Payment Failed        │
│                         │
│  ┌───────────────────┐  │
│  │ ⚠️ Error          │  │ ← Error card
│  │                   │  │   Red light background
│  │ Insufficient      │  │
│  │ funds             │  │ ← Error message
│  │                   │  │   14px, Gray 900
│  └───────────────────┘  │
│                         │
│  ┌───────────────────┐  │
│  │ Try Again         │  │ ← Primary button
│  └───────────────────┘  │
│                         │
│  [Change Payment Method]│ ← Secondary link
│  [Contact Support]      │
│                         │
└─────────────────────────┘
\`\`\`

**Design Details**:
- **Processing**: 
  - Full-screen overlay
  - White background
  - Centered content
  - Spinner: Blue, 48px, smooth rotation
  - Prevent back navigation
- **Success**: 
  - Checkmark animation: Scale + fade in
  - Green color (#00C853)
  - Order card: White with green border
  - QR code: High contrast, 120px
  - Status badge: Pill shape, colored
- **Error**: 
  - Error icon: Red, animated shake
  - Error card: Red light background
  - Clear error message
  - Actionable buttons

**Interaction**:
- Success: Auto-navigate to tracking after 3s
- Error: Allow retry or method change
- QR code: Tap to enlarge, long-press to save

---

## Post-Payment & Pickup

### 6.1 Order Tracking Screen

**Layout (Mobile-First)**
\`\`\`
┌─────────────────────────┐
│ ← Order #AP12345        │ ← Header
├─────────────────────────┤
│                         │
│  ┌───────────────────┐  │
│  │   [QR Code]       │  │ ← Large QR code
│  │                   │  │   White background
│  │   Order #AP12345  │  │   200px size
│  │                   │  │   Centered
│  │   Tap to enlarge  │  │
│  └───────────────────┘  │
│                         │
│  Status: Printing       │ ← Status badge
│                         │   Blue, animated
│  ┌───────────────────┐  │
│  │ ● Paid ✓          │  │ ← Progress tracker
│  │ │                 │  │   Vertical timeline
│  │ ● In Queue ✓      │  │   Green: completed
│  │ │                 │  │   Blue: current
│  │ ● Printing...     │  │   Gray: pending
│  │ │                 │  │
│  │ ○ Ready for Pickup│  │
│  └───────────────────┘  │
│                         │
│  Order Details          │ ← H3, Gray 900
│  ┌───────────────────┐  │
│  │ 📄 Assignment.pdf │  │ ← Details card
│  │ 5 pages, B&W      │  │   White background
│  │ 2 copies          │  │
│  │                   │  │
│  │ 📍 Stand A        │  │
│  │ Library Building  │  │
│  │                   │  │
│  │ 💰 ₦120 paid      │  │
│  │ Card •••• 4242    │  │
│  │                   │  │
│  │ 🕐 2:45 PM        │  │
│  │ Today             │  │
│  └───────────────────┘  │
│                         │
│  ┌───────────────────┐  │
│  │ 🔔 Notify Me      │  │ ← Toggle button
│  │ When ready        │  │   Switch (right)
│  └───────────────────┘  │
│                         │
│  [Download Receipt]     │ ← Secondary links
│  [Get Directions]       │
│  [Contact Support]      │
│                         │
└─────────────────────────┘
\`\`\`

**Ready for Pickup State**:
\`\`\`
┌─────────────────────────┐
│ ← Order #AP12345        │
├─────────────────────────┤
│                         │
│  ┌───────────────────┐  │
│  │   [QR Code]       │  │ ← Pulsing animation
│  │                   │  │   Green border
│  │   Order #AP12345  │  │
│  │                   │  │
│  │   Show at Stand A │  │
│  └───────────────────┘  │
│                         │
│  ┌───────────────────┐  │
│  │ ✓ Ready for       │  │ ← Success banner
│  │   Pickup!         │  │   Green background
│  │                   │  │   Animated
│  │ Your order is     │  │
│  │ waiting at Stand A│  │
│  └───────────────────┘  │
│                         │
│  ┌───────────────────┐  │
│  │ ● Paid ✓          │  │
│  │ ● In Queue ✓      │  │
│  │ ● Printing ✓      │  │
│  │ ● Ready ✓         │  │ ← All green
│  └───────────────────┘  │
│                         │
│  ┌───────────────────┐  │
│  │ 📍 Get Directions │  │ ← Action button
│  └───────────────────┘  │
│                         │
│  Pickup Instructions    │
│  1. Go to Stand A       │
│  2. Show QR code        │
│  3. Collect documents   │
│                         │
└─────────────────────────┘
\`\`\`

**Design Details**:
- **QR Code**: 
  - White background with shadow
  - 200px size (tap to enlarge to full screen)
  - Order number below (16px, Bold)
  - Current state: Blue border
  - Ready state: Green border with pulse
- **Status Badge**: 
  - Pill shape, 32px height
  - Colored background (Blue/Green)
  - White text, 14px, Bold
  - Animated: Subtle pulse when active
- **Progress Tracker**: 
  - Vertical timeline
  - Dots: 16px diameter
  - Lines: 2px width, connecting dots
  - Completed: Green dot + checkmark
  - Current: Blue dot + animated pulse
  - Pending: Gray outlined dot
  - Labels: 14px, aligned right
- **Details Card**: 
  - White background, Gray 200 border
  - 16px padding
  - Icons: 20px, Gray 600
  - Labels: 14px, Gray 600
  - Values: 14px, Gray 900
  - Sections separated by 12px spacing
- **Notification Toggle**: 
  - White card, Gray 200 border
  - Switch: Blue when on, Gray when off
  - Label: 14px, Gray 900
- **Ready Banner**: 
  - Green background (#E8F5E9)
  - Green text, checkmark icon
  - 16px padding
  - Animated: Slide down + bounce

**Interaction**:
- Real-time status updates (WebSocket)
- Push notification when ready
- QR code: Tap to enlarge, brightness boost
- Directions: Opens maps app
- Auto-refresh every 30 seconds

---

### 6.2 Pickup Confirmation (Attendant View)

**Layout (Mobile-First - Attendant Interface)**
\`\`\`
┌─────────────────────────┐
│ AutoPrint Stand A       │ ← Header
├─────────────────────────┤
│                         │
│  Pending Orders (3)     │ ← H2, Gray 900
│                         │
│  ┌───────────────────┐  │
│  │ #AP12345          │  │ ← Order card
│  │ Assignment.pdf    │  │   White background
│  │ 5 pages, B&W, x2  │  │   Blue border
│  │                   │  │
│  │ ₦120 • 2:45 PM    │  │
│  │                   │  │
│  │ [Mark Ready]      │  │ ← Action button
│  └───────────────────┘  │
│                         │
│  ┌───────────────────┐  │
│  │ [Scan QR Code]    │  │ ← Scan button
│  └───────────────────┘  │
│                         │
│  Ready for Pickup (2)   │ ← H3, Gray 900
│  ┌───────────────────┐  │
│  │ #AP12344          │  │ ← Ready order
│  │ Notes.pdf         │  │   Green border
│  │ Ready 5 min ago   │  │
│  │                   │  │
│  │ [Confirm Pickup]  │  │
│  └───────────────────┘  │
│                         │
└─────────────────────────┘
\`\`\`

**QR Scan View**:
\`\`\`
┌─────────────────────────┐
│ ← Scan QR Code          │
├─────────────────────────┤
│                         │
│  ┌───────────────────┐  │
│  │                   │  │
│  │   [Camera View]   │  │ ← Camera feed
│  │                   │  │   Full width
│  │   ┌─────────┐     │  │   300px height
│  │   │         │     │  │
│  │   │  Scan   │     │  │ ← Scan frame
│  │   │  Frame  │     │  │   Animated corners
│  │   │         │     │  │
│  │   └─────────┘     │  │
│  │                   │  │
│  │ Align QR code     │  │
│  │ within frame      │  │
│  └───────────────────┘  │
│                         │
│  [Enter Order ID]       │ ← Manual entry option
│                         │
└─────────────────────────┘
\`\`\`

**Confirmation View**:
\`\`\`
┌─────────────────────────┐
│                         │
│      ✓                  │ ← Success icon
│                         │   Green, 64px
│   Order Confirmed       │
│                         │
│  ┌───────────────────┐  │
│  │ #AP12345          │  │ ← Order summary
│  │ Assignment.pdf    │  │   Green background
│  │ 5 pages, B&W, x2  │  │
│  │                   │  │
│  │ Picked up by:     │  │
│  │ John Doe          │  │
│  │ 3:15 PM           │  │
│  └───────────────────┘  │
│                         │
│  ┌───────────────────┐  │
│  │ Done              │  │ ← Primary button
│  └───────────────────┘  │
│                         │
└─────────────────────────┘
\`\`\`

**Design Details**:
- **Order Cards**: 
  - Pending: Blue border
  - Ready: Green border
  - Completed: Gray background
  - 16px padding
  - Order ID: 16px, Bold, Gray 900
  - Details: 14px, Gray 600
  - Timestamp: 12px, Gray 600
- **Action Buttons**: 
  - Mark Ready: Blue background
  - Confirm Pickup: Green background
  - 40px height, full width
- **Scan Button**: 
  - Large, prominent
  - Blue background, white text
  - Camera icon
  - 56px height
- **Camera View**: 
  - Full-width camera feed
  - Scan frame: Animated corners
  - White overlay with cutout
  - Auto-detect QR code
- **Confirmation**: 
  - Success animation
  - Order summary
  - Timestamp recorded

**Interaction**:
- Real-time order updates
- QR scan: Auto-detect and confirm
- Manual entry: Fallback option
- Audio/haptic feedback on scan
- Order moves to completed list

---

## Additional Features

### 7.1 Notifications

**Push Notification Examples**:
\`\`\`
┌─────────────────────────┐
│ 🔔 AutoPrint            │
│                         │
│ Your order is ready!    │
│ #AP12345 at Stand A     │
│                         │
│ 2 minutes ago           │
└─────────────────────────┘
\`\`\`

**In-App Notification Center**:
\`\`\`
┌─────────────────────────┐
│ ← Notifications         │
├─────────────────────────┤
│                         │
│  Today                  │
│  ┌───────────────────┐  │
│  │ ✓ Order Ready     │  │
│  │ #AP12345          │  │
│  │ 10 min ago        │  │
│  └───────────────────┘  │
│                         │
│  ┌───────────────────┐  │
│  │ 🖨️ Printing       │  │
│  │ #AP12345          │  │
│  │ 25 min ago        │  │
│  └───────────────────┘  │
│                         │
│  Yesterday              │
│  ┌───────────────────┐  │
│  │ ✓ Completed       │  │
│  │ #AP12344          │  │
│  └───────────────────┘  │
│                         │
└─────────────────────────┘
\`\`\`

---

### 7.2 Settings & Profile

**Profile Screen**:
\`\`\`
┌─────────────────────────┐
│ ← Profile               │
├─────────────────────────┤
│                         │
│      [Avatar]           │ ← 80px, centered
│                         │
│   John Doe              │ ← H2, centered
│   john@university.edu   │ ← Caption, Gray 600
│                         │
│  ┌───────────────────┐  │
│  │ Edit Profile →    │  │ ← Menu items
│  └───────────────────┘  │
│  ┌───────────────────┐  │
│  │ Payment Methods → │  │
│  └───────────────────┘  │
│  ┌───────────────────┐  │
│  │ Order History →   │  │
│  └───────────────────┘  │
│  ┌───────────────────┐  │
│  │ Notifications →   │  │
│  └───────────────────┘  │
│  ┌───────────────────┐  │
│  │ Help & Support →  │  │
│  └───────────────────┘  │
│  ┌───────────────────┐  │
│  │ About AutoPrint → │  │
│  └───────────────────┘  │
│                         │
│  [Log Out]              │ ← Red text link
│                         │
└─────────────────────────┘
\`\`\`

---

### 7.3 Error States & Empty States

**No Orders (Empty State)**:
\`\`\`
┌─────────────────────────┐
│                         │
│      📄                 │ ← Empty state icon
│                         │   Gray 400, 64px
│   No orders yet         │
│                         │
│   Upload a document     │ ← Body, Gray 600
│   to get started        │
│                         │
│  ┌───────────────────┐  │
│  │ Start Printing →  │  │ ← Primary button
│  └───────────────────┘  │
│                         │
└─────────────────────────┘
\`\`\`

**Network Error**:
\`\`\`
┌─────────────────────────┐
│                         │
│      ⚠️                 │ ← Error icon
│                         │   Red, 64px
│   Connection Error      │
│                         │
│   Please check your     │ ← Body, Gray 600
│   internet connection   │
│                         │
│  ┌───────────────────┐  │
│  │ Try Again         │  │ ← Primary button
│  └───────────────────┘  │
│                         │
└─────────────────────────┘
\`\`\`

---

## Design System Summary

### Key Principles
1. **Mobile-First**: All layouts optimized for small screens (320px+)
2. **High Contrast**: Vibrant blue (#0066FF) against white for clarity
3. **Trust Signals**: Security badges, SSL indicators, clear pricing
4. **Instant Feedback**: Real-time updates, loading states, smooth animations
5. **Accessibility**: High contrast ratios, large touch targets (48px minimum), clear labels

### Component Library

**Buttons**
- **Primary**: Blue (#0066FF) background, white text, 48px height, 8px radius
- **Secondary**: White background, Gray 200 border, Gray 900 text, 48px height
- **Destructive**: Red (#FF3B30) background, white text, 48px height

**Cards**
- White background
- Gray 200 (#E5E5E5) border, 1px
- 12px border radius
- 16px padding
- Subtle shadow for elevation

**Input Fields**
- White background
- Gray 200 border, 1px
- 48px height
- 16px padding
- Focus state: Blue border (2px) with subtle glow
- Error state: Red border with error message below

**Status Badges**
- Pill shape (fully rounded)
- 32px height
- Colored backgrounds (Blue, Green, Yellow, Red)
- White text, 14px, Bold
- 12px horizontal padding

**Progress Indicators**
- Spinners: Blue, 48px, smooth rotation
- Progress bars: Blue fill, Gray 200 background, 4px height
- Timelines: Vertical, 16px dots, 2px connecting lines

### Responsive Breakpoints
- **Mobile**: 320px - 767px (primary focus)
- **Tablet**: 768px - 1023px (enhanced layouts, larger previews)
- **Desktop**: 1024px+ (multi-column layouts, side-by-side views)

### Animation Guidelines
- **Duration**: 200ms for micro-interactions, 300ms for transitions
- **Easing**: ease-out for entrances, ease-in for exits
- **Loading states**: Skeleton screens, spinners, progress bars
- **Success states**: Checkmark animations, scale + fade
- **Error states**: Shake animations, color transitions

### Accessibility Standards
- **Color Contrast**: Minimum 4.5:1 for normal text, 3:1 for large text
- **Touch Targets**: Minimum 48px × 48px for all interactive elements
- **Focus Indicators**: Visible blue outline (2px) on all focusable elements
- **Screen Reader Support**: Proper ARIA labels, semantic HTML
- **Keyboard Navigation**: Full keyboard support for all interactions

---

## Implementation Notes

### Technology Stack Recommendations
- **Frontend Framework**: React Native or Flutter for mobile-first development
- **UI Components**: Custom components following this design system
- **State Management**: Redux or Context API for app state
- **Real-time Updates**: WebSocket for order status updates
- **Payment Integration**: Stripe, Paystack, or Flutterwave
- **File Upload**: Multipart form data with progress tracking
- **Maps Integration**: Google Maps or Mapbox for stand locations
- **QR Code**: QR code generation and scanning libraries

### Performance Considerations
- **Image Optimization**: Compress and lazy-load images
- **Code Splitting**: Load screens on-demand
- **Caching**: Cache user data, recent files, and stand information
- **Offline Support**: Queue actions when offline, sync when online
- **Progressive Enhancement**: Core functionality works without JavaScript

### Security Considerations
- **HTTPS**: All communications over secure connections
- **Payment Security**: PCI DSS compliance, tokenization
- **Authentication**: JWT tokens, secure session management
- **File Validation**: Server-side validation of file types and sizes
- **Rate Limiting**: Prevent abuse of upload and payment endpoints

---

## Conclusion

This comprehensive UI/UX design specification provides a complete blueprint for building AutoPrint's mobile-first print automation service. The design prioritizes:

1. **Speed**: Instant file upload, real-time pricing, quick payment
2. **Trust**: Clear pricing, secure payment indicators, professional design
3. **Clarity**: High contrast, intuitive layouts, clear status updates
4. **Accessibility**: Large touch targets, readable text, proper contrast

The vibrant blue and white color scheme creates a modern, professional aesthetic while maintaining excellent readability. Every screen is designed with mobile users in mind, ensuring a seamless experience from file upload to document pickup.

**Next Steps**:
1. Review and approve design specification
2. Create high-fidelity mockups in Figma or similar tool
3. Develop component library based on design system
4. Build and test each screen iteratively
5. Conduct user testing and iterate based on feedback
6. Launch MVP with core features
7. Gather analytics and user feedback for improvements

---

**Document Version**: 1.0  
**Last Updated**: January 2025  
**Created For**: AutoPrint Mobile Application
