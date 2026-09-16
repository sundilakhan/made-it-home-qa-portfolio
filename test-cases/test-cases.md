# Made It Home – QA Test Cases

## Overview

This document contains sanitized QA test cases covering functional, regression, exploratory, usability, notification, location, background-state, automation, and edge-case testing performed for the Made It Home mobile application.

Testing covered both **Android and iOS** builds and focused on validating application behavior across different user flows and application states.

> **Note:** This document is a sanitized QA portfolio artifact. Internal project information, credentials, Jira references, team member names, and confidential data have been excluded.

---

# 1. Authentication & Onboarding

| Test Case ID | Test Scenario                                               | Expected Result                                                           | Status |
| ------------ | ----------------------------------------------------------- | ------------------------------------------------------------------------- | ------ |
| TC-001       | Launch application for the first time                       | Application launches successfully and displays onboarding flow            | Pass   |
| TC-002       | Complete onboarding with valid information                  | User should successfully complete onboarding                              | Pass   |
| TC-003       | Enter user name during onboarding                           | Name should be accepted and saved successfully                            | Pass   |
| TC-004       | Navigate back from the "What's Your Name?" screen           | User should return to the previous onboarding screen                      | Pass   |
| TC-005       | Add profile photo from Photo Library                        | Selected photo should be displayed in the profile preview                 | Pass   |
| TC-006       | Add profile photo using Camera                              | Camera should open and captured photo should be displayed                 | Pass   |
| TC-007       | Retake selected profile photo                               | User should be able to replace the previously selected photo              | Pass   |
| TC-008       | Continue onboarding without completing required information | Application should prevent progression and display appropriate validation | Pass   |
| TC-009       | Grant location permission during onboarding                 | Location permission should be accepted and onboarding should continue     | Pass   |
| TC-010       | Deny location permission                                    | Application should handle denied permission appropriately                 | Pass   |
| TC-011       | Test location permission timeout                            | Application should handle the timeout without crashing                    | Pass   |
| TC-012       | Relaunch application after completing onboarding            | User should remain authenticated/onboarded                                | Pass   |

---

# 2. Profile & Account

| Test Case ID | Test Scenario                                 | Expected Result                                                          | Status |
| ------------ | --------------------------------------------- | ------------------------------------------------------------------------ | ------ |
| TC-013       | View user profile                             | Profile information should load correctly                                | Pass   |
| TC-014       | Update profile information                    | Updated information should be saved successfully                         | Pass   |
| TC-015       | Update profile photo                          | New profile photo should be displayed                                    | Pass   |
| TC-016       | Logout from the application                   | User should be logged out successfully                                   | Pass   |
| TC-017       | Attempt logout during slow network conditions | Application should handle the request without becoming permanently stuck | Pass   |
| TC-018       | Reopen application after logout               | Login/onboarding state should be handled correctly                       | Pass   |
| TC-019       | Test session timeout                          | User should be logged out after the configured session timeout           | Pass   |
| TC-020       | Reopen application after session timeout      | Application should require the appropriate authentication state          | Pass   |

---

# 3. Permissions

| Test Case ID | Test Scenario                                   | Expected Result                                                       | Status |
| ------------ | ----------------------------------------------- | --------------------------------------------------------------------- | ------ |
| TC-021       | Grant location permission                       | Location functionality should become available                        | Pass   |
| TC-022       | Deny location permission                        | Application should continue according to the designed permission flow | Pass   |
| TC-023       | Revoke location permission from device settings | Application should detect the updated permission state                | Pass   |
| TC-024       | Grant camera permission                         | Camera functionality should work correctly                            | Pass   |
| TC-025       | Deny camera permission                          | Application should handle denial gracefully                           | Pass   |
| TC-026       | Grant photo library permission                  | User should be able to select photos                                  | Pass   |
| TC-027       | Test permissions after application relaunch     | Application should correctly recognize current permission states      | Pass   |
| TC-028       | Test native permission modal interaction        | Application should not crash during permission handling               | Pass   |

---

# 4. Event Creation

