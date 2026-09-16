# Made It Home — Bug Reports

## Overview

This document contains a portfolio-safe summary of bugs and issues identified during functional, regression, exploratory, usability, notification, automation, location, and cross-platform testing of the **Made It Home** mobile application.

Testing was performed across Android and iOS builds and covered core safety flows, event management, participant management, location tracking, Safe Home, notifications, sub-events, activities, pit stops, voice-based event creation, subscriptions, automation, and application stability.

> **Note:** Internal ticket IDs, team names, client information, credentials, and other confidential project details have been excluded.

---

# Bug / Issue Summary

| ID      | Module               | Issue                                                                                    | Status      | Severity |
| ------- | -------------------- | ---------------------------------------------------------------------------------------- | ----------- | -------- |
| BUG-001 | Creator Upgrade      | Close (X) button on Upgrade to Creator screen was not functioning                        | Fixed       | Medium   |
| BUG-002 | Performance          | Application pages loaded slowly and navigation was delayed                               | Fixed       | Medium   |
| BUG-003 | Location             | Incorrect user location was detected/displayed on map                                    | Fixed       | High     |
| BUG-004 | Location             | Location name did not update after moving map pin                                        | Fixed       | Medium   |
| BUG-005 | Onboarding           | Back button on "What's Your Name?" screen was not working                                | Fixed       | Medium   |
| BUG-006 | Permissions          | Location request displayed "Location Request Timed Out" during onboarding                | Fixed       | High     |
| BUG-007 | Safe Home            | Participants were not notified when a member marked themselves safe                      | Fixed       | High     |
| BUG-008 | One-Tap Events       | Ended One-Tap event remained visible on dashboard                                        | Not a Bug   | Low      |
| BUG-009 | Safe Home            | "Mark as Safe" remained available after user was already marked safe                     | Fixed       | Medium   |
| BUG-010 | Events               | Event image was not displayed on scheduled event card                                    | Fixed       | Medium   |
| BUG-011 | One-Tap Events       | Different One-Tap events displayed the same icon                                         | Fixed       | Low      |
| BUG-012 | Notifications        | Safe Home notification was received only by creator                                      | Not Fixed   | High     |
| BUG-013 | Subscription         | Subscription screen displayed Monthly regardless of selected plan                        | Not Fixed   | Medium   |
| BUG-014 | UI/UX                | Several screens were inconsistent with approved design                                   | Not Fixed   | Medium   |
| BUG-015 | Invitations          | Deleted event invitation remained actionable                                             | Not Fixed   | High     |
| BUG-016 | Permissions          | Native permission modal could cause application crash                                    | Fixed       | High     |
| BUG-017 | Event Creation       | Application could crash while adding contacts                                            | Fixed       | High     |
| BUG-018 | Voice Event Creation | Voice flow re-requested contacts already provided                                        | Fixed       | Medium   |
| BUG-019 | Voice Event Creation | Incorrect destination could be selected                                                  | Fixed       | High     |
| BUG-020 | Voice Event Creation | Some mentioned contacts were not recognized                                              | Fixed       | High     |
| BUG-021 | Voice Event Creation | Duplicate/contact selection behavior was inconsistent                                    | Fixed       | Medium   |
| BUG-022 | Voice Event Creation | Incorrect AM/PM could be assigned around midnight                                        | Fixed       | High     |
| BUG-023 | Voice UI             | Voice response text overlapped UI icon                                                   | Fixed       | Low      |
| BUG-024 | Invitations          | Invited contacts did not consistently receive notifications                              | Fixed       | High     |
| BUG-025 | Trusted People       | Accepted trusted-person request did not always trigger notification                      | Fixed       | Medium   |
| BUG-026 | Monitoring           | Monitoring bottom sheet appeared before expected contact-selection step                  | Fixed       | Medium   |
| BUG-027 | Event Editing        | Editing event could clear configured time values                                         | Fixed       | High     |
| BUG-028 | Event Editing        | Event displayed "Scheduled for no time" after editing                                    | Fixed       | High     |
| BUG-029 | Event Details        | Active event title was hidden behind Edit control                                        | Fixed       | Low      |
| BUG-030 | Navigation           | Back navigation from sub-event editing could create a loop                               | Fixed       | Medium   |
| BUG-031 | Sub-events           | Sub-event invitation could arrive before main event invitation was accepted              | Fixed       | High     |
| BUG-032 | Sub-events           | User could remain in sub-event after declining main event                                | Fixed       | High     |
| BUG-033 | Sub-events           | Sub-event remained Scheduled after start time                                            | Fixed       | High     |
| BUG-034 | Sub-events           | Ended sub-event continued displaying In Progress                                         | Fixed       | High     |
| BUG-035 | Sub-events           | Removed main-event participant could still be added to sub-event                         | Fixed       | High     |
| BUG-036 | Sub-events           | Sub-event invitation could be automatically accepted                                     | Fixed       | High     |
| BUG-037 | Sub-events           | All contacts were displayed instead of eligible main-event participants                  | Fixed       | Medium   |
| BUG-038 | Sub-events           | Main event and sub-event notifications had identical labels                              | Fixed       | Low      |
| BUG-039 | Sub-events           | Sub-event notifications were not received                                                | Not Fixed   | High     |
| BUG-040 | Sub-events           | Inactive sub-event displayed incorrect ending information                                | Fixed       | Medium   |
| BUG-041 | Sub-events           | Midnight event caused incorrect sub-event end-time restriction                           | Fixed       | High     |
| BUG-042 | Activities           | Activity destination pin opened hidden/stuck details card                                | Fixed       | High     |
| BUG-043 | Activities           | Activity ending notification was not received at expected time                           | Not Fixed   | High     |
| BUG-044 | Activities           | User was not automatically redirected to main event after activity ended                 | Improvement | Medium   |
| BUG-045 | Location             | Background/killed-state location behavior was inconsistent                               | In Progress | High     |
| BUG-046 | Safe Zone            | User was not automatically marked safe until app was opened                              | In Progress | High     |
| BUG-047 | Automation           | Event state changes sometimes required manual refresh                                    | In Progress | High     |
| BUG-048 | Automation           | Safety status was not always updated automatically in background                         | In Progress | High     |
| BUG-049 | Notifications        | Notification behavior was inconsistent across event actions                              | In Progress | High     |
| BUG-050 | Session              | Session timeout could be followed by immediate automatic login                           | Fixed       | Medium   |
| BUG-051 | Performance          | Application could remain on loading state for an extended period                         | In Progress | High     |
| BUG-052 | Stability            | Application randomly crashed on iOS/Android                                              | In Progress | Critical |
| BUG-053 | Stability            | Panic/Mark Safe/Logout actions could become stuck                                        | Fixed       | High     |
| BUG-054 | Invitations          | Declined invitation state did not always update correctly                                | Fixed       | High     |
| BUG-055 | Activities           | Activity invitation remained accessible after main-event participation changed           | Fixed       | High     |
| BUG-056 | Activity Details     | Activity details card could become stuck after opening                                   | Fixed       | High     |
| BUG-057 | Event Creation       | Saved contacts and manual number-entry options behaved inconsistently                    | Fixed       | Medium   |
| BUG-058 | Event Creation       | Contact selection flow could become inconsistent with multiple contacts                  | Fixed       | Medium   |
| BUG-059 | Event Creation       | Voice flow did not always retain previously provided information                         | Fixed       | Medium   |
| BUG-060 | Voice Event Creation | Voice flow could ask for information that had already been captured                      | Fixed       | Medium   |
| BUG-061 | Voice Event Creation | Event details could be created with incorrect location information                       | Fixed       | High     |
| BUG-062 | Voice Event Creation | Multiple contacts were not consistently added to event                                   | Fixed       | High     |
| BUG-063 | Voice Event Creation | Invitation/contact flow was inconsistent between manual and voice creation               | Fixed       | Medium   |
| BUG-064 | Event Creation       | Event creation flow could become stuck during contact processing                         | Fixed       | High     |
| BUG-065 | Trusted People       | Trusted contact acceptance flow did not consistently trigger expected state/notification | Fixed       | Medium   |
| BUG-066 | Safe Circle          | Safe Circle participant state was not consistently reflected immediately                 | Fixed       | Medium   |
| BUG-067 | Monitoring           | Monitoring/watcher information was not always displayed at the expected stage            | Fixed       | Medium   |
| BUG-068 | Participants         | Participant information was displayed inconsistently between event screens               | Fixed       | Low      |
| BUG-069 | Participants         | Participant avatar/name presentation differed between main event and sub-event           | Improvement | Low      |
| BUG-070 | Invitations          | Invitation state was not always synchronized with event participation                    | Fixed       | High     |
| BUG-071 | Invitations          | User could interact with invitation after related event state changed                    | Fixed       | High     |
| BUG-072 | Main Event           | Active event state was not always refreshed automatically                                | In Progress | High     |
| BUG-073 | Main Event           | Event completion state could require application interaction to update                   | In Progress | High     |
| BUG-074 | Main Event           | Event review/state information could remain stale                                        | In Progress | Medium   |
| BUG-075 | Safe Home            | Safe Home state did not always update immediately                                        | In Progress | High     |
| BUG-076 | Safe Home            | User could require app opening before safety status was reflected                        | In Progress | High     |
| BUG-077 | Location             | Location updates were inconsistent during background/killed-state testing                | In Progress | High     |
| BUG-078 | Location             | Location tracking and related safety automation were not fully synchronized              | In Progress | High     |
| BUG-079 | Location             | Location-dependent event state did not always update automatically                       | In Progress | High     |
| BUG-080 | Notifications        | Push notification timing was inconsistent for some event actions                         | In Progress | Medium   |
| BUG-081 | Notifications        | Notification content/labels were inconsistent between main and sub-events                | Fixed       | Low      |
| BUG-082 | Notifications        | Some expected notifications appeared only after manually navigating back                 | Not Fixed   | High     |
| BUG-083 | Activities           | Activity state did not always transition automatically at configured time                | Fixed       | High     |
| BUG-084 | Activities           | Activity completion flow depended on manual user interaction                             | Improvement | Medium   |
| BUG-085 | Activities           | Activity screen did not automatically return to parent event                             | Improvement | Medium   |
| BUG-086 | Activities           | Activity destination details did not always open correctly                               | Fixed       | High     |
| BUG-087 | Activities           | Activity details UI could be partially hidden                                            | Fixed       | High     |
| BUG-088 | Sub-events           | Sub-event state did not automatically update at exact scheduled time                     | Fixed       | High     |
| BUG-089 | Sub-events           | Sub-event timing behavior differed when event crossed midnight                           | Fixed       | High     |
| BUG-090 | Sub-events           | Invalid participants could remain available for sub-event selection                      | Fixed       | High     |
| BUG-091 | Sub-events           | Sub-event participant list was not restricted correctly                                  | Fixed       | Medium   |
| BUG-092 | Sub-events           | Sub-event invitation flow did not always respect main-event state                        | Fixed       | High     |
| BUG-093 | Sub-events           | Sub-event acceptance/decline states could become inconsistent                            | Fixed       | High     |
| BUG-094 | Sub-events           | Sub-event notification was not triggered for expected state change                       | Not Fixed   | High     |
| BUG-095 | Pit Stops            | Pit stop state/action behavior required additional validation after event changes        | Improvement | Medium   |
| BUG-096 | Pit Stops            | Pit stop flow did not always behave consistently with parent event state                 | Improvement | Medium   |
| BUG-097 | Event Timing         | Event time handling behaved inconsistently around AM/PM transition                       | Fixed       | High     |
| BUG-098 | Event Timing         | Time validation behaved differently for midnight-ending events                           | Fixed       | High     |
| BUG-099 | Event Timing         | Valid sub-event time could be rejected when main event crossed midnight                  | Fixed       | High     |
| BUG-100 | Event Editing        | Existing event information could be lost after saving edits                              | Fixed       | High     |
| BUG-101 | Event Editing        | Event schedule could become invalid after editing                                        | Fixed       | High     |
| BUG-102 | Event Deletion       | Deleted event state was not immediately reflected across invitation flow                 | Not Fixed   | High     |
| BUG-103 | Event Deletion       | Related invitation remained accessible after event deletion                              | Not Fixed   | High     |
| BUG-104 | Dashboard            | Event information could remain stale until refresh/navigation                            | In Progress | Medium   |
| BUG-105 | Dashboard            | Event status did not always update automatically                                         | In Progress | High     |
| BUG-106 | UI/UX                | Some event information was hidden by overlapping UI elements                             | Fixed       | Medium   |
| BUG-107 | UI/UX                | Event/action labels were inconsistent across related screens                             | Fixed       | Low      |
| BUG-108 | UI/UX                | Certain screens did not match expected design/layout                                     | Not Fixed   | Medium   |
| BUG-109 | UI/UX                | Some controls were difficult to identify or access due to placement                      | Improvement | Low      |
| BUG-110 | Navigation           | Back navigation could return user to an unexpected screen                                | Fixed       | Medium   |
| BUG-111 | Navigation           | Sub-event navigation could leave the user in an incorrect flow state                     | Fixed       | High     |
| BUG-112 | Navigation           | Returning from activity flow required manual navigation                                  | Improvement | Medium   |
| BUG-113 | Performance          | Some screens experienced noticeable loading delays                                       | In Progress | Medium   |
| BUG-114 | Performance          | Loader could remain visible while content was not immediately available                  | In Progress | High     |
| BUG-115 | Stability            | Random crashes occurred during general application usage                                 | In Progress | Critical |
| BUG-116 | Stability            | Application could become unresponsive during certain actions                             | Fixed       | High     |
| BUG-117 | Stability            | Certain safety actions could remain in loading state                                     | Fixed       | High     |
| BUG-118 | Cross Platform       | Some flows behaved differently between iOS and Android                                   | Improvement | Medium   |
| BUG-119 | Cross Platform       | Notification behavior differed between supported platforms                               | In Progress | High     |
| BUG-120 | Cross Platform       | Background behavior required platform-specific validation                                | In Progress | High     |
| BUG-121 | Permissions          | Permission-related flows could fail or become stuck                                      | Fixed       | High     |
| BUG-122 | Permissions          | Location-dependent features behaved differently based on permission state                | Fixed       | High     |
| BUG-123 | Event Creation       | Manual and voice event creation did not always produce consistent results                | Fixed       | Medium   |
| BUG-124 | Voice                | Voice flow could require repeated user input                                             | Fixed       | Medium   |
| BUG-125 | Voice                | Voice-created event details could differ from user-provided information                  | Fixed       | High     |
| BUG-126 | Voice                | Voice contact recognition was unreliable with multiple participants                      | Fixed       | High     |
| BUG-127 | Voice                | Voice time interpretation could be incorrect around date/time boundaries                 | Fixed       | High     |
| BUG-128 | Notifications        | Notification could be delayed until user performed another action                        | Not Fixed   | High     |
| BUG-129 | Notifications        | Notification was triggered only after manually returning to parent screen                | Not Fixed   | High     |
| BUG-130 | Automation           | Automatic transitions were not consistently triggered without app interaction            | In Progress | High     |
| BUG-131 | Automation           | Background automation required additional manual verification                            | In Progress | High     |
| BUG-132 | Automation           | Event completion automation was dependent on participant/app state                       | In Progress | High     |
| BUG-133 | Safe Zone            | Safe-zone detection did not always trigger expected safety action automatically          | In Progress | High     |
| BUG-134 | Safe Zone            | Safe-zone-related state required application interaction to become visible               | In Progress | High     |
| BUG-135 | Safe Home            | Automatic safe-home transition was not consistently reflected                            | In Progress | High     |
| BUG-136 | Main Event           | Event could remain active until application state was refreshed                          | In Progress | High     |
| BUG-137 | Main Event           | Parent event state was not always synchronized with sub-event state                      | In Progress | High     |
| BUG-138 | Activities           | Activity completion did not always synchronize immediately with main event               | Improvement | High     |
| BUG-139 | Activities           | Ending an activity did not automatically trigger expected parent-event navigation        | Improvement | Medium   |
| BUG-140 | Sub-events           | Participant eligibility was not always synchronized with main event                      | Fixed       | High     |

