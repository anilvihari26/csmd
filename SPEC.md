# Public Safety App - Project Specification

## 1. Project Overview

**Project Name:** SafeGuard - Public Safety Application

**Project Type:** Responsive Web Application (PWA-ready)

**Core Functionality:** A comprehensive public safety application designed to help users in emergency situations with quick access to emergency services, location sharing, incident reporting, and safety resources.

**Target Users:** College students, general public, campus security personnel

---

## 2. UI/UX Specification

### Layout Structure

**Pages:**
1. **Home/Dashboard** - Main landing page with quick actions
2. **Emergency Contacts** - List of emergency numbers
3. **Report Incident** - Form to report incidents
4. **Safety Tips** - Educational safety content
5. **Safe Zones** - Interactive map showing safe locations

**Navigation:** Bottom tab navigation (mobile-first) + hamburger menu for desktop

**Responsive Breakpoints:**
- Mobile: < 768px
- Tablet: 768px - 1024px
- Desktop: > 1024px

### Visual Design

**Color Palette:**
- Primary: `#1E3A5F` (Deep Navy Blue - trust & security)
- Secondary: `#2ECC71` (Emergency Green - safety)
- Accent: `#E74C3C` (Alert Red - emergency)
- Background: `#F8F9FA` (Light Gray)
- Card Background: `#FFFFFF` (White)
- Text Primary: `#2C3E50` (Dark Gray)
- Text Secondary: `#7F8C8D` (Medium Gray)

**Typography:**
- Font Family: 'Poppins' (headings), 'Open Sans' (body)
- Heading Sizes: H1: 32px, H2: 24px, H3: 18px
- Body: 16px, Small: 14px

**Spacing System:**
- Base unit: 8px
- Padding: 16px (cards), 24px (sections)
- Margins: 16px between elements, 32px between sections
- Border Radius: 12px (cards), 8px (buttons), 50% (icons)

**Visual Effects:**
- Box Shadow: `0 4px 20px rgba(0,0,0,0.1)`
- Hover transitions: 0.3s ease
- Button hover: scale(1.02) with shadow increase
- Card hover: translateY(-4px)

### Components

**1. SOS Button (Hero)**
- Large circular button (120px diameter)
- Pulsing red animation
- One-tap activation
- States: Default (red), Active (flashing), Sending (loading)

**2. Emergency Contact Cards**
- Icon, title, phone number
- One-tap call functionality
- Add to contacts button

**3. Quick Action Grid**
- 2x3 grid on mobile, 6x1 row on desktop
- Icons with labels
- Tap feedback animation

**4. Incident Report Form**
- Category dropdown
- Description textarea
- Location picker (map integration)
- Anonymous toggle
- Submit button with loading state

**5. Safety Tips Cards**
- Image/icon, title, brief description
- Expandable for full content
- Category badges

**6. Safe Zone Map**
- Interactive map (Leaflet.js - OpenStreetMap)
- Markers for: Police, Hospital, Fire Station, Campus Security
- Current location indicator
- Filter controls

---

## 3. Functionality Specification

### Core Features

**F1: SOS Emergency Alert**
- One-tap emergency button
- Get user's current GPS location
- Show confirmation modal with countdown
- Share location + emergency message to pre-set contacts
- Trigger loud alarm sound (optional)

**F2: Emergency Contacts Directory**
- Pre-loaded emergency numbers:
  - Police: 100
  - Fire: 101
  - Ambulance: 102
  - Campus Security: [Custom]
  - Women Helpline: 1091
  - Child Helpline: 1098
- Add custom contacts
- One-tap dialing
- Copy number functionality

**F3: Incident Reporting**
- Categories: Theft, Harassment, Suspicious Activity, Accident, Fire, Medical Emergency, Other
- Photo upload option (simulated)
- Location auto-detection
- Description field (min 20 chars)
- Anonymous reporting option
- Success confirmation with reference ID

**F4: Safety Tips & Resources**
- Categories: Personal Safety, Road Safety, Cyber Safety, Fire Safety, First Aid
- Tips displayed as expandable cards
- Search functionality
- Bookmark favorite tips

**F5: Safe Zones Map**
- Interactive map with user location
- Different colored markers for:
  - 🔵 Police Stations
  - ❤️ Hospitals
  - 🟠 Fire Stations
  - 🟢 Campus Security
  - 🟡 Safe Shelters
- Distance calculation from user
- Directions to selected location
- Filter markers by category

**F6: Quick Actions Dashboard**
- SOS Button (prominent)
- Call Emergency
- Report Incident
- Find Safe Zone
- Add Emergency Contact
- Share Location

### User Interactions

- Swipe gestures for navigation
- Pull-to-refresh on lists
- Loading spinners for async operations
- Toast notifications for actions
- Confirmation dialogs for critical actions

### Data Handling

- Local Storage for:
  - Custom emergency contacts
  - Saved tips/bookmarks
  - User preferences
  - Recent reports (draft)
- Geolocation API for GPS
- No backend required (frontend demo)

### Edge Cases

- GPS permission denied: Show manual address entry
- No network: Show offline message with cached data
- Empty contacts: Show "Add your first contact" prompt
- Form validation errors: Inline error messages

---

## 4. Acceptance Criteria

### Visual Checkpoints

- [ ] App loads with blue/green/red color scheme
- [ ] SOS button pulses with animation
- [ ] All 6 quick action buttons visible on home
- [ ] Navigation works on mobile and desktop
- [ ] Cards have proper shadows and hover effects
- [ ] Map displays with markers

### Functional Checkpoints

- [ ] SOS button shows confirmation modal
- [ ] Emergency contacts can be dialed
- [ ] Incident form validates required fields
- [ ] Tips can be expanded/collapsed
- [ ] Map shows user's current location
- [ ] Data persists in localStorage

### Performance Checkpoints

- [ ] Page loads in under 3 seconds
- [ ] Animations run at 60fps
- [ ] No console errors
- [ ] Responsive on all breakpoints

---

## 5. Technical Stack

- **HTML5** - Semantic structure
- **CSS3** - Styling with Flexbox/Grid
- **JavaScript (ES6+)** - Functionality
- **Leaflet.js** - Map integration (CDN)
- **Font Awesome** - Icons (CDN)
- **Google Fonts** - Typography (CDN)
- **No frameworks** - Pure vanilla implementation
