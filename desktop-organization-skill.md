# Desktop Organization Skill

> **Two parts:** Part 1 provides best practices for users. Part 2 defines the sequential workflow for the AI agent to execute.

---

# PART 1: Best Practices Guide (For Users)

## The Philosophy
Your desktop should be a **temporary workspace**, not permanent storage. Think of it like a physical desk - you wouldn't pile everything you own on it.

## Core Principles

### 1. The Minimal Desktop Approach
**What to keep:**
- Currently active projects (1-3 folders max)
- Frequently used shortcuts (5-10 max)
- Files you're actively working on this week

**What to remove:**
- Completed projects → Move to Documents
- Old files → Archive or delete
- Rarely used shortcuts → Use Start Menu/Search instead

### 2. Folder Structure Strategy

```
Desktop/
├── 📁 Active Projects/
│   ├── Current-Project-1/
│   └── Current-Project-2/
├── 📁 Quick Access/
│   └── (shortcuts only)
└── 📄 (2-3 active files max)
```

### 3. The "Three Folder" System

**Option A: By Status**
- `🔴 Urgent` - Things needing immediate attention
- `🟡 This Week` - Current work
- `🟢 Reference` - Quick-access resources

**Option B: By Type**
- `💼 Work` - Professional projects
- `🎨 Personal` - Personal projects
- `📚 Learning` - Courses, tutorials, resources

**Option C: By Time**
- `2026-01-Current` - This month's work
- `Archive` - Completed items
- `Resources` - Permanent reference materials

## Practical Implementation Guide

### Immediate Actions:

1. **Create a Projects folder** in Documents:
   ```
   Documents/
   ├── Dev-Projects/
   │   ├── active-project-1/
   │   ├── active-project-2/
   │   └── archived-projects/
   ├── Personal/
   │   ├── finances/
   │   ├── education/
   │   └── photos/
   └── Resources/
       └── installers/
   ```

2. **Desktop should only have:**
   - One "Active" folder with current project
   - 5-6 essential shortcuts (your most-used apps)
   - Maybe 1-2 files you're editing today

3. **Move these off desktop:**
   - Project folders → `Documents/Dev-Projects/`
   - Backup folders → `Documents/Dev-Projects/archived/`
   - Personal documents → `Documents/Personal/`
   - PDFs and images → Appropriate folders
   - Installers → `Downloads/` or delete after use

### File Naming Conventions

**Good:**
- `2026-01-29_project-name_description.ext`
- `client-name_document-type_v2.ext`
- `YYYY-MM-DD_meaningful-name.ext`

**Avoid:**
- `新建文件夹 (2).txt`
- `final_FINAL_v3_ACTUAL_FINAL.docx`
- `image.jpg`, `image2k.jpg` (not descriptive)

## The Weekly Cleanup Ritual

**Every Friday (5 minutes):**
1. Move completed work to Documents
2. Delete unnecessary files
3. Update project folders
4. Clear Downloads folder
5. Desktop should be nearly empty

## Advanced Tips

### Use Windows Features:
- **Quick Access** in File Explorer - Pin frequently used folders
- **Start Menu** - Pin apps instead of desktop shortcuts
- **Windows Search** (Win + S) - Find files without desktop clutter
- **Virtual Desktops** (Win + Tab) - Separate work contexts

### The "Inbox" Approach:
```
Desktop/
└── 📥 Inbox/
    └── (Everything lands here first)
```
- All downloads, screenshots, new files go here
- Process daily: file properly or delete
- Goal: Empty inbox by end of day

### Cloud Integration:
- OneDrive/Dropbox for Documents
- GitHub for code projects
- Desktop stays clean and synced

## Example Structure

Here's a practical example of an organized system:

```
Desktop/
├── 🔗 App-Shortcut-1.lnk
├── 🔗 App-Shortcut-2.lnk
├── 🔗 App-Shortcut-3.lnk
└── 📁 Current/ (optional - for this week's files only)

Documents/
├── Dev-Projects/
│   ├── project-name/
│   ├── project-backup/
│   └── archived/
├── Personal/
│   ├── finances/
│   ├── education/
│   └── photos/
├── Work/
│   └── presentations/
└── Resources/
    └── tools/
```

## The Reality Check

**Most organized people:**
- Have 0-5 items on desktop
- Use desktop as temporary staging area only
- Rely on File Explorer Quick Access
- Use search instead of visual browsing
- Clean desktop weekly (or daily)