---

# Highlighted Bug Reports

The following are selected examples of defects investigated in detail during testing.

---

## BUG-003 — Incorrect Location Detected on Map

**Severity:** High
**Status:** Fixed

### Description

The application displayed an incorrect user location on the map.

### Steps

1. Open the application.
2. Navigate to the location/map screen.
3. Allow location access.
4. Compare the displayed location with the actual device location.

### Expected

The user's current location should be detected and displayed accurately.

### Actual

The application displayed an incorrect location.

---

## BUG-017 — Crash While Adding Contacts

**Severity:** High
**Status:** Fixed

### Description

The application crashed while adding contacts during event creation.

### Steps

1. Start creating an event.
2. Navigate to participant/contact selection.
3. Select one or more contacts.
4. Continue through the event creation flow.

### Expected

Contacts should be selected successfully and the event creation flow should continue.

### Actual

The application could crash during contact selection.

---

## BUG-027 — Event Timing Cleared After Editing

**Severity:** High
**Status:** Fixed

### Description

Previously configured event timing information could be cleared after editing an existing event.

### Expected

Existing Expected Home By, Arrival Time, and End Time values should remain unchanged unless explicitly modified.

### Actual

Time values could be cleared after saving the edit.

---

## BUG-033 — Sub-event Remains Scheduled After Start Time

