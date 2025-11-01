# Whispermate Project Setup

## Automatic Xcode Project Generation

This project uses [XcodeGen](https://github.com/yonaskolb/XcodeGen) to automatically generate the `.xcodeproj` file.

### Why?

`.xcodeproj` files are in `.gitignore` because:
- They often cause merge conflicts
- Contain machine-specific settings
- Can be easily regenerated from `project.yml`

### How to Generate the Project

```bash
# Install XcodeGen (if not already installed)
brew install xcodegen

# Generate the project
xcodegen generate

# Open in Xcode
open Whispermate.xcodeproj
```

### Running the Application

After opening in Xcode:
1. Select the "Whispermate" scheme
2. Press ⌘R to run

### Modifying Project Configuration

All project settings are in `project.yml`. After making changes, run:

```bash
xcodegen generate
```

### Troubleshooting

**Problem:** Xcode cannot find files  
**Solution:** Regenerate the project: `xcodegen generate`

**Problem:** Compilation errors  
**Solution:** Clean build: Product → Clean Build Folder (⇧⌘K)

**Problem:** XcodeGen not installed  
**Solution:** `brew install xcodegen`