**The key insight:** 
Your desktop is prime real estate. Only put there what you need to see every single day. Everything else should be one search away in a logical folder structure.

## Quick Win: The 10-Minute Transform

1. Create `Documents/Dev-Projects/` and `Documents/Personal/`
2. Move active project folders to Dev-Projects
3. Move personal document folders to Personal
4. Delete obvious temp files (installers, duplicates)
5. Keep only 3-5 shortcuts on desktop
6. Enjoy the clean space

Remember: **A clean desktop = a clear mind**. You'll find things faster with good folders than with visual scanning of 50+ desktop items.


---

# PART 2: Agent Workflow (For Automation)

## Overview
This section defines the sequential, interactive workflow for the AI agent to organize desktop files with user guidance at each step.

## Workflow Sequence

**IMPORTANT FLOW CONTROL:**
- Steps marked "Wait for response" = STOP and wait for user input
- Steps marked "Auto-proceed" = Continue immediately to next step
- Only ask questions when explicitly instructed

### Step 1: Workspace Confirmation ⏸️ WAIT FOR RESPONSE
**Agent Action:**
```
Confirm current working directory and show root path.
Present: "I'm about to organize files in: [ABSOLUTE_PATH]"
```

**Ask User:**
```
"Is this the correct desktop folder to organize?"
Options: 
- 1. Yes, proceed
- 2. No, I need to change workspace
- 3. Show me all files first
```

**Wait for response before proceeding. Not not start a spec sessions**

---

### Step 2: Structure Analysis & Categorization ▶️ AUTO-PROCEED
**Agent Action:**
Analyze all files and folders, categorize them:

**Categories:**
- **Projects**: Folders with package.json, .git, or development markers
- **Documents**: .pdf, .docx, .odt, .txt, .md files
- **Media**: .jpg, .png, .mp4, video/image files
- **Shortcuts**: .lnk files (applications)
- **Archives**: backup folders, .zip files
- **Utilities**: Standalone executables, tool folders
- **Personal/Financial**: Folders with sensitive documents
- **Uncategorized**: Everything else

**Present to User:**
```
"Here's what I found on your desktop:

📂 Projects ([X] folders):
   - [List project folders with brief description]
   - Example: "my-app/ (React project, 300+ files)"

📄 Documents ([X] files):
   - PDFs: [count and types]
   - Office docs: [count and types]
   - Text files: [count]

🖼️ Media ([X] files):
   - Images: [count]
   - Videos: [count]
   - Audio: [count]

🔗 Shortcuts ([X] .lnk files):
   - Productivity: [list apps like IDEs, browsers]
   - Communication: [list apps like Zoom, Slack]
   - Games: [list game shortcuts]
   - Other: [list remaining shortcuts]

📁 Other Folders ([X] folders):
   - [List with brief descriptions]

Total: [X] files and [Y] folders"
```

**DO NOT wait for user response. Immediately proceed to Step 3.**

---

### Step 3: Application Priority Selection ⏸️ WAIT FOR RESPONSE
**Agent Action:**
List all application shortcuts found.

**Ask User:**
```
"Which application shortcuts should STAY on your desktop?
(These should be your most frequently used apps - recommend 3-5 max)

Found shortcuts:
[Categorized list of shortcuts]

📱 Productivity Apps:
1. [IDE/Code Editor]
2. [Browser]
3. [File Manager]

💬 Communication:
4. [Video conferencing]
5. [Chat/Messaging]

🎮 Games:
6. [Game 1]
7. [Game 2]

🛠️ Utilities:
8. [Other tools]

Options:
- List numbers (e.g., "1, 2, 4")
- List categories (e.g., "Productivity, Communication")
- "all" - keep all files on desktop
- "none" - move all to organized folders
- "top3" - keep your top 3 most used (you tell me which)
- "no-games" - keep all except games
- "icon sort" - get manual guidance for desktop icon arrangement only

📋 ABOUT THE "ICON SORT" OPTION:
If you choose "icon sort", I will:
• Skip creating new folders (Projects, Personal, Work, etc.)
• Skip moving any files or folders
• Skip organizing shortcuts into Apps/ folders
• ONLY provide desktop icon arrangement guidance to:
  - Analyze all current desktop items
  - Suggest grouping shortcuts and folders by type
  - Recommend arrangement: shortcuts first, then folders
  - Provide manual positioning instructions for a clean, compact layout
  - Guide you through Windows auto-arrange settings

⚠️ IMPORTANT: I cannot automatically move desktop icons due to Windows API limitations. I will provide detailed manual instructions for optimal icon positioning.
```

