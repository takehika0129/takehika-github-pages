---
title: "Simple Android note-taking app (2025/02/13)"
description: ""
---

#### [Visit (https://github.com/takehika0129/no5-android-note-taking-app)](https://github.com/takehika0129/no5-android-note-taking-app)

# **Concept**
This is a simple note-taking app with essential functionality allowing users to quickly create, view, and delete notes without complexity. This app stores notes locally using SharedPreferences, ensuring a lightweight and offline-friendly experience.


# 📖 **How to Use This App**

1️⃣ Creating a Note
- Tap the Title field and enter the name of your note.
- Tap the Content field and type the details of your note.
- Press the “Save” button to store the note.
- Once saved, the note will appear in the Saved Notes section at the bottom.

2️⃣ Viewing Saved Notes
- All saved notes are displayed in a scrollable list at the bottom of the screen.
- Notes remain saved even after closing the app.

3️⃣ Deleting the Latest Note
- Tap “Delete Latest” to remove the most recently added note first.
- If no notes are left, the screen will display “No notes saved.”


# **Other Features**
- **📜 Scrollable Notes Section**: Allows users to view old notes smoothly.
- **🔄 Auto-Clearing Input Fields**: – After saving a note, the input fields are reset for a better user experience.


# **Challenges & Solutions**  
- **Ensuring Simplicity with Only Two Buttons**: This app needed to be intuitive with minimal controls. Instead of cluttering the UI with multiple actions, I merged functionalities into just “Save” and “Delete Latest” buttons, making note management easy and efficient.
- **No Scrolling in the Notes List**: Without scrolling, users couldn’t access old notes once multiple entries were saved. This was resolved by implementing LazyColumn, enabling smooth scrolling and ensuring all notes remain accessible.


# **Future Improvements**
- **Cloud Sync**: Integrate Firebase or Google Drive backup for cross-device access.
- **Search Functionality**: Allow users to quickly find notes by title or content.

  
---
[Back to All Prototypes](../index.md)

