# QA Test Cases and Bug Reports

---

## Test Case 1  
**Validate Viber chat functionality in offline mode**  
**Test Case ID:** TC_VIBER_001  
**Platform:** iOS - iPhone 13  
**App Version:** Viber 25.5.2  
**Module:** Chat / Messaging  
**Test Type:** Negative / Offline functionality  
**Priority:** Medium  
**Test Data:** Message content: "Offline test message"  

### Description  
This test case verifies Viber’s behavior when launched offline. It evaluates:  
- Visibility of unsynced chat content (e.g., messages or images not previously loaded)  
- Availability of standard message actions (delete, forward)  
- Whether "Delete for everyone" is available for undelivered messages  

### Preconditions  
- The user is logged into the Viber app on iPhone 13  
- Internet connection is fully disabled (Airplane Mode or Wi-Fi/Data off)  
- At least one chat contains unsynced messages and images (not previously opened or loaded while online)  

### Steps  

| Step | Action                                    | Expected Result                                                      | Actual Result                                                     |
|-------|------------------------------------------|---------------------------------------------------------------------|------------------------------------------------------------------|
| 1     | Launch the Viber app while offline       | Viber opens, but unsynced chat content does not appear.             | Viber opens and all previous messages and images are visible, even without internet. |
| 2     | Open a chat conversation not recently active | Chat opens, but no messages or images are displayed if not cached. | Chat opens and messages and images are displayed.                |
| 3     | Type a new message in the input field    | Message appears in the input field.                                 | Message appears as expected.                                     |
| 4     | Tap the “Send” button                     | Message remains in "Sending..." state and is not delivered.          | Message remains in "Sending..." state as expected.               |
| 5     | Tap and hold on the unsent message        | "Delete for everyone" appears when the message is undelivered.       | Only "Delete for me" is available.                               |
| 6     | Tap “Delete for me”                       | Message is removed from user's view.                                | Message is deleted only for the sender.                         |
| 7     | Try to interact with the "Sending..." message | Options "Delete" and "Forward" are available for the message.        | Message is not clickable; no interaction is possible.           |

---

## Test Case 2  
**Validate registration form blocks already registered email – Negative Scenario**  
**Test Case ID:** TC_IG_002  
**Module:** User Registration  
**Platform:** Instagram PWA Web  
**Test Type:** Negative (with invalid input)  
**Priority:** High  

### Description  
This test case verifies that the registration form correctly detects and blocks email addresses already in use during account creation. A relevant error message must be displayed, and the registration process must not proceed, ensuring proper validation and user feedback.

### Preconditions  
- Email `ahhahaajaja@gmail.com` is already associated with an Instagram account  
- Instagram registration page is open  
- Stable internet connection is available  
- No browser or app errors occur  

### Test Data  
- Email: ahhahaajaja@gmail.com  
- Username: dekidekic2025  
- Password: Test12345!  
- Full Name: FDFFGDH  
- Date of Birth: 22.07.2001  

### Steps  

| Step No. | Step Description                         | Expected Result                                                        | Actual Result                                                    |
|----------|----------------------------------------|------------------------------------------------------------------------|-----------------------------------------------------------------|
| 1        | Navigate to the Instagram registration page | Registration page loads successfully                                   | Page loaded successfully                                         |
| 2        | Enter email: ahhahaajaja@gmail.com     | System checks if the email is already in use and displays an error message. Registration is disabled. | Error message appears: "Email already in use." Registration is blocked. |
| 3        | Enter username: dekidekic2025           | Username accepted                                                     | Username accepted                                               |
| 4        | Enter password: Test12345!              | Password accepted                                                     | Password accepted                                               |
| 5        | Enter full name: FDFFGDH                | Name accepted                                                       | Name accepted                                                 |
| 6        | Enter date of birth: 22.07.2001         | Age validated and accepted                                          | Date accepted                                                 |
| 7        | Click on "Sign Up" or equivalent button | Registration is blocked with appropriate message: "Email already in use" | Registration attempt is blocked. Error message displayed again. |

---

## Bug Report 1  
**Recently sent files and links not appearing in Messenger chat – iOS**  

### Summary  
Recently shared files and links are not immediately visible in the "Files and Links" tab of Messenger chats on iOS. They only appear after the user exits and reopens the chat multiple times.

### Description  
When opening an existing Messenger chat on iOS, the "Files and Links" tab initially appears empty, even though files or links have recently been exchanged in the conversation. The shared content becomes visible only after the user exits and re-enters the chat multiple times. This causes unnecessary delays in accessing shared materials and may lead users to believe the content was never sent or has been lost. Such inconsistencies reduce user trust in the reliability of the app’s media management and can negatively affect overall user experience, especially in conversations where timely access to shared files is important.

### Environment  
- Device: iPhone 13  
- iOS version: 18.5  
- Messenger app version: 512.0.0  

### Preconditions  
- The user has an active Messenger account and is logged in.  
- The conversation contains one or more files or links sent recently (within the last few minutes).  

### Steps to reproduce:  

1. Launch the Messenger app on an iPhone.  
2. Open a conversation where files or links have been recently shared.  
3. Tap the “i” icon (chat settings) in the top right corner.  
4. Select the “Files and Links” tab.  
5. Observe that the section initially appears empty, without showing the recently shared content.  
6. Exit the conversation (go back to the chat list).  
7. Re-enter the same conversation.  
8. Repeat steps 6 and 7 several times.  
9. Notice that after multiple entries, the shared files and links eventually become visible in the section.  

### Expected result  
Shared files and links should be instantly visible in the "Files and Links" tab after being sent, without needing to exit and reopen the chat.  

### Actual result  
Files and links are not visible at first and appear only after repeated re-entry into the chat.  

### Severity  
Medium  

### Priority  
Medium (relevant for usability; could affect user trust)  

---

## Bug Report 2  
**[iOS] Messages and push notifications not received until Messenger app is opened**  

### Summary  
Push notifications for new messages are not delivered unless the user manually opens the Messenger app.

### Description  
The user does not receive real-time notifications for new incoming messages. Messages are only received and shown when the user opens the Messenger application. This can result in missed or delayed communication and affects the app's core functionality.

### Environment  
- Device: iPhone 13  
- iOS version: 18.5  
- Messenger app version: 512.0.0  

### Preconditions  
- User is logged in to the Messenger app and the device has a stable internet connection.  
- Background app refresh and notifications are enabled in iOS settings.  

### Steps to reproduce  
1. Ensure Messenger app is not currently open (either closed or running in the background).  
2. Send a message to the user from another account/device.  
3. Observe that no push notification is received.  
4. Open the Messenger app.  
5. Message appears only after the app is opened.  

### Expected result  
User should receive a real-time push notification for a new message, even when the app is closed or running in the background.

### Actual result  
No notification or message is received until the app is manually opened.

### Severity  
Critical (impacts core messaging functionality)  

### Priority  
High (affects user trust and communication reliability)  

---