| Test Case ID | Test Scenario                                       | Expected Result                                                      | Status |
| ------------ | --------------------------------------------------- | -------------------------------------------------------------------- | ------ |
| TC-029       | Create event with valid details                     | Event should be created successfully                                 | Pass   |
| TC-030       | Create event with destination                       | Selected destination should be displayed correctly                   | Pass   |
| TC-031       | Move destination pin to another location            | Location and displayed location name should update correctly         | Pass   |
| TC-032       | Create event with expected arrival time             | Selected time should be saved correctly                              | Pass   |
| TC-033       | Create event with end time                          | End time should be saved correctly                                   | Pass   |
| TC-034       | Add participants during event creation              | Selected participants should be added successfully                   | Pass   |
| TC-035       | Add multiple participants                           | All selected participants should be included                         | Pass   |
| TC-036       | Remove a selected participant before creating event | Removed participant should not be included                           | Pass   |
| TC-037       | Create event without required information           | Application should prevent invalid event creation                    | Pass   |
| TC-038       | Create event with valid future time                 | Event should be scheduled for the selected time                      | Pass   |
| TC-039       | Create event with different AM/PM combinations      | Correct time should be displayed and stored                          | Pass   |
| TC-040       | Create event around midnight                        | Date and time should be interpreted correctly                        | Pass   |
| TC-041       | Create event with event image                       | Selected event image should be displayed on the event card           | Pass   |
| TC-042       | Create event without event image                    | Event should be created without an image if optional                 | Pass   |
| TC-043       | Cancel event creation                               | User should exit the creation flow without creating an event         | Pass   |
| TC-044       | Create event during slow network conditions         | Application should provide appropriate loading/error handling        | Pass   |
| TC-045       | Attempt to create duplicate/identical event         | Application should handle the request according to expected behavior | Pass   |

---

# 5. Create Event Now / One-Tap Events

| Test Case ID | Test Scenario                          | Expected Result                                                           | Status |
| ------------ | -------------------------------------- | ------------------------------------------------------------------------- | ------ |
| TC-046       | Use "Create Event Now"                 | Event should be created and activated according to the designed flow      | Pass   |
| TC-047       | Create a One-Tap event                 | One-Tap event should be created successfully                              | Pass   |
| TC-048       | Create multiple One-Tap events         | Each event should display its appropriate information and icon            | Pass   |
| TC-049       | Open an active One-Tap event           | Correct event details should be displayed                                 | Pass   |
| TC-050       | Complete a One-Tap event               | Event should transition to the appropriate completed state                | Pass   |
| TC-051       | Check ended One-Tap event on dashboard | Dashboard should display the event according to expected product behavior | Pass   |
| TC-052       | Verify One-Tap event icon              | Correct icon should be displayed for the corresponding event              | Pass   |

---

# 6. Event Editing

| Test Case ID | Test Scenario                            | Expected Result                                   | Status |
| ------------ | ---------------------------------------- | ------------------------------------------------- | ------ |
| TC-053       | Edit scheduled event                     | Event should enter edit mode successfully         | Pass   |
| TC-054       | Update event destination                 | New destination should be saved correctly         | Pass   |
| TC-055       | Update event participants                | Participant changes should be reflected correctly | Pass   |
| TC-056       | Update expected arrival time             | New time should be saved correctly                | Pass   |
| TC-057       | Update event end time                    | New end time should be saved correctly            | Pass   |
| TC-058       | Update event image                       | Updated image should be displayed                 | Pass   |
| TC-059       | Cancel event editing                     | Original event details should remain unchanged    | Pass   |
| TC-060       | Save event after editing multiple fields | All valid changes should persist                  | Pass   |
| TC-061       | Verify event timing after editing        | Event should retain valid scheduling information  | Pass   |

---

# 7. Event Deletion

| Test Case ID | Test Scenario                          | Expected Result                                                            | Status |
| ------------ | -------------------------------------- | -------------------------------------------------------------------------- | ------ |
| TC-062       | Delete scheduled event                 | Event should be removed according to expected behavior                     | Pass   |
| TC-063       | Cancel deletion                        | Event should remain available                                              | Pass   |
| TC-064       | Delete event with participants         | Participants should no longer be able to take actions on the deleted event | Pass   |
| TC-065       | Check deleted event invitation         | Deleted event invitation should no longer remain actionable                | Pass   |
| TC-066       | Refresh dashboard after deleting event | Deleted event should not incorrectly reappear                              | Pass   |

---

# 8. Trusted People & Contacts