**Wait for response before proceeding.**

**If user selects "icon sort":**
- Skip Steps 4 and 5 entirely
- Jump directly to Step 6 (Desktop Icon Sort)
- Present message: "Skipping file organization - proceeding directly to desktop icon sorting..."

---

### Step 4: Organization Strategy Proposal ⏸️ WAIT FOR RESPONSE
**Agent Action:**
Based on analysis and user's app preferences, generate a detailed organization plan.

**Reference:** Use folder structures from Part 1 (Three Folder System options) as templates.

**Present Plan:**
```
"Here's my proposed organization strategy:

📁 FOLDERS TO CREATE:
Documents/
├── Dev-Projects/
│   ├── Active/
│   │   └── [active-project]/ (moved from desktop)
│   └── Archive/
│       └── [old-project]/ (moved from desktop)
├── Personal/
│   ├── Finances/
│   │   └── [financial-docs]/ (moved from desktop)
│   ├── Education/
│   │   └── [educational PDFs, etc.]
│   └── Media/
│       ├── [media-folder]/ (moved from desktop)
│       └── [video-folder]/ (moved from desktop)
└── Resources/
    └── Utilities/
        └── [utility-folder]/ (moved from desktop)

Desktop/ (AFTER organization):
├── [Your selected shortcuts - e.g., IDE, Browser, Communication]
├── Apps/
│   ├── Productivity/ (moved unselected work apps)
│   ├── Communication/ (moved unselected chat/video apps)
│   ├── Games/ (moved game shortcuts)
│   └── Utilities/ (moved utility shortcuts)
└── .kiro/ (stays - configuration folder)

📦 FILES TO MOVE:
→ Documents/Personal/Education/:
   - [Educational PDFs]
   - [Thesis documents]
   - [Course materials]
   - [Presentation files]

→ Documents/Personal/Media/:
   - [Image files]
   - [Wallpapers]
   - [Screenshots]

→ Desktop/Apps/Productivity/:
   - [IDE shortcuts not selected]
   - [Office app shortcuts]

→ Desktop/Apps/Communication/:
   - [Video conferencing apps not selected]
   - [Chat apps not selected]

→ Desktop/Apps/Games/:
   - [Game launcher shortcuts]
   - [Individual game shortcuts]

→ Desktop/Apps/Utilities/:
   - [System tools]
   - [Utility shortcuts]

→ Documents/Resources/Utilities/:
   - [Standalone executables]
   - [Installer folders]

🗑️ POTENTIAL CLEANUP (will ask before deleting):
   - System files (desktop.ini)
   - Duplicate files
   - Broken shortcuts

📌 STAYING ON DESKTOP:
   - [Your selected app shortcuts]
   - .kiro/ folder (if present)
   - [Any other items you specified]

SUMMARY:
- Creating [X] new folders
- Moving ~[Y] files
- Moving [Z] project folders
- Organizing [W] shortcuts into categories
- Keeping [N] shortcuts on desktop
- Desktop will go from [A] items to [B] items
```

**Ask User:**
```
"Does this organization plan work for you?

Options:
- Yes, proceed with this plan
- Modify - I want to change something (tell me what)
- Show me alternative folder structures
- Cancel - I'll organize manually
```

**Wait for response. If "Modify", ask what to change and regenerate plan.**

---

### Step 5: Execution with Progress Updates ▶️ AUTO-PROCEED
**Agent Action:**
Execute the approved plan step-by-step.

**Safety Rules:**
- Never delete files without explicit permission
- Create all folders first
- Move files in batches by category
- Preserve file timestamps
- Handle errors gracefully (skip and report)
- Log all operations

