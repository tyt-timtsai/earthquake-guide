# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository contains a single-file earthquake safety web application (`earthquake_safety_app.html`) - a progressive web app (PWA) providing earthquake safety guidance in multiple languages (English, Traditional Chinese, Japanese).

## Architecture

The project is built as a self-contained HTML file with embedded CSS and JavaScript:

- **Single-file architecture**: All styles, scripts, and markup in one HTML file
- **Multi-language support**: Built-in translation system with language selector
- **Mobile-first design**: Responsive layout optimized for mobile devices (414px max-width)
- **Progressive Web App features**: Service worker registration for offline functionality
- **Screen-based navigation**: Multiple screens managed through JavaScript with navigation stack
- **Touch gesture support**: Swipe gestures for mobile navigation

## Key Components

### Screen Management
- Home screen with location selection (indoor/outdoor/about)
- Emergency mode with urgent location selection
- Location-specific guides with Drop/Cover/Hold instructions
- Situation-specific detailed instructions
- About screen with safety principles

### Multi-language System
- Translation object structure in JavaScript
- Dynamic text updates via `data-text` attributes
- Speech synthesis support for audio instructions in all languages

### Navigation System
- Navigation stack for back button functionality
- Footer navigation for main screens
- Touch gesture support for swipe-to-go-back

## Development Notes

Since this is a single HTML file with no build system:

- **No package managers**: No npm, yarn, or other package management
- **No build process**: File can be opened directly in browser
- **No dependencies**: All functionality is vanilla HTML/CSS/JavaScript
- **Local development**: Simply open the file in a web browser
- **Testing**: Manual testing in browser, especially mobile viewport testing

## Common Tasks

- **Local testing**: Open `earthquake_safety_app.html` in any modern web browser
- **Mobile testing**: Use browser developer tools to simulate mobile devices
- **Language testing**: Use the language selector dropdown to test all translations
- **Audio testing**: Test speech synthesis functionality across different languages
- **Service Worker**: May need local server for service worker functionality in some browsers

## File Structure

The application uses a component-based approach within the single HTML file:
- CSS animations and responsive design
- JavaScript modules for different functionality (language, navigation, audio)
- Structured data for translations and situation-specific instructions

## Security Considerations

The application is client-side only with no external dependencies or server communication, making it safe for offline use during emergencies.