| Test Case ID | Test Scenario                                 | Expected Result                                            | Status |
| ------------ | --------------------------------------------- | ---------------------------------------------------------- | ------ |
| TC-067       | Add trusted person                            | Contact should be added successfully                       | Pass   |
| TC-068       | Add multiple trusted people                   | All selected contacts should be added                      | Pass   |
| TC-069       | Remove trusted person                         | Contact should be removed successfully                     | Pass   |
| TC-070       | Invite contact to an event                    | Selected contact should receive the appropriate invitation | Pass   |
| TC-071       | Accept event invitation                       | User should join the event according to the expected flow  | Pass   |
| TC-072       | Decline event invitation                      | User should not remain an active participant               | Pass   |
| TC-073       | Verify invitation notification                | Invited user should receive the expected notification      | Pass   |
| TC-074       | Verify invitation after event deletion        | Deleted invitation should no longer be actionable          | Pass   |
| TC-075       | Test contact selection with multiple contacts | Correct contacts should be selected without duplication    | Pass   |

---

# 9. Safe Circle & Monitoring

| Test Case ID | Test Scenario                                      | Expected Result                                                        | Status |
| ------------ | -------------------------------------------------- | ---------------------------------------------------------------------- | ------ |
| TC-076       | Add person to Safe Circle                          | Person should be added successfully                                    | Pass   |
| TC-077       | Remove person from Safe Circle                     | Person should be removed successfully                                  | Pass   |
| TC-078       | Enable monitoring/watcher functionality            | Monitoring option should work according to expected behavior           | Pass   |
| TC-079       | Select monitoring contact during event setup       | Correct contact should be selected                                     | Pass   |
| TC-080       | Verify monitoring UI sequence                      | Monitoring controls should appear at the appropriate stage of the flow | Pass   |
| TC-081       | Verify watcher receives relevant event information | Appropriate event information should be available                      | Pass   |

---

# 10. Event Invitations

| Test Case ID | Test Scenario                                         | Expected Result                                                 | Status |
| ------------ | ----------------------------------------------------- | --------------------------------------------------------------- | ------ |
| TC-082       | Receive main event invitation                         | Invitation should be received successfully                      | Pass   |
| TC-083       | Accept main event invitation                          | User should become a participant                                | Pass   |
| TC-084       | Decline main event invitation                         | User should not become a participant                            | Pass   |
| TC-085       | Accept invitation after reopening application         | Invitation state should remain correct                          | Pass   |
| TC-086       | Decline invitation after reopening application        | Invitation should remain declined                               | Pass   |
| TC-087       | Receive invitation while application is in background | Notification should be delivered appropriately                  | Pass   |
| TC-088       | Receive invitation while application is killed        | Notification should be delivered according to platform behavior | Pass   |
| TC-089       | Verify deleted event invitation                       | Deleted invitation should not remain actionable                 | Pass   |

---

# 11. Main Event & Active Event

| Test Case ID | Test Scenario                            | Expected Result                                     | Status |
| ------------ | ---------------------------------------- | --------------------------------------------------- | ------ |
| TC-090       | Open scheduled event                     | Correct scheduled event details should be displayed | Pass   |
| TC-091       | Open active event                        | Active event screen should be displayed             | Pass   |
| TC-092       | Verify active event title                | Correct event title should be visible               | Pass   |
| TC-093       | Verify active event destination          | Correct destination should be displayed             | Pass   |
| TC-094       | Verify participant list                  | Correct participants should be displayed            | Pass   |
| TC-095       | Verify event status                      | Status should reflect the actual event state        | Pass   |
| TC-096       | Refresh active event                     | Current event state should be displayed             | Pass   |
| TC-097       | Reopen active event after leaving screen | Correct event state should be retained              | Pass   |

---

# 12. Mark as Safe / Safe Home

| Test Case ID | Test Scenario                                        | Expected Result                                                               | Status |
| ------------ | ---------------------------------------------------- | ----------------------------------------------------------------------------- | ------ |
| TC-098       | Mark user as Safe                                    | User should be marked safe successfully                                       | Pass   |
| TC-099       | Mark user safe while inside expected safe zone       | Safe state should be updated correctly                                        | Pass   |
| TC-100       | Mark user safe outside expected safe zone            | Application should handle the state according to requirements                 | Pass   |
| TC-101       | Attempt to mark safe after already being marked safe | Duplicate action should not incorrectly remain available                      | Pass   |
| TC-102       | Verify Safe Home notification                        | Relevant participants should receive appropriate notification                 | Pass   |
| TC-103       | Verify Safe Home notification for event creator      | Creator should receive expected notification                                  | Pass   |
| TC-104       | Verify Safe Home notification for participants       | Eligible participants should receive expected notification                    | Pass   |
| TC-105       | Open application after reaching safe location        | Safe state should update correctly                                            | Pass   |
| TC-106       | Test automatic Safe Home behavior                    | User should be marked safe automatically when all required conditions are met | Pass   |
| TC-107       | Test Safe Home while application is in background    | Safety state should update according to supported background behavior         | Pass   |
| TC-108       | Test Safe Home while application is killed           | Safety state should update according to supported killed-state behavior       | Pass   |