**Progress Updates:**
```
"Starting organization...

✓ Created Documents/Dev-Projects/Active/
✓ Created Documents/Dev-Projects/Archive/
✓ Created Documents/Personal/Finances/
✓ Created Documents/Personal/Education/
✓ Created Documents/Personal/Media/
✓ Created Documents/Resources/Utilities/
✓ Created Desktop/Apps/Productivity/
✓ Created Desktop/Apps/Communication/
✓ Created Desktop/Apps/Games/
✓ Created Desktop/Apps/Utilities/

Moving projects...
✓ Moved [project-folder]/ → Documents/Dev-Projects/Active/
✓ Moved [backup-folder]/ → Documents/Dev-Projects/Archive/

Moving documents...
✓ Moved [X] PDF/Office files → Documents/Personal/Education/

Moving media files...
✓ Moved [X] image files → Documents/Personal/Media/

Moving folders...
✓ Moved [personal-folder]/ → Documents/Personal/[category]/
✓ Moved [media-folder]/ → Documents/Personal/Media/
✓ Moved [utility-folder]/ → Documents/Resources/Utilities/

Organizing shortcuts...
✓ Kept [selected shortcuts] on desktop
✓ Moved [X] productivity apps → Desktop/Apps/Productivity/
✓ Moved [X] communication apps → Desktop/Apps/Communication/
✓ Moved [X] game shortcuts → Desktop/Apps/Games/
✓ Moved [X] utility shortcuts → Desktop/Apps/Utilities/

File organization complete! Proceeding to desktop sorting...
```

**🚨 CRITICAL: DO NOT STOP HERE - IMMEDIATELY CONTINUE TO STEP 6**
**The workflow is NOT complete until desktop sorting is finished!**

---

### Step 6: Desktop Icon Arrangement Guidance ▶️ AUTO-PROCEED

**Agent Action:**
Provide detailed manual guidance for desktop icon arrangement after file moves are complete.

**IMPORTANT LIMITATION:**
Due to Windows API restrictions and security limitations, I cannot automatically move desktop icons. Instead, I will provide comprehensive manual guidance for optimal desktop organization.

**MANUAL ARRANGEMENT GUIDANCE:**

```
# Analyzing desktop items for optimal arrangement...
$desktopPath = [Environment]::GetFolderPath("Desktop")
Write-Host "Analyzing desktop items for color-based organization..."

# Get all desktop items with their properties
$items = Get-ChildItem -Path $desktopPath | Select-Object Name, Extension, FullName

Write-Host "Found $($items.Count) items to organize"

# STEP 1: Analyze and categorize items
$categories = @{
    "Essential_Apps" = @()     # Your selected shortcuts to keep
    "App_Folders" = @()        # Apps/ subfolders created
    "Project_Folders" = @()    # Any remaining project folders
    "System_Items" = @()       # .kiro, system files
}

foreach ($item in $items) {
    $category = "System_Items"
    
    if ($item.Extension -eq ".lnk") {
        # Check if it's one of the user's selected essential apps
        $category = "Essential_Apps"
    }
    elseif ($item.Name -match "Apps") {
        $category = "App_Folders"
    }
    elseif ($item.Name -match "Project|Dev|Work") {
        $category = "Project_Folders"
    }
    
    $categories[$category] += $item
    Write-Host "  $($item.Name) → $category"
}

# STEP 2: Create positioning recommendations
Write-Host ""
Write-Host "=== MANUAL DESKTOP ARRANGEMENT GUIDE ==="
Write-Host "Follow these steps to organize your desktop icons:"
Write-Host ""

Write-Host "1️⃣ ENABLE AUTO-ARRANGE (Recommended):"
Write-Host "   • Right-click empty desktop space"
Write-Host "   • Select 'View' → 'Auto arrange icons'"
Write-Host "   • Select 'View' → 'Align icons to grid'"
Write-Host ""

Write-Host "2️⃣ OPTIMAL ARRANGEMENT ORDER (Top to Bottom, Left to Right):"
Write-Host ""

Write-Host "🔗 ESSENTIAL SHORTCUTS (Top row):"
foreach ($item in $categories["Essential_Apps"]) {
    Write-Host "   • $($item.Name) - Keep in top-left area for quick access"
}

Write-Host ""
Write-Host "📁 APP FOLDERS (Second area):"
foreach ($item in $categories["App_Folders"]) {
    Write-Host "   • $($item.Name) - Place below essential shortcuts"
}

Write-Host ""
Write-Host "📂 PROJECT FOLDERS (Third area):"
foreach ($item in $categories["Project_Folders"]) {
    Write-Host "   • $($item.Name) - Place in middle-right area"
}

Write-Host ""
Write-Host "⚙️ SYSTEM ITEMS (Bottom area):"
foreach ($item in $categories["System_Items"]) {
    Write-Host "   • $($item.Name) - Keep in bottom area, less frequently accessed"
}

Write-Host ""
Write-Host "3️⃣ MANUAL POSITIONING STEPS:"
Write-Host "   1. Drag essential app shortcuts to top-left corner"
Write-Host "   2. Place Apps/ folders below shortcuts"
Write-Host "   3. Position any remaining project folders to the right"
Write-Host "   4. Keep system folders (.kiro) at bottom"
Write-Host "   5. Leave some empty space for temporary files"
Write-Host ""

Write-Host "4️⃣ ALTERNATIVE: Use Windows Snap Layouts:"
Write-Host "   • Press Win + Z while hovering over desktop"
Write-Host "   • Choose a layout that groups similar items"
Write-Host ""

Write-Host "5️⃣ FINAL CLEANUP:"
Write-Host "   • Remove any broken shortcuts"
Write-Host "   • Delete empty folders"
Write-Host "   • Refresh desktop (F5) to apply changes"
Write-Host "========================================"
```

