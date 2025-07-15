Test case : Validate Viber chat functionality without internet connection (iPhone 13, v25.5.2)

Test Case ID: TC\_VIBER\_001

Platform: iPhone 13

App Version: Viber 25.5.2

Module: Chat / Messaging

Test Type: Negative / Offline functionality

Priority: Medium

Test Data: Message content: "Offline test message"

Description:

This test case verifies how the Viber mobile application behaves when the user opens the app without an internet connection. It focuses on the visibility of unsynced chat content (messages and images) and the availability of message actions like delete or forward. It also validates whether undelivered messages allow the “Delete for everyone” option while offline.

Preconditions:

The user is logged in to the Viber app on iPhone 13.

The internet connection is completely turned off.

The chat in question has not been recently synced (some messages and images were not previously opened while online).

| Step | Action | Expected Result | Actual Result |
| --- | --- | --- | --- |
| 1 | Launch the Viber app while offline | Viber opens, but unsynced chat content does not appear. | Viber opens and all previous messages and images are still visible, even without internet |
| 2 | Open a chat conversation that was not recently active | Chat opens but no messages or images should be displayed if not cached | Chat opens and messages and images are displayed, |
| 3 | Type a new message in the input field | Message appears in the input field | Message appears as expected |
| 4 | Tap the “Send” button | Message stay in "Sending..." state and not be delivered | Message remains in "Sending..." state as expected |
| 5 | Tap and hold on the unsent message | 'Delete for everyone' appears when the message remains undelivered. | Only "Delete for me" option is available |
| 6 | Tap “Delete for me” | Message is removed from user's view | Message is deleted only for the sender |
| 7 | Try to interact with the "Sending..." message | Options delete and forward are available for the message | Message is not clickable,no interaction possible |

TEST CASE2-Validate Registration Form Handles Existing Email Correctly (Happy Path)

Test Case ID:TC\_IG\_002

Title:Validate registration form handles existing email correctly – Happy Path

*   Module-User Registration

Platform Instagram PWA Web

Test Type-Positive / Happy Path (with invalid input)

Priority :High

Description:

This test case verifies that the registration form correctly detects and blocks email addresses that are already in use during account creation. A relevant error message must be displayed, and the registration process must not proceed. This ensures proper validation and user feedback.

Preconditions

1.  Email ahhahaajaja@gmail.com is already associated with an Instagram account.
2.  \- The Instagram registration page is open.
3.  \- Stable internet connection is available.
4.  \- No browser or app errors occur.

Test Data:

\- Email: ahhahaajaja@gmail.com

\- Username: dekidekic2025

\- Password: Test12345!

\- Full Name: FDFFGDH

\- Date of Birth: 22.07.2001

| Step No. | Action | Expected Result | Actual Result |
| --- | --- | --- | --- |
| 1 | Navigate to the Instagram registration page | Registration page loads successfully | Page loaded successfully |
| 2 | Enter email: ahhahaajaja@gmail.com | System check if email is already in use and displays error | Error message shown |
| 3 | Enter username: dekidekic2025 | Accept username | Username accepted |
| 4 | Enter password: Test12345! | Password is accepted | Password accepted |
| 5 | Enter full name: FDFFGDH | Name accepted | Name accepted |
| 6 | Enter date of birth: 22.07.2001 | Age validated and accepted | Date accepted |
| 7 | Click on "Sign Up" or equivalent registration button | Registration is blocked with appropriate message: "Email already in use" | Registration blocked |

BUG REPORT : Files and links missing in Messenger chat – iOS

Summary:

Recently sent files and links are not displayed in the Messenger chat under the "Files and Links" tab until the user exits and re-enters the conversation multiple times.

Description:

When opening a Messenger chat on iPhone, the "Files and Links" section appears empty, even though files or links have recently been exchanged in the conversation. After re-entering the chat several times, the files and links are eventually displayed. This delays access to shared content and may confuse users.

Environment:

Mobile – iPhone 13

iOS version: 18.5

Messenger app version: 512.0.0

Preconditions:

User is in a conversation where files and/or links were recently shared.

Steps to reproduce:

Open Messenger on an iPhone.

Enter a conversation where files or links have been recently sent.

Tap on the "Files and Links" section.

Observe that the section is empty.

Exit the conversation.

Re-enter the conversation multiple times.

Files and links eventually appear.

Expected result:

Files and links should appear immediately after they are sent, without requiring the user to refresh the chat manually.

Actual result:

Files and links are not visible at first and appear only after repeated re-entry into the chat.

Severity: Medium

Priority: Low

BUG REPORT-Messages are not received until the app is opened – iOS

*   Summary:

Push notifications for new messages are not delivered unless the user manually opens the Messenger app.

*   Description:

The user does not receive real-time notifications for new incoming messages. Messages are only received and shown when the user opens the Messenger application. This can result in missed or delayed communication and affects the app's core functionality.

*   Environment:

Mobile – iPhone 13

iOS version: 18.5

Messenger app version: 512.0.0

*   Preconditions:

User is logged in to the Messenger app and the device has a stable internet connection. Background app refresh and notifications are enabled in iOS settings.

*   Steps to reproduce:

1.  Make sure Messenger is not currently open (run it in the background or close it).
2.  Send a message to the user from another account/device.
3.  Observe that no push notification is received.
4.  Open the Messenger app.
5.  Message appears only after the app is opened.

*   Expected result:

User should receive a real-time push notification for a new message, even when the app is closed or running in the background.

*   Actual result:

No notification or message is received until the app is manually opened.

Severity: High

Priority: Medium