---

# 13. Panic / Emergency Flow

| Test Case ID | Test Scenario                     | Expected Result                                                   | Status |
| ------------ | --------------------------------- | ----------------------------------------------------------------- | ------ |
| TC-109       | Trigger Panic during active event | Panic workflow should start successfully                          | Pass   |
| TC-110       | Verify Panic notification         | Appropriate participants should receive the relevant notification | Pass   |
| TC-111       | Trigger Panic with slow network   | Application should provide appropriate loading/error behavior     | Pass   |
| TC-112       | Trigger Panic repeatedly          | Application should prevent unintended duplicate actions           | Pass   |
| TC-113       | Return to event after Panic flow  | User should be returned to the appropriate screen                 | Pass   |

---

# 14. Safe Zone & Location

| Test Case ID | Test Scenario                                    | Expected Result                                                     | Status |
| ------------ | ------------------------------------------------ | ------------------------------------------------------------------- | ------ |
| TC-114       | Detect current user location                     | Correct location should be detected                                 | Pass   |
| TC-115       | Display current location on map                  | User location should be displayed correctly                         | Pass   |
| TC-116       | Move destination pin                             | Map location and associated information should update               | Pass   |
| TC-117       | Add safe location/zone                           | Safe zone should be created successfully                            | Pass   |
| TC-118       | Add multiple safe zones                          | User should be able to configure multiple safe zones if supported   | Pass   |
| TC-119       | Enter safe zone during active event              | Application should detect the safe-zone condition                   | Pass   |
| TC-120       | Leave safe zone                                  | Application should update location-dependent state appropriately    | Pass   |
| TC-121       | Test location while application is in background | Location should update according to supported behavior              | Pass   |
| TC-122       | Test location while application is killed        | Location should continue according to supported background behavior | Pass   |
| TC-123       | Disable device location services                 | Application should handle unavailable location appropriately        | Pass   |
| TC-124       | Test location accuracy while moving              | Location should update appropriately                                | Pass   |

---

# 15. Background & Killed-State Testing

| Test Case ID | Test Scenario                                     | Expected Result                                                | Status |
| ------------ | ------------------------------------------------- | -------------------------------------------------------------- | ------ |
| TC-125       | Perform event flow with application open          | Event state should update correctly                            | Pass   |
| TC-126       | Perform event flow with application in background | Supported event updates should continue                        | Pass   |
| TC-127       | Swipe application away and continue event         | Supported background behavior should continue                  | Pass   |
| TC-128       | Kill application and continue event               | Supported automation should continue                           | Pass   |
| TC-129       | Receive event notification while app is killed    | Notification should be received according to platform behavior | Pass   |
| TC-130       | Location tracking while app is killed             | Supported location updates should continue                     | Pass   |
| TC-131       | Safe Home automation while app is killed          | Application should process supported safety conditions         | Pass   |
| TC-132       | Reopen app after background event updates         | Latest event state should be displayed                         | Pass   |
| TC-133       | Reopen app after killed-state event updates       | Latest server/application state should be synchronized         | Pass   |

---

# 16. Event Automation & State Transitions

| Test Case ID | Test Scenario                                             | Expected Result                                                        | Status |
| ------------ | --------------------------------------------------------- | ---------------------------------------------------------------------- | ------ |
| TC-134       | Wait until scheduled event start time                     | Event should transition from Scheduled to the appropriate active state | Pass   |
| TC-135       | Wait until event end time                                 | Event should transition to the appropriate ended state                 | Pass   |
| TC-136       | Verify event status without manually refreshing           | Status should update automatically where automation is supported       | Pass   |
| TC-137       | Verify event status after manual refresh                  | Latest status should be displayed                                      | Pass   |
| TC-138       | Verify event completion when all participants reach home  | Event should complete according to business rules                      | Pass   |
| TC-139       | Verify creator behavior after all participants reach home | Creator should be able to review the completed event appropriately     | Pass   |
| TC-140       | Verify event state after reopening app                    | Latest state should be synchronized                                    | Pass   |

