# Scope Session — critical iPhone tests

Status: **READY FOR EXPLORATORY TESTING — NOT RUN. Final candidate verification is still in progress.**

Sections 1–8 can be explored on the development app already installed on Kal
iPhone 14 Pro. Its verified installed bundle is `ai.ashraya.scopesession`, version
**1.0**, built from `78aecdc8a5a08c4d0538b03a755d2e970058a0ce`. The installed
build-number readback is unknown; do not substitute the local build number.
Largest-text clipping/contrast issues are still under investigation. Record any
failure rather than treating it as expected success.

Final acceptance must repeat the checks on the designated internal TestFlight
build supplied by Codex. Section 9 is blocked until that delivery; section 10's
links wait for published app pages. An unchecked or blocked item is not a pass.

## Before starting

- Device: Kal iPhone 14 Pro. iOS version: __________
- Run type: DEVELOPMENT EXPLORATION / INTERNAL TESTFLIGHT ACCEPTANCE
- App version/build: __________ (development version 1.0; installed build unknown)
- Source commit: __________ (development source above; TestFlight source pending)
- Test date: __________
- Use fictional sessions, notes and non-sensitive test photos. Preserve a complete
  backup of any existing records before deletion, replacement or reinstall.
- The exact totals below require an empty test library. If this installation
  already holds records, first save and verify a complete backup you intend to
  keep, then deliberately clear the library using Settings → Delete All App Data.
  If you prefer to preserve the current library in place, mark the exact-total
  and deletion/replacement sections BLOCKED and tell Codex; do not mix fixtures
  with existing M31 records and report those totals as passing.
- Run free-capacity checks before the Sandbox purchase. Purchase tests must use
  the prepared Sandbox/TestFlight environment; never make a real paid purchase.
- Record PASS, FAIL or BLOCKED for every section. For a failure, include the step,
  expected/actual result and a screenshot without personal content.

## 1. Offline logging and persistence

- [ ] Enable airplane mode and turn Wi-Fi off. Cold-launch Scope Session; Log
  opens without an account, a forced paywall or a network requirement.
- [ ] With no setup selected, choose M31, enter **180 seconds × 42 frames** and
  filter **L**. Expected logged integration time: **2h 6m 0s**.
- [ ] Save, close the app from the app switcher, then reopen. History contains
  exactly one matching session with the same date, values and total.
- [ ] Start an unsaved custom target **TEST Panel A**, enter **30 × 5** and a note.
  Visit History and Settings, background/lock the phone, then reopen the app.
  The unsaved input is still present; it has not become a saved duplicate.

Result / issue: __________

## 2. Multiple rows, dates and target totals

- [ ] Save a second M31 session on a different observing date with rows
  **60 × 10, Ha** and **120 × 5, OIII**. Its total is **20m 0s**.
  First finish saving the fictional Panel A draft from section 1 so it is preserved.
- [ ] History → Group by target → M31 shows **2h 26m 0s** across both sessions:
  L **2h 6m**, Ha **10m**, OIII **10m**. Notes/search do not silently change the
  all-night target total.
- [ ] Edit the second session to **Ha 60 × 5**; its total becomes **15m 0s** and
  M31 becomes **2h 21m 0s**. Relaunch and check again.
- [ ] Save a separate **TEST Panel B** custom target with **30 × 5**. Grouping
  shows both it and the saved **TEST Panel A** as separate targets. Also save a
  long custom target with Unicode notes and check that the text is preserved.
- [ ] If practical, change the phone's time zone, reopen History and confirm the
  chosen observing dates did not move. Restore your original time-zone setting.

Result / issue: __________

## 3. Invalid inputs, editing and setup snapshots

- [ ] Try saving without a target, then with a second exposure row missing its
  frame count. Each is rejected with a useful message; all input remains and the
  affected field is reachable. Correct it and save once; no duplicate appears.
- [ ] In Settings, create **Test refractor** with a telescope and camera. Use it
  for one saved session. Edit the preset, then delete only that test preset.
  The saved session's original equipment snapshot remains unchanged.
- [ ] Leave a new unsaved draft, edit an existing session from History, and try
  leaving the edit. Check **Keep Editing** and **Discard Changes** separately.
  Discarding an edit does not lose the parked new draft or alter the saved record.

Result / issue: __________

## 4. Real Photos picker

- [ ] Attach a non-sensitive portrait JPEG or HEIC, save and reopen its session.
  Preview orientation and proportions are correct. Repeat with a landscape photo.
- [ ] Open the picker to replace an attachment, then cancel. The old image and
  draft stay intact. If an iCloud-only image is available, try selecting it offline;
  a download failure must preserve the old attachment and every entered field.
- [ ] Remove an attached copy from a test session. Its original still exists in
  Photos. No camera, location or library-wide access prompt is required by the app.

Codex separately verifies exported attachment metadata; do not infer metadata
removal from appearance alone.

Result / issue: __________

## 5. CSV and PDF in real apps

- [ ] Add this note to a test session, preserving the newline:

  ```text
  Test, "quoted" — 星
  Second line
  ```

