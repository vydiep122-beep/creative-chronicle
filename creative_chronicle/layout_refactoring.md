# Layout Refactoring Report - CreativeChronicle

## 1. Legacy Layout Problems

Float was designed mainly for wrapping content, not for building complete responsive layouts. Floated elements can cause their parent containers to collapse, requiring clearfix or overflow workarounds. Absolute positioning removes elements from normal document flow, so the parent does not automatically account for their height. Fixed dimensions also cause overlap on smaller screens.

## 2. New Layout Strategy

Flexbox is used for Author Info to align the avatar, author details and sharing buttons vertically. It supports flexible wrapping on mobile devices.

CSS Grid is used for the Mosaic Gallery. The main image spans two rows, while two smaller images occupy the right column. A media query changes the gallery to one column on mobile.

Bootstrap Grid is used for Recommended Articles with `col-12 col-md-6 col-lg-3`. This provides one column on mobile, two on tablets and four on desktop.