**Severity:** High
**Status:** Fixed

### Description

A scheduled sub-event did not automatically transition to its active state after the configured start time.

### Expected

The sub-event should automatically transition from Scheduled to the appropriate active state.

### Actual

The sub-event continued displaying Scheduled after the start time had passed.

---

## BUG-034 — Ended Sub-event Remains In Progress

**Severity:** High
**Status:** Fixed

### Description

A sub-event could remain In Progress after its configured end time.

### Expected

The sub-event should automatically transition to its ended/completed state.

### Actual

The sub-event continued displaying In Progress.

---

## BUG-035 — Removed Participant Available in Sub-event

**Severity:** High
**Status:** Fixed

### Description

A participant removed from the main event could still be selected when creating/editing a sub-event.

### Expected

Only active participants of the main event should be eligible for its sub-events.

### Actual

The removed participant remained available for selection.

---

## BUG-039 — Sub-event Notifications Not Received

**Severity:** High
**Status:** Not Fixed

### Description

Expected notifications related to sub-events were not received.

### Expected

Relevant participants should receive notifications for applicable sub-event actions and state changes.

### Actual

The expected sub-event notifications were not received.

---

## BUG-041 — Incorrect Time Validation Around Midnight

**Severity:** High
**Status:** Fixed

### Description