- [ ] Export all sessions as CSV to Files. Open it in Numbers or another CSV
  reader: each session stays one record, notes retain quotes/newlines/Unicode,
  and every exposure row/filter and total is present.
- [ ] Export a target PDF and an all-session PDF. Open both in Files/Preview.
  Check scope, dates, totals, all exposure rows, notes, photo proportions and the
  final page. Add long notes to exercise multiple pages; no text is cut off.
- [ ] Cancel a share sheet and return to logging. No saved data or draft is lost.

Result / issue: __________

## 6. Complete backup and recovery — test data only

- [ ] Create and retain a new preset **Backup test setup** with telescope
  **Backup telescope**. Turn **Prefer PDF reports** on (the nondefault setting).
  These must be present in the backup and restored after deletion.
- [ ] Settings → **Create Complete Backup** explains that the file is plaintext.
  Save the completed `.scopesessionbackup` to Files. Note session/preset counts,
  photo-bearing records and **Prefer PDF reports** setting before continuing.
- [ ] **Restore Backup from Files** → select that backup. Verify the counts and
  full-replacement warning, then **Cancel**. The current library remains intact.
- [ ] Only after confirming the backup exists, use **Delete All App Data** on the
  fictional library. Records, photos inside the app, presets, draft and preferences
  clear. Files exports/backups and Photos originals remain.
- [ ] Restore the backup and confirm replacement. Compare counts, exact notes,
  observing dates, row values, totals, photos, presets and report preference.
  Specifically verify **Backup test setup / Backup telescope** reappears and
  **Prefer PDF reports** is on again.
  Close/reopen the app and compare again.
- [ ] Select an unrelated small text file as a backup. It is rejected clearly;
  the restored valid library remains unchanged.

Result / issue: __________

## 7. Ten-session free boundary

- [ ] Before purchasing, build up to **10 current saved sessions**. Try saving an
  eleventh with a note/photo. The dismissible upgrade screen appears; **Close**
  preserves the entire draft.
- [ ] At the limit, read/edit an existing session, export and create a backup.
  These actions stay free. Delete one fictional session and save the preserved
  draft: the freed slot works without buying anything.
- [ ] Offline or with Apple's price unavailable, no guessed price or false
  purchase success appears; the draft and existing records stay available.

Result / issue: __________

## 8. VoiceOver, largest text and low-light usability

- [ ] In iPhone Accessibility settings, enable Larger Accessibility Sizes at the
  largest size and Reduce Motion. Traverse Log, expanded equipment/details,
  History, target detail, Settings, preset editor, upgrade and backup prompts.
  Scroll to every action; text, fields and buttons remain usable above the tab bar
  and keyboard. Pay particular attention to exposure fields and Save.
- [ ] Enable VoiceOver. Enter/save a session, correct an error, dismiss a sheet
  and navigate back. Labels identify target, exposure seconds, frame count,
  filters and actions; reading order and focus make sense.
- [ ] With the phone in both system Light and Dark appearance, Scope Session
  stays dark and legible. At your normal nighttime brightness, read secondary
  labels and identify controls without relying on color alone.
- [ ] Restore your preferred accessibility/appearance settings afterward.

Result / issue: __________

## 9. Sandbox purchase and restore — after delivery is ready

**BLOCKED until Codex verifies the real product and supplies the exact internal
TestFlight candidate.** Local StoreKit simulator tests are separate evidence.

- [ ] Online, open **Unlock Unlimited Logging**. Apple's localized price and
  one-time purchase are clear. Cancel the purchase sheet; nothing is charged,
  no access is falsely granted, and the draft remains.
- [ ] Complete the prepared Sandbox purchase. More than ten sessions can now
  be saved. The waiting draft is not silently saved twice. Relaunch offline;
  previously verified access and all data remain available.
- [ ] Tap **Restore Purchases** and verify access. For reinstall testing, first
  make and verify a complete test-data backup; reinstall only the named candidate,
  restore purchases, then restore the library from Files. Purchase restoration
  must not imply that Apple restores the app's records automatically.
- [ ] With Codex's prepared Sandbox controls, exercise pending purchase and
  refund/revocation. Pending does not unlock; revocation only restricts new saves
  at the free limit. Existing records, edits, exports and backups remain available.
  If those controls are unavailable, mark this item BLOCKED, not PASS.

Result / issue: __________

## 10. Public links and acceptance

- [ ] After the app pages are published, **Privacy Policy** and **Terms** open
  the correct Scope Session pages without errors. **Support** opens a message to
  `support@madebykal.com` with only `Scope Session` in the subject and no private
  content or automatic attachments. Cancel the message; no test email is needed.
- [ ] Optional usability observation: time one returning entry with a saved
  setup. Record seconds here: ____. The 15-second target is a hypothesis.

Overall: **NOT RUN / PASS / FAIL / BLOCKED**

Blocking issues: __________

Founder acceptance of the exact internal TestFlight version/build above: __________
(Leave blank for a development exploration run.)

Acceptance does not authorize App Review submission or public release.
