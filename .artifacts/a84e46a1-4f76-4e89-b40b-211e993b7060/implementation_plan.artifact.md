# Implementation Plan - Display Note Timestamps

This plan outlines the addition of creation and last updated timestamps to the note list and editor.

## Proposed Changes

### [Component] UI Utilities

#### [MODIFY] Utility Function
I will use a simple formatting function to convert the `Long` timestamps from the database into readable strings (e.g., "23 Jul 2026, 02:56").

### [Component] UI Layer (Screens)

#### [MODIFY] [DashboardScreen.kt](file:///D:/Semester 6/Pemrograman Mobile/Dams/10-MyNote/app/src/main/java/com/adamtri/mynoteapp/ui/screens/DashboardScreen.kt)
- Update `NoteItem` to display the `updatedAt` timestamp at the bottom of the card.
- Format the timestamp for better readability.

#### [MODIFY] [EditorScreen.kt](file:///D:/Semester 6/Pemrograman Mobile/Dams/10-MyNote/app/src/main/java/com/adamtri/mynoteapp/ui/screens/EditorScreen.kt)
- Display both "Created" and "Last Updated" timestamps at the bottom of the editor content.
- Ensure the text color adapts to the chosen note background color.

## Verification Plan

### Automated Tests
- Run `./gradlew :app:assembleDebug` to verify compilation.

### Manual Verification
1. Open the app and check the Dashboard.
2. Verify that each note card now shows a timestamp (e.g., "Last updated: ...").
3. Open a note for editing.
4. Verify that both the creation date and the last update date are visible at the bottom.
5. Edit the note, save it, and verify the "Last Updated" timestamp updates correctly on both screens.
