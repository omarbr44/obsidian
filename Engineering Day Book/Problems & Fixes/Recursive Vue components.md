# Problem: Needed a way to render nested folders/files

**Date:** {{date}}

## Context
(Where did this happen? Project, environment, etc.)

## Problem
(Describe the issue clearly)

## Solution
Built a **recursive Vue component**  that calls itself for children

Demonstration

SidebarComponent (Main Container)
└── SidebarFilesStrucureComponent (File Structure Root)
	└── **SidebarSubFilesStrucureComponent (Recursive Component)**
		├── SidebarFolderComponent (if item.items.length > 0)
		   ├── Folder Name
		   └── **SidebarSubFilesStrucureComponent (Recursive for children)**
		└── SidebarFileComponent (if item.items.length === 0)
		   └── File Name

## Lessons Learned
(What to remember for next time)

## Tags
#problem #fix #{{project}}