---

# 17. Sub-events / Activities

| Test Case ID | Test Scenario                                            | Expected Result                                                              | Status |
| ------------ | -------------------------------------------------------- | ---------------------------------------------------------------------------- | ------ |
| TC-141       | Create a sub-event within a main event                   | Sub-event should be created successfully                                     | Pass   |
| TC-142       | Create sub-event with valid participants                 | Eligible participants should be added                                        | Pass   |
| TC-143       | Edit sub-event                                           | Updated details should be saved                                              | Pass   |
| TC-144       | Delete sub-event                                         | Sub-event should be removed appropriately                                    | Pass   |
| TC-145       | Schedule sub-event within main event duration            | Sub-event should be scheduled successfully                                   | Pass   |
| TC-146       | Attempt sub-event outside main event timing              | Application should prevent invalid scheduling                                | Pass   |
| TC-147       | Schedule sub-event ending before main event ends         | Valid earlier end time should be accepted                                    | Pass   |
| TC-148       | Schedule sub-event around midnight                       | AM/PM and date handling should be correct                                    | Pass   |
| TC-149       | Start sub-event at scheduled time                        | Sub-event should transition to the appropriate active state                  | Pass   |
| TC-150       | Verify sub-event status after start time                 | Status should update correctly                                               | Pass   |
| TC-151       | Verify sub-event status after end time                   | Status should transition to ended/completed                                  | Pass   |
| TC-152       | Accept sub-event invitation after main event invitation  | User should enter sub-event according to eligibility rules                   | Pass   |
| TC-153       | Attempt to accept sub-event before main event invitation | Application should enforce the required invitation sequence                  | Pass   |
| TC-154       | Decline main event after joining a sub-event             | User should no longer remain improperly associated with the sub-event        | Pass   |
| TC-155       | Remove participant from main event                       | Participant should lose eligibility for associated sub-events where required | Pass   |
| TC-156       | Edit sub-event participant list                          | Only eligible main-event participants should be available                    | Pass   |
| TC-157       | Open sub-event from main event                           | Correct sub-event details should be displayed                                | Pass   |
| TC-158       | Navigate back from sub-event                             | User should return to the main event                                         | Pass   |
| TC-159       | Complete sub-event                                       | User should be returned to the appropriate main-event flow                   | Pass   |

---

# 18. Activity Destination & Details

| Test Case ID | Test Scenario                           | Expected Result                                      | Status |
| ------------ | --------------------------------------- | ---------------------------------------------------- | ------ |
| TC-160       | Open activity destination pin           | Activity details should open correctly               | Pass   |
| TC-161       | View complete activity details card     | Entire card should be visible and usable             | Pass   |
| TC-162       | Close activity details                  | User should return to the previous screen            | Pass   |
| TC-163       | Open activity destination from map      | Correct activity should be displayed                 | Pass   |
| TC-164       | Verify activity destination information | Destination should match configured activity details | Pass   |

---

# 19. Pit Stops

| Test Case ID | Test Scenario                       | Expected Result                                              | Status |
| ------------ | ----------------------------------- | ------------------------------------------------------------ | ------ |
| TC-165       | Add pit stop to an event            | Pit stop should be added successfully                        | Pass   |
| TC-166       | View pit stop details               | Correct pit stop information should be displayed             | Pass   |
| TC-167       | Edit pit stop                       | Updated information should be saved                          | Pass   |
| TC-168       | Remove pit stop                     | Pit stop should be removed successfully                      | Pass   |
| TC-169       | Verify pit stop timing              | Pit stop timing should remain within valid event constraints | Pass   |
| TC-170       | Verify pit stop during active event | Pit stop should appear at the appropriate stage              | Pass   |

---

# 20. Voice-Based Event Creation

