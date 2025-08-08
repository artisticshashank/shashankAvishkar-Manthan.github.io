# Event Card System Guide

## Overview
The website now features an advanced two-card event system that provides an intuitive and interactive way to display event information.

## Features

### Main Event Card
- **Event Logo**: Displays in a circular container with hover effects
- **Event Date**: Shows date and month in the top-right corner
- **Event Title**: Prominently displayed with gradient text effects
- **Event Status**: Color-coded badges (Competition, Workshop, etc.)
- **Register Button**: Call-to-action button with hover animations

### Detail Event Card
- **Comprehensive Information**: Full event details with date, time, and location
- **Event Highlights**: Bulleted list of key features
- **Enhanced Tags**: More detailed categorization
- **Multiple Actions**: Register and Info buttons
- **Responsive Design**: Adapts to all screen sizes

## Event Logos
Event logos should be placed in: `assets/imgs/event-logos/`

Expected filenames:
- `ideathon.png`
- `elocution.png`
- `workshop.png`
- `mentorship.png`
- `walkathon.png`
- `awards.png`

If logo files are not found, the system will fallback to the main logo (`assets/imgs/logo/logo.png`).

## Interaction Methods

### Desktop
- **Click**: Click on the main card to open details
- **Hover**: Hover effects on all interactive elements
- **Close**: Click the X button or click outside to close

### Mobile
- **Tap**: Tap the main card to open details
- **Double Tap**: Alternative method for touch devices
- **Close**: Tap the X button or tap outside to close

### Keyboard
- **Escape Key**: Press Escape to close any open detail card

## Technical Implementation

### HTML Structure
```html
<div class="event-card-container" data-event="eventname">
  <!-- Main Card -->
  <div class="event-card main-card">
    <!-- Event logo, title, date, register button -->
  </div>
  
  <!-- Detail Card -->
  <div class="event-card detail-card">
    <!-- Comprehensive event information -->
  </div>
</div>
```

### CSS Classes
- `.event-card-container`: Wrapper for both cards
- `.main-card`: Primary card with basic info
- `.detail-card`: Expanded card with full details
- `.active`: Applied to detail card when visible

### JavaScript Events
- Click handlers for card interactions
- Escape key support
- Touch device optimization
- Accessibility features

## Customization

### Colors
Event status badges use different colors:
- **Competition**: Blue (`rgba(93, 93, 245, 0.8)`)
- **Workshop**: Teal (`rgba(69, 183, 209, 0.3)`)
- **Mentorship**: Green (`rgba(150, 206, 180, 0.3)`)
- **Community**: Orange (`rgba(78, 205, 196, 0.3)`)
- **Celebration**: Purple (`rgba(155, 89, 182, 0.3)`)

### Animation
- Glass morphism effects with backdrop-filter
- Smooth transitions with cubic-bezier timing
- 3D transform effects on hover
- Staggered loading animations

## Browser Support
- Modern browsers with CSS Grid support
- Webkit backdrop-filter support recommended
- Touch events for mobile devices
- Keyboard navigation support

## Performance
- Optimized for smooth animations
- Lazy loading for event logos
- Efficient event delegation
- Minimal DOM manipulation