**Present Progress:**
```
"Finalizing desktop organization...

✓ File organization completed successfully
✓ Analyzing remaining desktop items for arrangement
✓ Found [X] items: [Y] essential shortcuts, [Z] app folders, [W] other items
✓ Generated optimal arrangement recommendations
✓ Provided step-by-step manual positioning guide

⚠️ IMPORTANT: Due to Windows security restrictions, I cannot automatically move desktop icons. Please follow the detailed manual arrangement guide above for optimal desktop organization.

🎯 DESKTOP ORGANIZATION GUIDANCE COMPLETE!"
```

**🚨 CRITICAL: DO NOT STOP HERE - IMMEDIATELY CONTINUE TO STEP 7**
**The workflow is NOT complete until final summary is provided!**

---

### Step 7: Final Summary & Recommendations ▶️ AUTO-PROCEED
**Agent Action:**
Provide final summary and recommendations.

**Present:**
```
"✅ Desktop Organization Complete!

📊 RESULTS:
- Folders created: [X]
- Files moved: [Y]
- Project folders moved: [Z]
- Shortcuts organized: [W]
- Desktop items: [Before] → [After] (reduced by [X]%)

📁 YOUR NEW STRUCTURE:
Desktop/
├── [Selected shortcuts - e.g., IDE, Browser, Communication app]
├── Apps/
│   ├── Productivity/ ([X] shortcuts)
│   ├── Communication/ ([X] shortcuts)
│   ├── Games/ ([X] shortcuts)
│   └── Utilities/ ([X] shortcuts)
└── .kiro/ (if present)

Documents/
├── Dev-Projects/ (your code projects)
├── Personal/ (documents, media, finances)
└── Resources/ (utilities)

💡 RECOMMENDATIONS:
1. Review Documents/Personal/Media/ - consider organizing by date or event
2. Check Desktop/Apps/Games/ - pin frequently played games to Start Menu
3. Consider archiving old project backups if no longer needed
4. Set up weekly cleanup ritual (see Part 1 of this guide)
5. Use Windows Quick Access to pin frequently used folders

⚠️ ISSUES ENCOUNTERED:
[None / List any files that couldn't be moved / Note: Desktop icon positioning requires manual arrangement due to Windows API limitations]

🎯 NEXT STEPS:
- Verify all files are in correct locations
- Follow the manual desktop icon arrangement guide provided
- Review Apps/ folders - delete shortcuts you don't need
- Consider archiving old project backups if no longer needed
- Set up weekly cleanup ritual (see Part 1 of this guide)
- Use Windows Quick Access to pin frequently used folders
- Enable Windows auto-arrange for consistent icon positioning
```

**Workflow Complete.**

---

## Technical Implementation Notes

### File Operation Commands (Windows)
```powershell
# Create directory
New-Item -ItemType Directory -Path "path"

# Move file/folder
Move-Item -Path "source" -Destination "dest"

# Check if exists
Test-Path "path"
```

### Error Handling
- Files in use: Skip and report
- Duplicate names: Append timestamp
- Permission errors: Skip and report
- Large folders (>1GB): Ask before moving

### Edge Cases
- Non-English filenames: Handle with UTF-8 encoding
- System files (.ini, hidden): Skip automatically
- Broken shortcuts: Identify and ask user
- Empty folders: Ask before creating

### Validation
After each major operation:
- Verify file exists at destination
- Verify file removed from source
- Check file size matches
- Log operation to summary

---

## Success Criteria
- ✅ User feels in control throughout process
- ✅ All questions asked sequentially with clear options
- ✅ No files lost or misplaced
- ✅ Desktop is significantly cleaner
- ✅ Frequently used items remain accessible
- ✅ User understands new folder structure
- ✅ Process is repeatable for future cleanups