| Test Case ID | Test Scenario                                            | Expected Result                                                         | Status |
| ------------ | -------------------------------------------------------- | ----------------------------------------------------------------------- | ------ |
| TC-171       | Start voice event creation                               | Voice interaction should start successfully                             | Pass   |
| TC-172       | Provide destination through voice                        | Correct destination should be identified                                | Pass   |
| TC-173       | Provide arrival time through voice                       | Correct time should be identified                                       | Pass   |
| TC-174       | Provide multiple contacts through voice                  | All mentioned eligible contacts should be identified                    | Pass   |
| TC-175       | Provide a single contact through voice                   | Correct contact should be identified                                    | Pass   |
| TC-176       | Continue voice flow after providing contacts             | Application should not unnecessarily request the same information again | Pass   |
| TC-177       | Provide destination and contacts in a single interaction | Application should correctly process the provided information           | Pass   |
| TC-178       | Use "Tonight" in voice interaction                       | Correct date and AM/PM should be interpreted                            | Pass   |
| TC-179       | Provide time around midnight                             | Correct date and time should be determined                              | Pass   |
| TC-180       | Mention three or more contacts                           | All valid mentioned contacts should be handled correctly                | Pass   |
| TC-181       | Mention a contact not available in saved contacts        | Application should provide the expected handling                        | Pass   |
| TC-182       | Review voice-generated event details                     | Generated event information should match user input                     | Pass   |
| TC-183       | Confirm voice-created event                              | Event should be created with the confirmed information                  | Pass   |
| TC-184       | Cancel voice event creation                              | Event should not be created                                             | Pass   |
| TC-185       | Verify voice response UI                                 | Text and interface elements should not overlap                          | Pass   |

---

# 21. Notifications

| Test Case ID | Test Scenario                                  | Expected Result                                                 | Status |
| ------------ | ---------------------------------------------- | --------------------------------------------------------------- | ------ |
| TC-186       | Receive main event invitation notification     | Correct notification should be received                         | Pass   |
| TC-187       | Receive sub-event invitation notification      | Correct notification should be received                         | Pass   |
| TC-188       | Receive Mark as Safe notification              | Relevant users should receive notification                      | Pass   |
| TC-189       | Receive Safe Home notification                 | Relevant users should receive notification                      | Pass   |
| TC-190       | Receive event ending notification              | Relevant users should receive event ending notification         | Pass   |
| TC-191       | Receive activity ending notification           | Relevant users should receive activity ending notification      | Pass   |
| TC-192       | Compare main event and sub-event notifications | Notification content should clearly identify the event type     | Pass   |
| TC-193       | Receive notification while app is foregrounded | Notification behavior should match expected platform behavior   | Pass   |
| TC-194       | Receive notification while app is backgrounded | Notification should be delivered correctly                      | Pass   |
| TC-195       | Receive notification while app is killed       | Notification should be delivered according to platform behavior | Pass   |
| TC-196       | Tap event notification                         | User should be taken to the relevant event                      | Pass   |
| TC-197       | Tap activity notification                      | User should be taken to the relevant activity/sub-event         | Pass   |

---

# 22. Subscription & Creator Upgrade

| Test Case ID | Test Scenario                                         | Expected Result                                                            | Status |
| ------------ | ----------------------------------------------------- | -------------------------------------------------------------------------- | ------ |
| TC-198       | Open Upgrade to Creator screen                        | Upgrade screen should load correctly                                       | Pass   |
| TC-199       | Close Upgrade to Creator screen                       | X button should close the screen                                           | Pass   |
| TC-200       | Select Monthly subscription                           | Monthly plan should be selected and displayed correctly                    | Pass   |
| TC-201       | Select Yearly subscription                            | Yearly plan should be selected and displayed correctly                     | Pass   |
| TC-202       | Switch between Monthly and Yearly plans               | Correct selected plan and pricing should be displayed                      | Pass   |
| TC-203       | Verify subscription information after switching plans | Selected plan should remain consistent throughout the flow                 | Pass   |
| TC-204       | Test subscription screen on different platforms       | Subscription information should display according to platform requirements | Pass   |

---

# 23. UI / UX & Usability

| Test Case ID | Test Scenario                                 | Expected Result                                             | Status |
| ------------ | --------------------------------------------- | ----------------------------------------------------------- | ------ |
| TC-205       | Verify screen layout against approved design  | UI should match the approved design                         | Pass   |
| TC-206       | Verify buttons and navigation controls        | Controls should be visible and functional                   | Pass   |
| TC-207       | Verify event cards                            | Event information should be displayed correctly             | Pass   |
| TC-208       | Verify event images                           | Images should display without distortion or missing content | Pass   |
| TC-209       | Verify event icons                            | Correct icons should be displayed                           | Pass   |
| TC-210       | Verify text does not overlap icons            | UI content should remain readable                           | Pass   |
| TC-211       | Verify long event titles                      | Text should remain readable without breaking the layout     | Pass   |
| TC-212       | Verify activity details card                  | Card should be fully visible and usable                     | Pass   |
| TC-213       | Verify Back navigation throughout event flows | Back action should return to the logically previous screen  | Pass   |
| TC-214       | Verify Edit screen layout                     | Event information and controls should remain accessible     | Pass   |