When a main event ended at midnight, valid sub-event end times were incorrectly restricted.

### Expected

The application should allow any valid sub-event end time within the main event duration.

### Actual

The application restricted valid time selections when the main event crossed midnight.

---

## BUG-042 — Activity Details Card Hidden/Stuck

**Severity:** High
**Status:** Fixed

### Description

Opening an activity through its destination pin displayed a hidden or stuck activity details card.

### Expected

The complete activity details card should open correctly and remain usable.

### Actual

The card was partially hidden and could become stuck.

---

## BUG-043 — Activity Ending Notification Not Received

**Severity:** High
**Status:** Not Fixed

### Description

The activity ending notification was not received when the activity reached its configured end time.

### Expected

The relevant user should automatically receive the activity ending notification.

### Actual

The notification was not received at the expected time.

---

## BUG-044 — No Automatic Redirect After Activity End

**Severity:** Medium
**Status:** Improvement

### Description

After an activity ended, the user remained on the activity screen and had to manually select "Back to Main Event."

### Expected

The application should automatically redirect the user to the main event when the activity ends.

### Actual

Manual navigation was required.

---

## BUG-046 — User Not Automatically Marked Safe

**Severity:** High
**Status:** In Progress

### Description

The user could enter the safe zone while the application was running in the background/killed state, but the Safe Home status was not automatically updated.

