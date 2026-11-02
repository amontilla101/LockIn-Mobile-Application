# What I Learned Building LockIn App

## Resources I used
| Resource | Link | What it helped with |
|---|---|---|
| Apple Developer Docs | [FamilyControls Framework](https://developer.apple.com/documentation/familycontrols) | Understanding authorization requests and parental control access tokens. |
| Apple Developer Docs | [ManagedSettingsStore](https://developer.apple.com/documentation/managedsettings) | Learning how to programmatically apply and lift application shields. |
| Combine Documentation | [Publishers & Sinks](https://developer.apple.com/documentation/combine) | Setting up reactive 1-second countdown timers for study sessions. |

## Log
### [November 2026]
- **What I didn't know:** How Apple's Screen Time and FamilyControls frameworks handle asynchronous authorization and device shielding securely without violating sandbox rules.
- **How I figured it out** Used Gemini AI as a code explainer, research partner, and debugging support to break down Apple's documentation, combined with targeted SwiftUI tutorials.
- **Where the AI got it wrong** (and how I noticed): When styling specific UI components like side scroll bars, the AI repeatedly suggested looping layout code that didn't resolve the layout bug. I noticed the visual overflow, manually fixed the layout constraints myself, and fed the working code back to refine the architecture.
- **What I built / changed:** Designed and implemented `StudySession.swift` using a Combine-backed timer publisher, integrated `ManagedSettingsStore` to automatically lift app shields when time expires, and refactored a monolithic `ContentView` into modular, reusable view components following clean OOP principles.