---

# 24. Performance & Stability

| Test Case ID | Test Scenario                                          | Expected Result                                                        | Status |
| ------------ | ------------------------------------------------------ | ---------------------------------------------------------------------- | ------ |
| TC-215       | Launch application                                     | Application should load within an acceptable time                      | Pass   |
| TC-216       | Navigate between major screens                         | Navigation should respond without excessive delay                      | Pass   |
| TC-217       | Open event details                                     | Event details should load correctly                                    | Pass   |
| TC-218       | Perform event creation under normal network conditions | Event creation should complete successfully                            | Pass   |
| TC-219       | Perform event creation under slow network conditions   | Application should display appropriate loading/error handling          | Pass   |
| TC-220       | Repeatedly navigate through event screens              | Application should remain stable                                       | Pass   |
| TC-221       | Perform repeated Mark as Safe actions                  | Application should remain stable and prevent invalid duplicate actions | Pass   |
| TC-222       | Perform repeated Panic interactions                    | Application should remain stable                                       | Pass   |
| TC-223       | Logout and relaunch application repeatedly             | Application should remain stable                                       | Pass   |
| TC-224       | Test application stability on iOS                      | Application should not randomly crash during normal flows              | Pass   |
| TC-225       | Test application stability on Android                  | Application should not randomly crash during normal flows              | Pass   |

---

# 25. Cross-Platform Testing

| Test Case ID | Test Scenario                                      | Expected Result                                       | Status |
| ------------ | -------------------------------------------------- | ----------------------------------------------------- | ------ |
| TC-226       | Execute core event flow on Android                 | Functionality should work as expected                 | Pass   |
| TC-227       | Execute core event flow on iOS                     | Functionality should work as expected                 | Pass   |
| TC-228       | Compare event creation on Android and iOS          | Core behavior should remain consistent                | Pass   |
| TC-229       | Compare notifications on Android and iOS           | Supported notification behavior should be consistent  | Pass   |
| TC-230       | Compare location behavior on Android and iOS       | Platform-specific behavior should follow requirements | Pass   |
| TC-231       | Compare navigation flows across platforms          | Navigation should remain consistent                   | Pass   |
| TC-232       | Verify UI responsiveness on different screen sizes | UI should remain usable and readable                  | Pass   |

---

# 26. Regression Testing

The following areas were included in regression testing after fixes and new builds:

* Authentication and onboarding
* Profile management
* Permissions
* Event creation
* Event editing
* Event deletion
* One-Tap events
* Event invitations
* Trusted People
* Safe Circle
* Monitoring / Watcher
* Mark as Safe
* Safe Home
* Panic
* Location tracking
* Safe zones
* Background behavior
* Killed-state behavior
* Notifications
* Sub-events
* Activities
* Pit stops
* Voice event creation
* Subscription flow
* UI navigation
* Application stability
* Cross-platform behavior

---

# 27. Exploratory Testing Areas

In addition to predefined test cases, exploratory testing was performed around:

### State-Based Testing

* Foreground
* Background
* Killed state
* Scheduled state
* Active state
* Ended state
* Declined state
* Accepted state

### Time-Based Edge Cases

* Events starting near the current time
* Events ending near midnight
* AM/PM transitions
* Sub-events ending before the main event
* Sub-events starting at their scheduled time
* State transitions after scheduled times

### User & Participant Edge Cases

* Single participant
* Multiple participants
* Multiple contacts
* Removed participants
* Declined invitations
* Main event vs. sub-event eligibility
* Repeated invitations/actions

### Network & Stability

* Slow network
* Delayed loading
* Repeated actions
* App relaunch
* Background-to-foreground transitions
* Killed-to-open transitions

---

# 28. Testing Summary

The Made It Home QA process covered:

* Functional testing
* Regression testing
* Smoke testing
* Exploratory testing
* Usability testing
* UI testing
* Cross-platform testing
* Notification testing
* Location testing
* Background and killed-state testing
* Time-based testing
* State-transition testing
* Voice interaction testing
* Subscription testing
* Participant and permission testing
* Stability and performance testing

The primary focus was not only validating individual features but also verifying how features interacted with one another across different **users, event states, time conditions, application states, and platform environments**.