### Expected

The user's safe status should be updated automatically when the configured location condition is satisfied.

### Actual

The application required the user to open the app before the Safe Home state was reflected.

---

## BUG-052 — Random Application Crashes

**Severity:** Critical
**Status:** In Progress

### Description

The application experienced random crashes during testing on supported iOS and Android builds.

### Expected

The application should remain stable during normal usage and supported user flows.

### Actual

The application could randomly crash during usage.

---

## BUG-053 — Safety Actions Become Stuck

**Severity:** High
**Status:** Fixed

### Description

Certain safety actions, including Panic, Mark as Safe, or Logout, could remain stuck in a loading state.

### Expected

The selected action should complete and provide appropriate feedback.

### Actual

The action could remain loading or become unresponsive.

---

# Major Testing Areas Covered

* Authentication and onboarding
* Profile and account management
* Permission handling
* Event creation
* Event editing and deletion
* Create Event Now / One-Tap events
* Trusted People
* Participant management
* Safe Circle
* Watcher/Monitor functionality
* Event invitations
* Main event lifecycle
* Mark as Safe
* Safe Home
* Panic/Emergency flow
* Safe Zones
* Location tracking
* Background location
* Killed-state behavior
* Event automation
* Sub-events
* Activities
* Activity destinations
* Pit Stops
* Voice-based event creation
* Push notifications
* Subscription flow
* Creator upgrade
* UI/UX
* Navigation
* Performance
* Stability
* iOS testing
* Android testing
* Cross-platform behavior
* Regression testing
* Exploratory testing

---

# QA Coverage Summary

The defects above represent issues identified across both **functional behavior and real-world edge cases**, including:

* Time and date boundary conditions
* Midnight and AM/PM transitions
* Background and killed application states
* Location-dependent automation
* Multiple participants
* Invitation state changes
* Parent/child event relationships
* Notification timing
* State synchronization
* Manual vs. automated transitions
* Cross-platform differences
* Application stability and performance

This portfolio demonstrates experience beyond basic UI validation, including **workflow testing, state-transition testing, negative testing, edge-case testing, notification validation, location-based testing, background processing, and exploratory testing**.
