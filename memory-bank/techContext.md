# Technical Context: Freya Dataset Builder

## Technology Stack

### Frontend
- **HTML5** - Single file application
- **CSS3** - Dark mode and responsive design
- **Vanilla JavaScript** - No framework dependencies

### Storage & Sync
- **localStorage** - Primary data persistence
- **JSONL** - Data portability format
- **File API** - Backup/restore functionality

### Hosting
- **GitHub Pages** - Static site hosting
- **HTTPS** - Secure access
- **Custom Domain** - drifter-supremo.github.io/JSONgenerator

## Development & Deployment
- Single HTML file architecture
- No build process needed
- Direct GitHub deployment
- Instant updates

## Technical Architecture

### Data Layer
```javascript
// localStorage Structure
{
  freya_dataset: [
    {
      input: string,  // User input with "user: " prefix
      output: string  // Freya response with "Freya: " prefix
    },
    // ... more examples
  ]
}
```

### Export Format (JSONL)
```jsonl
{"input": "user: message", "output": "Freya: response"}
```

### Cross-Device Features
- Download dataset as JSONL
- Upload to other devices
- Merge with existing data
- Maintain format consistency

## Browser Support
- Modern browsers (Chrome, Firefox, Safari, Edge)
- Mobile browsers
- PWA-ready structure
- Offline capability

## Performance Optimizations
- Debounced search
- Efficient DOM updates
- Lazy stat calculations
- Memory management
- Mobile-optimized

## Mobile Considerations
- Touch-friendly interface
- Responsive layout
- Efficient data handling
- Cross-device sync
- Storage limits

## Security & Data
- Client-side only
- No server dependencies
- Data backup support
- Format validation
