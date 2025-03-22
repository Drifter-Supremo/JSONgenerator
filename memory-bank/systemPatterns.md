# System Patterns: Freya Dataset Builder

## Architecture Overview

```mermaid
flowchart TD
    UI[UI Components] --> DS[DataStore]
    DS --> LS[(localStorage)]
    UI --> Stats[Stats Panel]
    UI --> Search[Search]
    
    subgraph UI Components
        Input[Input Fields]
        Counter[Counter Display]
        Actions[Action Buttons]
        Upload[Backup/Restore]
    end
    
    subgraph DataStore
        State[State Management]
        Export[JSONL Utils]
        Backup[Sync Utils]
    end
```

## Implementation Patterns

### Single File Architecture
- All code in index.html
- Inline CSS and JavaScript
- No external dependencies
- GitHub Pages compatible

### Event-Driven Updates
- Dataset changes trigger UI updates
- Real-time search filtering
- Stats panel updates
- Counter synchronization

### Data Management
- localStorage persistence
- JSONL format for portability
- Backup/restore for sync
- Atomic operations

## Component Structure

### UI Components
```mermaid
flowchart TD
    Form[Input Form] --> Save[Save Example]
    Save --> Counter[Example Counter]
    Counter --> Stats[Stats Panel]
    Stats --> Basic[Basic Stats]
    Stats --> Words[Word Analysis]
    Stats --> Flow[Flow Stats]
    Counter --> Actions[Actions]
    Actions --> Download[Download JSONL]
    Actions --> Upload[Upload Backup]
    Actions --> Clear[Clear All]
    Actions --> Search[Search]
```

### Data Flow
```mermaid
flowchart LR
    Input[User Input] --> Format[Format Data]
    Format --> Validate[Validation]
    Validate --> Store[localStorage]
    Store --> Update[Update UI]
    Store --> Stats[Update Stats]
    Store --> Export[Export JSONL]
```

## Deployment Strategy

### GitHub Pages
- Main branch deployment
- No build process needed
- Instant updates
- Cross-device access

### Cross-Device Sync
- Download JSONL backup
- Upload to other devices
- Merge datasets
- Maintain consistency

## Error Handling
- Input validation
- Format verification
- Storage limits
- Export reliability
- Upload validation

## State Management
- localStorage as source of truth
- Real-time UI updates
- Search state management
- Stats panel state

## Mobile Support
- Responsive design
- Touch-friendly controls
- Efficient data handling
- Cross-device sync
