# Changelog

All notable changes to the Forge Compliance product are documented here.
Newest release first.

## v1.3.48 — 2026-09-17

### Photos & Files
- The related photos and files panel now has a clear Show/Hide control with a more obvious orange bar and chevron, making it easier to see when the panel is open or closed.
- You can now choose where related photos appear in the report workflow: under the report, under the AI proof-check, or in both places, using the picker on the photos bar.
- Choosing Both now shows one continuous full-width photo panel instead of duplicate panels, so the same photos stay available without wasting space.
- The photo panel now remembers your preference in the browser and uses the same setting in both Review & Sign and the pre-upload proof-check.
- The photos panel now keeps a minimum visible height when shown in grid mode, so it does not collapse into a thin sliver when the AI panel is tall.
- Photo tiles, photo pickers, and emailed attachments now show clearer photo labels built from the tag, equipment, and note instead of relying on the original camera filename.
- Photos now also show a second line with the worker and date, making it easier to identify the right image at a glance.
- In the email attachment list, photos now appear with a thumbnail plus the clearer label and smaller filename, so recipients can identify attachments faster.
### Review & Sign
- The PDF toolbar now floats in the viewer corner with zoom out, zoom percentage, zoom in, fit to width, and fit to page controls, giving reviewers quicker control over how the report is displayed.
- Compare and Reset signature actions are now grouped with the PDF review controls, making the review/sign workflow easier to use from the same toolbar.
- The PDF and AI panel now start aligned at the top, so the page feels cleaner and more balanced when reviewing a report.
- Findings that are dismissed now sink to the bottom in a greyed-out state, so the most important unresolved items stay front and center.
- When every finding has been handled, reviewers now see a clear completion banner, making it obvious that the report is done.
- Cleared findings now move into a collapsible bin with a Re-open action, so reviewers can review or undo decisions without losing track of what was cleared.
- Clicking a photo-related item in review now keeps the chosen photo label consistent with the new photo naming format, making attachments easier to match to findings.
### Pre-upload Proof-check
- Marked findings, answered claims, and answered corrections now sink into their own cleared-item bins, keeping the active checklist easier to scan.
- Cleared proof-check items remain editable in the bin, so reviewers can still adjust decisions after clearing them.
- When all checks are cleared, the proof-check screen now shows a clear ready-to-submit banner, making the next step obvious.
- The same photo placement options used in review now also apply in the proof-check dialog, so teams can keep photos where they are most useful.
### Performance & Reliability
- The related photos panel now expands to use the space the AI section leaves available, helping the PDF remain as tall and readable as possible.
- The report review and proof-check screens now keep photo placement and collapse state in sync more reliably, so the chosen layout stays consistent while you work.
- The new cleared-item bins help reduce clutter in both review and proof-check flows, making long reports easier to work through without losing context.

## v1.3.47 — 2026-09-17

### Mobile & Camera
- Take photo now opens Forge’s in-app camera on supported phones, giving a live preview with capture, retake and use controls instead of launching the phone’s camera app. This avoids the Android issue where the camera app could return an empty file after Chrome was killed, so photos are much more reliable on the Sign On screen, the risk photo flow, sign-on job files and the mobile job detail page.
- When the device or browser doesn’t support camera access, the photo flow falls back to the standard phone camera/file picker so users can still attach an image instead of being blocked.
### Review & Proof Check
- The Review & sign screen now uses a split-pane layout with a draggable divider between the PDF and AI panels, and the divider position is remembered for each user so the layout reopens the way they left it.
- Double-clicking the divider resets the review layout back to its default balance, making it easy to recover from an awkward panel size.
- The PDF viewer area now keeps a proper bounded scroll region in both single-document and compare mode, so later pages remain reachable and stamp placement works reliably again.
- The signature reset control now floats in the top-right corner of the PDF pane with hover help, so reviewers can quickly move a misplaced signature back into position without hunting through the page.
- The Related photos & files strip on the review screen is now collapsible and remembers its state, giving more room to the PDF when needed.
- Compare mode now includes a Sync scroll toggle, turned on by default, so both PDFs stay aligned page-for-page while reviewing changes.
- The review header now keeps the status, filename and Upload revised version action together on one line, making the document state and upload action easier to scan at a glance.
### AI Review Panel
- The AI panel has been streamlined so the reviewer sees a clearer scoreboard row with issues, contradicted, unsupported and verified counts, helping them understand the overall review status faster.
- Run options are now tucked behind a settings button, reducing clutter and leaving more room for the findings list and document preview.
- AI findings are now shown in a more compact format that clamps each item to two lines, with a more · suggested fix link when a finding needs expansion.
- Flagged claims are now shown first in the AI panel, so the items that need action are easier to find and work through.
- Verified claims are now hidden behind a N verified chip, which keeps the list focused on unresolved items while still making the checked claims available when needed.
- The pre-check dialog uses the same streamlined review layout, with verified claims tucked behind the verified chip and a reviewed count that reflects only findings, corrections and flagged claims.
### Photos & Files
- You can now select multiple photos in the gallery by dragging a marquee across thumbnails, which makes bulk selection much faster than clicking each item one by one.
- The gallery marquee selection supports Ctrl/Cmd additive selection, so users can build up a selection in multiple passes without losing what they already picked.
- Shift-click range selection is now supported in the gallery for faster selection across a run of photos.
- Selected photo cards now show an orange highlight ring, making it obvious which items are included in the current selection.
- While dragging to select, the gallery suppresses the bulk action bar to avoid layout jumping, so the selection experience stays smooth and predictable.
- A helper hint has been added above the gallery grid to make the new selection behavior easier to discover.
### Templates & Settings
- The document template token panel is now wider and lets tokens wrap instead of truncating, so long field names and example expressions are easier to read and copy when building templates.
### Performance & Reliability
- Review and proof-check scrolling is now stable again after the layout change, so the PDF pane no longer loses its scroll container in normal mode.
- Stamp placement and dragging were verified in both single and side-by-side review modes, improving confidence that later-page signatures and annotations remain usable.
- The camera flow avoids relying on the Android OS camera handoff that could produce a zero-byte file, which improves reliability for photo capture on affected devices.

## v1.3.46 — 2026-09-17

### Proof-check
- The proof-check dialog now uses a wider two-pane layout, so uploaders can review the PDF and the AI checks side by side before submitting for approval.
- The left side of the proof-check screen now shows the uploaded PDF with zoom controls, making it easier to inspect the report while you work through the findings.
- The proof-check screen now includes the related job and equipment photos in a shared strip beside the document, helping you confirm evidence without leaving the page.
- The right side of the proof-check screen now shows AI findings, claim checks, and suggested corrections together, so uploaders can review everything in one place.
- Non-PDF uploads now show a clear note in the proof-check screen telling you to open the file separately.
### Review & Sign
- Review & sign now includes a Compare versions button when earlier PDF versions exist, letting approvers switch between a previous version and the current one.
- When comparing versions in Review & sign, the document pane splits into Previous and Current so changes are easier to check before signing.
- The signature placement area now re-fits properly when switching versions, so signing stays accurate even as the document view changes.
### AI Review Coverage
- The proof-check screen now lets uploaders mark every AI item, not just the claim-by-claim statements, so the review can be completed more consistently.
- Findings now have thumbs up/down marking for relevant or not relevant, helping uploaders confirm whether each AI result applies.
- Suggested corrections now have thumbs up/down marking for will apply or not needed, making it easier to confirm whether the AI edits should be used.
- Claim statements still support agree/disagree marking, so all AI review items can now be handled in the same flow.
- The proof-check footer now shows progress as “n of N AI items reviewed,” so uploaders can immediately see how much is left to do.
- Review & sign now shows an uploader review banner with the number of marked items and the agree/disagree split, so approvers can tell at a glance whether the proof-check was completed.
- The review banner now turns red when nothing was marked, helping approvers spot an incomplete uploader review before approving.
- When the AI check is rerun automatically, Review & sign now shows that the uploader was not marked manually, so approvers can distinguish an auto-check from a completed upload review.
- Reviewers can now see an uploader badge beside each finding, making it easier to tell which AI items were covered by the uploader.
- Review & sign now includes a collapsible Suggested corrections section, so approvers can review AI edits that were previously missing from the screen.
### Performance & Reliability
- The PDF page renderer has been rebuilt for the proof-check and review flows, improving consistency between the upload and approval screens.
- Signature placement now survives switching between previous and current versions, reducing the chance of losing work while comparing report history.

## v1.3.45 — 2026-09-17

### Report Reviews
- On the job’s report card, revised reports now show a clearer revision history line with the revision number, who revised it, when it was revised, whether it is awaiting review, who last rejected it, and who originally created it.
- On the report card, users now see live AI review status tags such as “AI re-check running” and how many earlier issues have been rectified.
- When a revised PDF report is uploaded from the job’s report flow, the app now automatically re-runs the AI check if AI is enabled and no earlier pre-check was attached, so reviewers do not have to start that again manually.
- In Review & sign, revised uploads now include a “Previous issues” section that shows each earlier issue and whether it was rectified, still present, or unclear, making it easier to see what changed since the last rejection.
- Re-uploading a revised report now clears stale AI findings and check status so the new revision is reviewed cleanly.
### Approvals & Sign-off
- In Approvals and on mobile Actions, service reports now only appear for people who actually have the “Can approve & sign” permission, which removes the phantom approve option that would previously be rejected by the backend.
- The action for reports is now clearly labeled “Review & sign” and opens the report’s signing dialog directly, instead of sending users to an approval path that could not be completed.
- Self-approval is still allowed where your account permissions permit it.
### Photos & Files
- On sign-on and mobile job screens, photo and file picking is now split into separate camera and gallery choices, so Android users can choose the direct camera path or browse files without getting stuck in the wrong picker.
- On mobile job pages, camera capture and gallery upload are now shown as separate actions for a smoother upload flow.
- Gallery uploads now accept multiple files at once and send them through in sequence, making it easier to add several job files in one go.
- Files attached from the public sign-on flow are now treated as field-uploaded files, which means they can be managed later instead of being locked away as office-only uploads.
- From Job Detail and Equipment Detail, files can now be deleted even if they came from the field, so managers are no longer blocked by the file source.
- The file gallery now supports bulk selection, including a Select all control and a Delete N action, so large cleanup jobs are much faster.
- Bulk file deletion is now available from both job files and equipment files, letting users remove multiple files in one action instead of deleting them one by one.
### Template Tokens & Doc Templates
- Doc templates now support equipment-based tokens, so templates can pull equipment type, OEM, model, serial, rating, site, location, client, notes, and custom specification fields directly from the equipment record.
- Template tokens can now use custom spec labels and keys, which makes it easier to reference site-specific equipment fields without hardcoding them.
- Equipment tokens now merge the register record with the job’s equipment item, giving templates access to the most complete equipment data available.
- Template fields can now include simple arithmetic, so users can build calculated values directly inside a token when generating documents.
- Unresolved calculation or token values are left in place instead of being blanked out, making it easier to spot missing data before a document is used.
- The Settings > Doc Templates area now includes a grouped token catalog with copy-to-clipboard support, helping admins find and insert the right token faster.
### Mobile & Sign-on
- The sign-on page now offers a direct camera option for photo capture, alongside a separate gallery option, instead of forcing Android users into the wrong file chooser.
- On mobile job detail screens, users now have clearer Camera, Gallery, and Files actions for attachments.
- The mobile actions area now follows the same report review and sign flow, reducing confusion between viewing and signing.
### My Training
- If the My Training page fails to load, users now see a visible red error message with the status code and a Retry button instead of the page quietly hiding the problem.
- The training page now handles job and company gap lookup failures more safely, so one bad record no longer hides the rest of the training list.
### Backup Health & Cluster
- Backup health now uses a stable server identity instead of the Docker container hostname, so the same server no longer appears as multiple fake rows after upgrades.
- Ghost backup rows now collapse into the real server row automatically, keeping the latest successful backup while removing stale duplicates and old trackers.
- In the Servers/cluster backup health view, each row now shows a friendly label and clearly marks the current server, making it easier to spot the active node.
- On standalone installs, the current server is now correctly recognized in backup health instead of being treated like a missing node.
### Landing & Links
- The Welcome page now includes a GitHub link in the top navigation, giving users a quick way to find the project releases.
- The Welcome page footer now also includes a GitHub Releases link next to the portal link, so release notes are easier to find from the landing page.
### Performance & Reliability
- Static assets are now cached more aggressively in the web layer, which helps pages load faster for repeat visits.
- The app shell, service worker, and manifest are now served without caching so users get the latest version reliably after a deployment.
- File uploads are now streamed more efficiently through the web server, improving upload behavior for larger files.
- The server proxy now avoids unnecessary request buffering, which helps reduce upload delays and memory pressure.
- The backend image now starts with a single Uvicorn worker by default, preventing duplicate background loops from running on the same server.
- A redundant backend curl dependency was removed from the image build, reducing container overhead.
- In the app’s backend code, unused imports and placeholder-style string issues were cleaned up, reducing noise and helping keep the codebase healthier.
### Admin & Settings
- The Edit Personnel dialog is now wider and lays out fields more cleanly on larger screens, making it easier to edit staff details.
- Certification rows in the personnel editor now stack properly on smaller phones, improving usability on mobile devices.
### Security
- The web server now hides version details from responses, reducing unnecessary exposure of server information.
- Cloudflare Access sign-out behavior is now better understood for admins: signing out ends the Access session, while Microsoft sign-in on managed Windows devices may still re-authenticate automatically because of device SSO.

## v1.3.44 — 2026-09-16

### Sign-on
- The sign-on page now uses a compact sticky mobile header and safer top/bottom spacing, so the logo stays clear of the iPhone status bar and the footer no longer sits under the home indicator.
- On the Sign-on screen, if Android Chrome reloads the page after opening the camera, your sign-on progress is now restored automatically instead of being lost.
- Sign-on now shows a “Welcome back” message when it restores a saved in-progress session, so users know they can carry on where they left off.
- The risk-photo picker on Sign-on now lets Android users choose either Camera or Gallery, instead of forcing camera capture only.
- Sign-on photos are now reduced in the browser before upload, which helps large camera images upload more reliably on mobile and weaker connections.
- Upload errors on Sign-on are now shown as clear, specific messages, so users can tell whether the problem was an empty camera file, a file that was too large, an expired session, a timeout, no connection, or a server-side issue.
### Photos & Files
- Photo and file uploads across the app now compress large images before sending them, helping reduce failed uploads and making uploads faster on mobile.
- The upload tray now shows clearer progress and failure reasons, so users can see what happened without guessing.
### Mobile
- Mobile upload handling is more resilient on Android, especially when the camera app interrupts the browser and returns to the app.
- The app now handles common Android camera-return failures better by keeping upload state and surfacing the real error instead of silently losing the file.
### Performance & Reliability
- Large camera images are now resized client-side before upload, which lowers memory usage and improves reliability on devices with limited resources.
- Upload failures now produce more useful diagnostics for support and troubleshooting, including the file size and the type of failure.
- The app now warns more clearly when uploads fail, making intermittent network issues and server rejections easier to spot and recover from.
### Security
- Sign-on progress is stored only for the current job session and is cleared when signing out or restarting the sign-on flow.

## v1.3.43 — 2026-09-14

### My Actions
- The desktop sidebar now shows **My Actions** instead of **My Training**, giving office users one place to see everything that needs their attention.
- The **My Actions** page now groups items into **For you** and **Your team**, so it’s easier to find what you personally need to finish versus what you need to review for others.
- On the **My Actions** page, you can now see rejected service reports you uploaded, tickets and licences needing approval or about to expire, onboarding items, job-required compliance gaps, company insurance gaps, and policies and training still to complete.
- Managers and approvers now get a clearer **Your team** view on the **My Actions** page, with approvals grouped by type, approved-but-unsent reports, and team tickets that are expiring or already expired.
- Count chips on the **My Actions** page now show how many items are open in each area, with an overall **N open / All clear** summary at the top.
- Completed training is now tucked into a collapsible section on **My Actions**, so the page stays focused on unfinished work.
- Links from grouped approvals now take you to the **Approvals** page and jump straight to the matching section, making review faster.
- Team ticket items now link into **Users** with the right person highlighted, so managers can act on them more quickly.
- The old **My Training** route now redirects to **My Actions**, so existing bookmarks and links still work.
### Service Reports
- When reviewing a report, you can now see whether the uploader agreed or disagreed with each AI finding, helping reviewers understand the uploader’s perspective before making a decision.
- The **Review & sign** screen now includes an uploader summary line showing how many AI claims were agreed with versus disputed.
- Report history now shows manual send changes more clearly, including reports that were **marked sent manually** or **marked not sent**, with the note, recipients, and send details preserved in the timeline.
- Manual send and not-sent entries are now shown in chronological order alongside real email sends in the **History** drawer, so the full report trail is easier to follow.
### Mobile
- On the mobile job page, users can now upload a service report directly from the job, instead of needing to switch back to desktop.
- PDF report uploads on mobile now run the same AI proof-check flow as desktop, so mobile users can review findings before submitting.
- While the proof-check is running on mobile, the job page shows a banner and lets the uploader close the dialog and get notified when the review is ready.
- Mobile uploaders can now reopen a pending proof-check from a notification link and continue from the job page.
- After the AI proof-check finishes on mobile, users can tick agree/disagree against each finding, then submit the report, submit without waiting, or cancel the upload if they need to fix the file first.
- Revised-version report uploads on mobile now also use the proof-check flow, keeping the experience consistent for resubmissions.
- Non-PDF uploads on mobile continue to submit directly, so simpler file types still move through quickly.
### Photos & Files
- Uploading a report now includes a safer pre-submission check that gives users time to review AI findings before the report is sent.
- If a report upload is cancelled during the proof-check, the uploaded file is now discarded so unfinished uploads do not linger.
### Notifications
- Users now receive an in-app and push notification when a background report proof-check is ready, making it easier to return and finish the upload.
- Notification links now open the correct report check on mobile, so the action takes users straight back to where they left off.
### Approvals
- Approval items are now grouped by type on the **My Actions** page, making it easier to jump into the right kind of review.
- Clicking an approval group now takes approvers to the **Approvals** page with that group highlighted and scrolled into view.
### Performance & Reliability
- Report AI proof-checks now run in the background instead of holding the browser open, which avoids long waits and reduces timeout failures during large or slow LLM checks.
- Users can now close the proof-check dialog while the AI runs and come back later, instead of being forced to wait on the same screen.
- If a report is submitted before the proof-check finishes, the result is now attached later when it becomes available, so users do not lose work.
- Re-running a proof-check on the same uploaded file now supersedes the previous check, keeping the latest review attached.
- The report proof-check flow now exposes clearer error details, including a log reference when something goes wrong, which should make support easier.
### Security
- The report proof-check now stores uploader agreement and disagreement marks with the report, so review decisions keep a fuller audit trail of what was checked and how the uploader responded.

## v1.3.42 — 2026-09-14

### Service Reports
- On a job’s approved report card, you can now manually **Mark as sent** for reports emailed outside Forge or sent before the job was tracked here, so the report no longer stays stuck in “approved, not sent.”
- From the same report card, you can also **Mark not sent** when a send failed; the report moves back to the “approved, not sent” queue in Actions so it can be handled again.
- When marking a report as sent, you can add the real send date, choose recipients, and leave a note so the report history reflects what actually happened.
- The report status now shows a **MANUAL** indicator when sent outside Forge, along with who made the change, when it happened, and any note for a clearer audit trail.
- Manual sent/not sent changes are now written into the report’s send log and audit history, so support and admins can see how the report was handled later.
### Admin & Settings
- In **Settings › Job Status**, admins can now control who is allowed to manually mark service reports sent or not sent, making the feature available to office managers or other roles when needed.
- The new report-sent override setting is visible to the app so the job page only shows the manual action buttons to people who are allowed to use them.
### Performance & Reliability
- Attempting to mark a report as already sent or already not sent now returns a clear validation error, helping prevent duplicate status changes and keeping report status data consistent.
- Marking a report not sent now requires a note, which improves traceability and reduces accidental status reversals.

## v1.3.41 — 2026-09-11

### Jobs
- Deleting a job now starts an approval request instead of removing it right away, so the job stays usable while it waits for a decision on the Job page.
- A red “Deletion awaiting approval” banner now appears on the Job page when deletion is pending, with options to withdraw the request, keep the job, or approve and delete it if you’re an approver.
- The trash action is disabled while a deletion request is pending, so users can see at a glance that the job is already under review.
- The Jobs list now shows a “deletion pending” badge, making pending removals visible from the list view.
- Approvers now get a Job Deletions item in Approvals on desktop and in mobile Actions, with the job linked from the approval card.
- Requesters can no longer approve their own job deletion request, and contractor managers can no longer see or decide job deletions.
- When a deletion request is approved, the job is deleted as before, including calendar cancellations, webhook handling, and audit history that records who requested the deletion.
- When a deletion request is rejected, the job stays in place and the requester gets the rejection reason.
- Requesters and approvers can withdraw a pending job deletion request from the Job page or through the approvals flow.
### Approvals & Actions
- The Actions hub now correctly includes service reports that were uploaded from the office or mobile and are still under review, so report approvals no longer disappear from Actions, desktop Approvals, or the dashboard “Reports pending” tile.
- Actions now serves as the one place to see everything needing attention, including training and policies, job-required gaps, your own tickets and renewals, your own rejected reports, team competency expiries, approvals for certs, new users, email changes, service reports, supplier insurance, and approved reports that still need to be sent.
- Personal Actions now includes rejected service reports you uploaded, with the rejection reason, so you can jump back to the related job from “For you.”
- For people with Service Reports write access, Actions now also shows approved reports that have not yet been sent to the client, under “Your team.”
- On the desktop Approvals page, Job Deletions now appears as its own approval group, with a disabled approve action on your own requests and a link back to the job.
- On mobile, the Actions approvals list now includes job deletions alongside the other approval types.
- The Actions badge count now includes the new report items as well as the expanded approval coverage.
### Service Reports
- You can now upload a revised version of a service report while it is still under review, so you can correct it before it is approved.
- The same “Upload revised version” option is now available from the desktop Job page, the Report Review sheet, and the mobile Job page.
- Rejected reports still show “Upload corrected version,” keeping the fix-up flow clear.
- Reports in the old revoked state no longer show the re-upload option, since revoked reports are reopened as under review instead.
### Photos, Videos & Files
- Video thumbnails now show a real poster frame instead of a generic tile, making galleries easier to scan on desktop and mobile.
- Video poster frames are generated from the clip itself and cached like other thumbnails, so the first view is quick and repeat visits are faster.
- When a video can’t be decoded for a poster frame, the app now remembers that result and stops retrying, which avoids repeated delays and speeds up gallery loads.
- In file galleries, video tiles now show the poster under the play button when available, and fall back to the dark play tile when it isn’t.
- In the lightbox, videos now use a poster image while the player loads, which makes opening clips feel smoother.
### Mobile
- The mobile Job page now supports uploading a revised report while it is still under review, matching the desktop workflow.
- Mobile Actions now includes the new Job Deletions approval items, so approvers can handle deletion requests from the phone.
- Mobile gallery video tiles now use the new poster-frame thumbnails, giving media a clearer preview on smaller screens.
### Performance & Reliability
- Video thumbnails now use a bundled ffmpeg-based poster generator, which removes the need for a system ffmpeg package and makes video preview generation more reliable in the app’s runtime.
- Poster frames are cached in the same thumbnail pipeline as photos and PDFs, reducing repeat processing and speeding up gallery browsing.
- Undecodable videos are flagged once so the app does not keep reprocessing the same failed clip on every gallery load.
- Approval routing now correctly treats both submitted and under-review reports as pending, preventing missing approval work in the queue and dashboard counts.

## v1.3.40 — 2026-09-08

### Photos & Files
- You can now upload videos as well as photos on job and equipment records, including iPhone `.mov`/`.mp4` files, Android `.mp4`/`.3gp`/`.webm`, and other common formats like `.mkv`, `.avi`, and `.m4v`.
- The upload screen now shows videos clearly with a film-style icon, file size, and a note that they are not AI-reviewed, helping you understand what’s being stored before you submit.
- Files over 100 MB are now flagged at upload time, so you get early feedback before a large video fails.
- On photo and file screens, video items now appear as a dedicated dark video tile with a play icon instead of looking like a broken or empty image.
- Video attachments now open and play directly in the file viewer and mobile media viewer, so you can review clips without leaving the job.
- If a video codec can’t be played in the current browser, the viewer now shows a clear message with an option to open or download the original file instead of displaying a black box.
- Video playback now supports seeking and scrubbing in the viewer, so longer clips can be jumped through like normal media.
- On mobile job details, the media grid now shows video tiles correctly, making it easier to spot clips attached to a job.
- From the mobile Photos/Files pickers, you can now choose video files when adding media to a job or equipment record.
### Job Records
- Video attachments now behave as server-owned video records, so they are consistently treated as videos no matter what the browser sends.
- AI review actions are no longer available for video files, which prevents confusing attempts to run photo AI on clips.
- The rerun AI option now returns an error for videos in both job and equipment areas, so users are guided away from unsupported actions.
### Mobile
- Mobile media screens now support video playback in the same viewer used on desktop, giving a consistent experience across devices.
- Mobile Photos/Files selection now includes video formats, so field users can attach clips directly from the app.
### Performance & Reliability
- Large video uploads are supported up to 100 MB, with longer server timeouts and higher request limits to make big clips more reliable to send.
- Video files now stream with proper byte-range support, which improves playback reliability and lets browsers seek through clips smoothly.
- Video files are served inline for in-browser playback, reducing friction when reviewing media attached to a job or asset.

## v1.3.39 — 2026-09-08

### Photos & Files
- Upload photos and documents from a much larger dashed drop area in the Files screen, with the whole gallery panel now accepting drag-and-drop so it’s easier to add files.
- See clear page-wide drag feedback across Forge: every upload drop zone now pulses as soon as you drag a file anywhere on the page, including the Documents, Reports, Incidents and Assets areas.
- Uploads are more reliable for big batches on the Files screen: they now run three at a time, keep going if one file fails, and finish with a summary of what added successfully and what did not.
- If a file fails to upload, you can retry just the failed items instead of starting over, with the server’s reason shown for each problem file.
- Duplicate checks now help with re-uploads: when you try the same files again, Forge can identify items already in the system and let you skip them.
- Delete a file directly from the photo/video viewer with the trash icon, confirm the removal, and continue browsing the next item without closing the viewer unless it was the last file.
- Arrow-key navigation in the viewer no longer jumps away while you are typing in the caption field.
### Video Support
- Upload and view video files in photos and documents: Forge now accepts .mp4 and .mov files up to 100 MB.
- Play videos inline in the desktop lightbox and on mobile, with proper video controls and seeking support.
- Video files now show as dark video tiles with a play icon in galleries, making them easy to spot.
- Video uploads are stored as video, not as photos, so AI review does not run on them and rerun actions are blocked for videos.
- The upload dialog now shows video-specific cues such as a film icon, file size, and a note that videos are not AI-reviewed.
- File pickers on mobile now accept video files too, so you can add videos from mobile screens as well.
- Video playback works better in the viewer and on iPhone/iPad Safari thanks to support for ranged loading and inline streaming.
### Uploads
- Keep uploads running while you move around Forge with a new persistent upload tray in the corner, showing overall progress and each file’s status.
- The upload tray lets you retry a failed file, retry all failed files, remove items, clear the list, or collapse the tray when you want it out of the way.
- The tray includes a quick link back to the destination screen so you can jump straight to the job or equipment record where the files belong.
- Your uploads now survive in-app navigation, so you can leave the page and come back without losing the batch as long as the browser tab stays open.
- Forge warns you before leaving the page while uploads are still active, helping prevent accidental interruption.
- Upload progress is now easier to understand during large batches, with live counts and failure summaries instead of a silent stall.
### Jobs & Equipment
- Job detail pages now respect the tab in the URL, so upload tray links can take you directly to the Files tab for the right job.
- Mobile job screens now use the shared upload flow, so uploads from the mobile view also keep working in the background.
- Equipment screens now use the same refresh flow after uploads, keeping attached files up to date there as well.
### Admin & Settings
- In Settings > Backup > Storage, run a duplicate sweep to scan legacy files, fingerprint them, and flag duplicate or similar files across your existing records.
- Storage reports now surface duplicate-related counts and sweep status, including files that still need fingerprints and storage wasted by spare duplicate copies.
- Merge duplicate files from the Storage area to repoint records to a single shared copy and delete spare blobs, helping reduce storage use.
- Duplicate handling now respects files that are already referenced elsewhere, so reports, documents, people and settings assets are not accidentally changed.
- Duplicates are now marked at the record level so older files can also show duplicate and similar badges in galleries after the sweep.
### Performance & Reliability
- Large batches no longer stop at the first bad file, which prevents the old “stalled halfway through” behavior during drag-and-drop uploads.
- Video uploads are configured for larger files and longer transfers, improving reliability for media-heavy field jobs.
- Upload handling is more resilient overall, with a clearer in-progress state and a safer before-leave warning while work is still active.
- Duplicate fingerprinting and merge operations now run in the background so storage cleanup can happen without blocking normal app use.

## v1.3.38 — 2026-09-08

### Photos & Files
- Uploaded files are now fingerprinted and reused when the exact same bytes are uploaded again, so re-uploads no longer create duplicate storage or bloat the file database.
- File galleries now show a red Duplicate badge when the same file is already attached to that job or piece of equipment, helping you spot repeats at a glance.
- File galleries now also flag visually near-identical images with an amber Similar badge, which makes it easier to catch re-shoots, re-crops, and re-compressed photos.
- A new Duplicates filter chip in the gallery lets you narrow the view to only repeated or similar files when checking a job or equipment record.
- Before uploading, the app now checks whether any selected files are already on that job or equipment and warns you with a clear Skip or Add anyway choice, so you can avoid accidental duplicates.
- PDF uploads now generate a real first-page thumbnail in the gallery, with a PDF badge, so PDFs are easier to recognize and open from the file view.
- Clicking a PDF thumbnail now opens the PDF directly from the gallery, making document review faster from the job or equipment screen.
### Settings & Admin
- A new Storage report in Settings › Backup gives you a clear view of total storage use, broken down by file type, so you can understand where space is going.
- The Storage report now highlights the largest files and shows what records are using them, which helps you find oversized items that may be worth reviewing.
- The Storage report now shows how much storage has been saved by deduplication, so you can see the impact of repeated uploads.
- The Storage report now counts flagged duplicate and similar files, giving you a quick sense of how much repeated content exists in the system.
- The Storage report now includes orphaned blobs, helping you identify storage that is no longer linked to any record.
- A new Remove orphans action in the Storage report deletes unreferenced files safely, while protecting anything still used by jobs, equipment, settings assets like logos and stamps, reports, signatures, and recent uploads under 2 hours old.
- The storage cleanup view now helps admins spot and remove old leftover test or unused files without affecting active records.
### Performance & Reliability
- File uploads now reuse existing stored blobs when the same file is uploaded again, which reduces storage growth and keeps the system leaner over time.
- Orphan-file cleanup now scans across all collections for anything still referenced before deleting storage, reducing the risk of accidental data loss.
- The storage cleanup process now avoids removing very recent uploads, which protects in-progress work while background checks run.
### Security
- Storage cleanup now treats referenced assets conservatively, including settings assets such as logos and stamps, as well as reports and signatures, so important files are not removed by mistake.
- The new storage reporting and cleanup flow helps administrators find and remove unneeded files while preserving records that are still in use.

## v1.3.37 — 2026-09-07

### Release Notes
- Release notes now include the full set of user-visible changes since the last tag, so nothing important is missed in the published notes.
- The notes builder now uses the detailed changelog entries, real commit subjects, and file change summary to produce more complete release notes.
- Release notes are now grouped by area and aim to cover every visible change, rather than a short partial summary.
### Performance & Reliability
- Release notes generation is more reliable and complete, reducing the chance of missing changes from the latest release.
- A live verification showed the new process captures a much fuller change list across the app, improving trust in release communications.

## v1.3.36 — 2026-09-07

- Fixed a GitHub save conflict issue so changes now go through cleanly without manual overwrite steps.

## v1.3.35 — 2026-09-07

- Mobile upload and equipment dialogs now fit better on phones, with scrolling that stays within the screen.
- Mobile Jobs now includes a sort control, with newest jobs shown first by default and your choice saved on each device.
- Full-size photos now open faster and more reliably on mobile by loading a smaller viewing copy first, with an option to open the original image.
- Older photos are being automatically reduced in size in the background to improve performance and save memory.
- The Equipment page now has a clearer layout with Overview, Files, and a new Timeline showing the full history for each unit.
- QR labels are back on the Equipment side panel for quicker access.
- The Equipment table now shows ratings and lets you add more useful columns like OEM, model, location, and notes.
- Equipment list columns are now sortable, making it easier to find and compare assets.

## v1.3.34 — 2026-09-07

- Faster photo galleries now load thumbnails more efficiently, so large job and equipment photo sets open much quicker.
- Added a dedicated Equipment page with tabs for details, service reminders, files, and service history, plus QR and print actions.
- You can now add equipment directly from a job’s Equipment card, including selecting existing site equipment or creating a new item.
- The photo crop tool now appears on top of the viewer and is easier to use, with the caption and category controls centered below the image.
- Job and equipment files now use the same shared gallery, making photo features consistent across the app.
- Improved AI and upload workflows for files, including cropping, batch upload, and gallery actions from the new equipment files area.
- Fixed a build issue caused by temporary package registry failures by making installs retry automatically during deployment.
- Reduced app size by removing unused packages, which should help the app start and load more efficiently.

## v1.3.33 — 2026-09-06

- Added stronger access controls for file downloads so users can only open files they’re allowed to see.
- Fixed a regression that was blocking legitimate contractor downloads for files without owner details.
- Required users to be signed in before adding or editing on-site equipment, closing an access gap on public pages.
- Made photo category updates more reliable so your chosen category is no longer overwritten by background AI or other updates.
- Improved equipment edit rows in Settings so they behave correctly after the recent form changes.
- Reduced the chance of silent data mix-ups by giving user edits higher priority than automated updates.

## v1.3.32 — 2026-09-06

- Added photo categories, so users can organize uploads more easily.
- Enabled captions to be added when uploading photos.
- Added photo cropping so images can be trimmed before saving.
- Removed the Fleet page, since compliance due dates are already shown on the Compliance page.

## v1.3.31 — 2026-09-06

- Added inline captions for each photo in Job Detail so managers can label images quickly and save changes instantly.
- Made equipment field specs easier to organize by adding drag-and-drop reordering, with up/down buttons as a backup.
- Kept equipment spec display order aligned with the order set in Admin, so the on-equipment view matches what admins arrange.

## v1.3.30 — 2026-09-04

- Fixed an issue where custom field values could be saved under the wrong key when labels started the same or changed as you typed.
- Improved custom field handling so data now stays tied to the correct field as you enter or edit labels.

## v1.3.29 — 2026-09-03

- You can now apply one custom equipment field to multiple equipment types at once, making setup easier and reducing duplicate entries.
- The Catalogs area has been redesigned into a cleaner grouped accordion layout, making it easier to find and manage items.
- The first Catalogs section now opens by default, helping you get to the most-used settings faster.

## v1.3.28 — 2026-09-03

- Added custom equipment fields so teams can define their own specs, capture them on equipment records, and keep them visible in the relevant parts of the app.
- Made equipment rules easier to set up with separate dropdowns for type, OEM, and model, improving matching and reducing manual entry.
- Added a one-click select-all for the equipment list that works with the current filters and sorting, so bulk actions are faster and safer.
- Let users show custom fields as columns in the equipment register, sort them, and save those columns as the default view.
- Added a field-based filter in the equipment register so users can narrow equipment lists by custom field values.
- Enabled service reminders to be calculated from an equipment date field plus an interval, such as setting an end-of-life reminder from a battery install date.
- Improved reminder setup so users can choose to use a date field when creating or updating reminders on equipment and in rules.

## v1.3.27 — 2026-09-02

- Job types now have their own colors, making Service and Project work easier to spot in job lists and job details.
- Job lists now show a Type column with colored badges, so you can scan job type at a glance on web and mobile.
- Equipment records now include an Equipment Type field, with common types like UPS, BESS, RTU, PLC, Diesel Generator, Transformer, and Switchgear.
- You can now filter Serviced Equipment by type, sort by type, and include the type in CSV exports.
- Mobile and web equipment screens now support scanning a nameplate photo to auto-fill equipment details, including equipment type when available.
- Job numbers and service numbers now auto-generate from the job type and client, with separate counters for each prefix.
- The old job-level Equipment Type field has been replaced by Job Type settings, giving more flexible setup and clearer job classification.
- Existing jobs were updated automatically during the release so current records keep working without manual cleanup.

## v1.3.26 — 2026-09-02

- Clarified the mobile bell badge so it now shows unread notifications only, with “Actions due” shown separately.
- Service reminders now link to the Description of Works instead of a task, making reminder setup clearer across equipment, rule, and bulk edit screens.
- When a reminder rule is applied, due dates are now filled in automatically from the completed job, reducing manual entry.
- Existing task-only reminder rules now show as manual until a Description of Works is selected, with a simple way to re-link and update all matching items at once.

## v1.3.25 — 2026-09-02

- Add and edit equipment directly from the mobile job page, with fields for make, model, serial number, rating, and details.
- Equipment entered on a job now stays linked for reporting and photo tagging, making job records more consistent.
- Updated the notifications recipient layout so chips are easier to scan and fit better on the page.
- Kept the preview/test button in its own space for a cleaner, more usable notifications screen.

## v1.3.24 — 2026-09-02

- Maintenance release.

## v1.3.23 — 2026-09-02

- The preview/test action is now a separate button column, making it easier to spot and clearly distinct from recipient choices.
- You can now send a test alert to yourself directly from the recipient setup modal.
- Notification recipient routing has been fixed so the right managers receive report submitted and expiring competency alerts.
- Web push notifications are now much easier to set up in production, with the needed settings and key file wiring fixed.
- A ready-to-use VAPID key setup has been added, so push notifications can be enabled without needing local Python tools.
- The setup guide and environment template were updated with simpler Docker-based steps for generating and configuring push keys.
- Once push is configured, the iOS app can show the “Turn on notifications” card and Forge notifications in the iOS settings page.

## v1.3.22 — 2026-09-02

- Fixed a notification-routing bug so alerts now reach the right people more reliably, including manager-based recipients.
- Improved push notification delivery so “report ready for review” and similar alerts are less likely to be missed.
- Audited notification sending across the app and corrected remaining recipient-type issues.

## v1.3.21 — 2026-09-02

- Added a “Test push notification” button in Admin > Settings > Notifications so admins can verify push alerts are working.
- Improved push notification reliability by automatically re-sending the device’s current subscription whenever the app opens or returns to the foreground.
- Made push setup easier to troubleshoot by confirming the push endpoint is active and properly protected, rather than unavailable.

## v1.3.20 — 2026-09-02

- Fixed a login/logout issue so users can sign out and back in more reliably.
- Improved the Cloudflare Access sign-in flow to handle short delays after logout.
- Reduced the chance of being temporarily blocked from logging back in after ending a session.

## v1.3.19 — 2026-09-02

- Added a branded sign-out screen so users see a clear “Signing you out…” message before being logged out.
- Improved logout behavior to redirect more smoothly after sign-out.

## v1.3.18 — 2026-09-01

- Fixed Cloudflare sign-out so users are properly re-challenged by Access instead of being dumped back to the app login screen.
- Improved logout behavior to remove the brief “flash” of the wrong page during sign-out.

## v1.3.17 — 2026-09-01

- Fixed Microsoft sign-in so users stay on the same site they started on, instead of being bounced to the Cloudflare access page.
- Improved logout behavior so it uses the current site’s address and only shows the Cloudflare logout step when it’s actually needed.
- Added support for multiple Microsoft redirect addresses, so each site can use the right login path automatically.
- Resolved an issue that could send users to the wrong host after successful login when the app base URL was set to a public address.
- Added test coverage to prevent this login/logout host mix-up from coming back.

## v1.3.16 — 2026-09-01

- Fixed sign-in on the internal domain so the app no longer routes users through Cloudflare during login.
- Improved authentication handling to keep the internal Microsoft/Entra login flow on the correct domain.

## v1.3.15 — 2026-09-01

- Fixed an issue where older Forge versions could appear as separate offline servers after an update.
- Improved server tracking so machines are recognized consistently across version or image changes.

## v1.3.14 — 2026-09-01

- Fixed logout so LAN users stay on the local domain instead of being sent through Cloudflare sign-out.
- Removed a brief password-form flash when signing out on the Cloudflare domain, making logout smoother.
- Cleaned up unused code and files from the app to reduce bloat and keep the product lean.

## v1.3.13 — 2026-09-01

- Simplified sign-in so login flows are more reliable behind Cloudflare Access.
- Fixed the “Something went wrong” error that could block users from logging in.
- Added clearer push notification handling and messaging.
- Added a bell badge to make unread alerts easier to spot.

## v1.3.12 — 2026-09-01

- See outstanding work at a glance with a red count badge on the Actions tab and on the app icon.
- Open job photos in a full-screen in-app viewer with swipe and arrow navigation, then return cleanly to the job page.
- Browse attached files as thumbnail grids for easier review on mobile.
- Fixed Microsoft sign-in errors caused by a date/time mismatch during the login callback.

## v1.3.11 — 2026-08-31

- Added an Actions hub on mobile to bring together your due training, licences, renewals, and team approvals in one place, with quick approve/reject actions.
- Let managers approve or reject items directly from the mobile app without leaving the main workflow.
- Added an admin-only option to hide owners or other excluded staff from personnel lists, approvals, training views, and related tracking screens.
- Improved compliance views so excluded accounts no longer clutter team lists or reporting.
- Simplified our release process so updates are generated automatically from recent changes.
- Reduced build overhead by stopping an extra backend image from being published on every update.

## v1.3.10 — 2026-08-31

- The phone experience is now a full, self-contained app: a bottom tab bar (Home, Jobs, Training, More) with its own screens, so field crews stay in the mobile app instead of jumping to the desktop site
- New mobile dashboard shows what matters onsite at a glance — active jobs, what's coming up, and renewals due for you and the people you manage — with tap-through tiles
- Managers get a quick mobile job view (sign-on QR, who's onsite, and required documents) without opening the full desktop page
- Notifications now live inside the mobile app, and today's jobs are cached so "Coming up" and sign-on still work with no signal on site
- Microsoft (Entra ID) sign-in is more reliable, with clear on-screen messages instead of a generic error if something is misconfigured
- Signing out under Cloudflare now cleanly signs you back in next time, including on the installed phone app
- Smaller, faster app images for quicker, more reliable updates
- Mobile home dashboard streamlined: tappable tiles now stay inside the phone app, a one-tap "Report an incident" button, searchable team list, tidier header, and renewals you can tap straight through to fix
- Mobile Jobs now lists the job number with client and site, with Active/All filtering and search
- New mobile "My profile" screen (details, licences and competencies with expiry status)
- Clearer "Install app" guidance on iPhone, and Microsoft sign-in now shows a helpful message instead of an error page if something needs fixing

## v1.3.9 — 2026-08-31

- The phone experience is now a full, self-contained app: a bottom tab bar (Home, Jobs, Training, More) with its own screens, so field crews stay in the mobile app instead of jumping to the desktop site
- New mobile dashboard shows what matters onsite at a glance — active jobs, what's coming up, and renewals due for you and the people you manage — with tap-through tiles
- Managers get a quick mobile job view (sign-on QR, who's onsite, and required documents) without opening the full desktop page
- Notifications now live inside the mobile app, and today's jobs are cached so "Coming up" and sign-on still work with no signal on site
- Microsoft (Entra ID) sign-in is more reliable, with clear on-screen messages instead of a generic error if something is misconfigured
- Signing out under Cloudflare now cleanly signs you back in next time, including on the installed phone app
- Smaller, faster app images for quicker, more reliable updates
- Mobile home dashboard streamlined: tappable tiles now stay inside the phone app, a one-tap "Report an incident" button, searchable team list, tidier header, and renewals you can tap straight through to fix
- Mobile Jobs now lists the job number with client and site, with Active/All filtering and search
- New mobile "My profile" screen (details, licences and competencies with expiry status)
- Clearer "Install app" guidance on iPhone, and Microsoft sign-in now shows a helpful message instead of an error page if something needs fixing

## v1.3.8 — 2026-08-31

- The phone experience is now a full, self-contained app: a bottom tab bar (Home, Jobs, Training, More) with its own screens, so field crews stay in the mobile app instead of jumping to the desktop site
- New mobile dashboard shows what matters onsite at a glance — active jobs, what's coming up, and renewals due for you and the people you manage — with tap-through tiles
- Managers get a quick mobile job view (sign-on QR, who's onsite, and required documents) without opening the full desktop page
- Notifications now live inside the mobile app, and today's jobs are cached so "Coming up" and sign-on still work with no signal on site
- Microsoft (Entra ID) sign-in is more reliable, with clear on-screen messages instead of a generic error if something is misconfigured
- Signing out under Cloudflare now cleanly signs you back in next time, including on the installed phone app
- Smaller, faster app images for quicker, more reliable updates
- Mobile home dashboard streamlined: tappable tiles now stay inside the phone app, a one-tap "Report an incident" button, searchable team list, tidier header, and renewals you can tap straight through to fix
- Mobile Jobs now lists the job number with client and site, with Active/All filtering and search
- New mobile "My profile" screen (details, licences and competencies with expiry status)
- Clearer "Install app" guidance on iPhone, and Microsoft sign-in now shows a helpful message instead of an error page if something needs fixing

## v1.3.7 — 2026-08-31

- Servers page: give each server a friendly name, and single standalone servers now show their version
- AI Calls log now shows the model's reasoning (chain-of-thought) and flags responses that were cut off
- Report AI review now runs in the background — keep working while it checks; results appear when ready
- Report AI review is now more reliable: deterministic checking, an automatic retry, and a clear High-confidence / Review-carefully badge showing exactly what was analysed
- Job photos are now understood automatically on upload — each gets an AI caption, category and any notable observations, which you can edit
- Report AI review now verifies the report claim-by-claim (a statement check: verified / contradicted / unsupported) and understands your attached photos
- Report AI review learns your brand voice from your own reject notes on past reports, plus an optional house-style you can set in Settings → Brand
- Cleaner, controlled release notes (curated per release instead of auto-scraped from commits)

## v1.3.6 — 2026-08-28

- Servers page: give each server a friendly name, and single standalone servers now show their version
- AI Calls log now shows the model's reasoning (chain-of-thought) and flags responses that were cut off
- Report AI review now runs in the background — keep working while it checks; results appear when ready
- Report AI review is now more reliable: deterministic checking, an automatic retry, and a clear High-confidence / Review-carefully badge showing exactly what was analysed
- Job photos are now understood automatically on upload — each gets an AI caption, category and any notable observations, which you can edit
- Report AI review now verifies the report claim-by-claim (a statement check: verified / contradicted / unsupported) and understands your attached photos
- Report AI review learns your brand voice from your own reject notes on past reports, plus an optional house-style you can set in Settings → Brand
- Cleaner, controlled release notes (curated per release instead of auto-scraped from commits)

## v1.3.5 — 2026-08-27

- Servers page: give each server a friendly name, and single standalone servers now show their version
- AI Calls log now shows the model's reasoning (chain-of-thought) and flags responses that were cut off
- Report AI review now runs in the background — keep working while it checks; results appear when ready
- Report AI review is now more reliable: deterministic checking, an automatic retry, and a clear High-confidence / Review-carefully badge showing exactly what was analysed
- Job photos are now understood automatically on upload — each gets an AI caption, category and any notable observations, which you can edit
- Report AI review now verifies the report claim-by-claim (a statement check: verified / contradicted / unsupported) and understands your attached photos
- Report AI review learns your brand voice from your own reject notes on past reports, plus an optional house-style you can set in Settings → Brand
- Cleaner, controlled release notes (curated per release instead of auto-scraped from commits)

## v1.3.4 — 2026-08-27

- Servers page: give each server a friendly name, and single standalone servers now show their version
- AI Calls log now shows the model's reasoning (chain-of-thought) and flags responses that were cut off
- Report AI review now runs in the background — keep working while it checks; results appear when ready
- Report AI review is now more reliable: deterministic checking, an automatic retry, and a clear High-confidence / Review-carefully badge showing exactly what was analysed
- Job photos are now understood automatically on upload — each gets an AI caption, category and any notable observations, which you can edit
- Report AI review now verifies the report claim-by-claim (a statement check: verified / contradicted / unsupported) and understands your attached photos
- Report AI review learns your brand voice from your own reject notes on past reports, plus an optional house-style you can set in Settings → Brand
- Cleaner, controlled release notes (curated per release instead of auto-scraped from commits)

## v1.3.3 — 2026-08-27

- Servers page: give each server a friendly name, and single standalone servers now show their version
- AI Calls log now shows the model's reasoning (chain-of-thought) and flags responses that were cut off
- Report AI review now runs in the background — keep working while it checks; results appear when ready
- Report AI review is now more reliable: deterministic checking, an automatic retry, and a clear High-confidence / Review-carefully badge showing exactly what was analysed
- Job photos are now understood automatically on upload — each gets an AI caption, category and any notable observations, which you can edit
- Report AI review now verifies the report claim-by-claim (a statement check: verified / contradicted / unsupported) and understands your attached photos
- Report AI review learns your brand voice from your own reject notes on past reports, plus an optional house-style you can set in Settings → Brand
- Cleaner, controlled release notes (curated per release instead of auto-scraped from commits)

## v1.3.2 — 2026-08-27

- All four items are implemented and verified

## v1.3.1 — 2026-08-27

- AI error deep-link
- AI Calls audit log
- AI tuning knobs + shared helper + reviewer-picked photos + thinking-safe parsing — built & tested (7/7)
- Install nudge + desktop start-view fix + offline-node alert
- PWA install offer + phone→mobile routing + stale-node badge
- Per-node version check on the Servers page
- Automated release notes + GitHub Release
- Release image-name fix + Backup Health on Servers page
- Servers Page: Cluster Dashboard + Guarded Failover
- Nameplate Reader + Incident AI Assist
- Quiet Hours + Vision (VLM) AI Upgrades
- Web Push + Server Nudge + Tunable Timing
- Auto-Retry Nudge + App-Tile Badge
- Tappable sync badge — details + retry
- Offline photos + sync badge
- Offline sign-on
- install banner + manager "My team" ticket upload (offline sign-on scoped next)
- Worker mobile app — Phase 1
- Clarified backup question + fixed a real backup gap
- verified (features #1, #3, #4) + DB/failover advice (#2)
- Serviced Equipment — reminder rules + bulk edit + sort/filter
- Security Audit + Remediation
- Photo compression + send-history detail
- Report send/re-upload enhancements
- Image slimming + release automation
- Confirmed — here's the clean model and what to do
- Distribution build scaffolded — streamlined product image (no demo/welcome/Stripe/licence-gen)
- Admin Integrations tab + Cloudflare Access diagnostics
- Licence-server default + Forge Compliance branding
- Cloudflare Access SSO + dedicated marketing SMTP
- Landing form + spam protection + Licensing (model B)
- Landing lead form — email validation + simplified consent (TESTED iter104 via testing_agent: backend 100%, frontend 100…

## v1.3.0 — 2026-08-27

- AI error deep-link
- AI Calls audit log
- AI tuning knobs + shared helper + reviewer-picked photos + thinking-safe parsing — built & tested (7/7)
- Install nudge + desktop start-view fix + offline-node alert
- PWA install offer + phone→mobile routing + stale-node badge
- Per-node version check on the Servers page
- Automated release notes + GitHub Release
- Release image-name fix + Backup Health on Servers page
- Servers Page: Cluster Dashboard + Guarded Failover
- Nameplate Reader + Incident AI Assist
- Quiet Hours + Vision (VLM) AI Upgrades
- Web Push + Server Nudge + Tunable Timing
- Auto-Retry Nudge + App-Tile Badge
- Tappable sync badge — details + retry
- Offline photos + sync badge
- Offline sign-on
- install banner + manager "My team" ticket upload (offline sign-on scoped next)
- Worker mobile app — Phase 1
- Clarified backup question + fixed a real backup gap
- verified (features #1, #3, #4) + DB/failover advice (#2)
- Serviced Equipment — reminder rules + bulk edit + sort/filter
- Security Audit + Remediation
- Photo compression + send-history detail
- Report send/re-upload enhancements
- Image slimming + release automation
- Confirmed — here's the clean model and what to do
- Distribution build scaffolded — streamlined product image (no demo/welcome/Stripe/licence-gen)
- Admin Integrations tab + Cloudflare Access diagnostics
- Licence-server default + Forge Compliance branding
- Cloudflare Access SSO + dedicated marketing SMTP
- Landing form + spam protection + Licensing (model B)
- Landing lead form — email validation + simplified consent (TESTED iter104 via testing_agent: backend 100%, frontend 100…

## v1.2.1 — 2026-08-27

- Install nudge + desktop start-view fix + offline-node alert
- PWA install offer + phone→mobile routing + stale-node badge
- Per-node version check on the Servers page
- Automated release notes + GitHub Release
- Release image-name fix + Backup Health on Servers page
- Servers Page: Cluster Dashboard + Guarded Failover
- Nameplate Reader + Incident AI Assist
- Quiet Hours + Vision (VLM) AI Upgrades
- Web Push + Server Nudge + Tunable Timing
- Auto-Retry Nudge + App-Tile Badge
- Tappable sync badge — details + retry
- Offline photos + sync badge
- Offline sign-on
- install banner + manager "My team" ticket upload (offline sign-on scoped next)
- Worker mobile app — Phase 1
- Clarified backup question + fixed a real backup gap
- verified (features #1, #3, #4) + DB/failover advice (#2)
- Serviced Equipment — reminder rules + bulk edit + sort/filter
- Security Audit + Remediation
- Photo compression + send-history detail
- Report send/re-upload enhancements
- Image slimming + release automation
- Confirmed — here's the clean model and what to do
- Distribution build scaffolded — streamlined product image (no demo/welcome/Stripe/licence-gen)
- Admin Integrations tab + Cloudflare Access diagnostics
- Licence-server default + Forge Compliance branding
- Cloudflare Access SSO + dedicated marketing SMTP
- Landing form + spam protection + Licensing (model B)
- Landing lead form — email validation + simplified consent (TESTED iter104 via testing_agent: backend 100%, frontend 100…

## v1.2.0 — 2026-08-26

- Per-node version check on the Servers page
- Automated release notes + GitHub Release
- Release image-name fix + Backup Health on Servers page
- Servers Page: Cluster Dashboard + Guarded Failover
- Nameplate Reader + Incident AI Assist
- Quiet Hours + Vision (VLM) AI Upgrades
- Web Push + Server Nudge + Tunable Timing
- Auto-Retry Nudge + App-Tile Badge
- Tappable sync badge — details + retry
- Offline photos + sync badge
- Offline sign-on
- install banner + manager "My team" ticket upload (offline sign-on scoped next)
- Worker mobile app — Phase 1
- Clarified backup question + fixed a real backup gap
- verified (features #1, #3, #4) + DB/failover advice (#2)
- Serviced Equipment — reminder rules + bulk edit + sort/filter
- Security Audit + Remediation
- Photo compression + send-history detail
- Report send/re-upload enhancements
- Image slimming + release automation
- Confirmed — here's the clean model and what to do
- Distribution build scaffolded — streamlined product image (no demo/welcome/Stripe/licence-gen)
- Admin Integrations tab + Cloudflare Access diagnostics
- Licence-server default + Forge Compliance branding
- Cloudflare Access SSO + dedicated marketing SMTP
- Landing form + spam protection + Licensing (model B)
- Landing lead form — email validation + simplified consent (TESTED iter104 via testing_agent: backend 100%, frontend 100…

## v1.1 — 2026-08-25

**Automated release notes + GitHub Release**
- **Name**: desc` lines) render tidily. You can always hand-polish any single release by editing it on the Releases tab afterwards

**Servers Page: Cluster Dashboard + Guarded Failover**
- **Settings → Servers** (admin-only, on every node): live replica-set view — "This server is PRIMARY (master) / STANDBY" banner, per-member health, replication lag, uptime, priority/votes, auto-refresh, plus a warning when you're on 2 voting members. Single-server installs just show "standalone" - **Guarded actions replace every §5 docker-exec command**: Step down primary (Mongo refuses without a caught-up standby), Promote this node (locked until NO primary is reachable + typed PROMOTE; force-reconfig on the survivor — split-brain refused server-side), and Re-add mem…
- **Tested with a full disaster drill** on a real local 2-member replica set: killed the primary → promote unlocked → promoted → old node re-added and rejoined as SECONDARY (no split-brain) → step-down handed primary back → watchdog fired both down and recovered alerts. All guard rails (wrong confirm, primary-alive refusal, quorum failures) verified; preview restored to standalone afterwards - **To enable on your cluster**: create the `forgecluster` Mongo user and set `MONGO_CLUSTER_URL` + `CLUSTER_SELF_HOST` per the new §5b in MULTI_SERVER_SETUP.md (compose + env.template updated). ⚠️ Not yet run on your real Synology/Nebula cluster — t…

**Nameplate Reader + Incident AI Assist**
- **Nameplate Reader**: "Read nameplate (AI)" in the Serviced Equipment detail sheet — snap/pick a photo (camera capture on mobile) and the VLM pre-fills OEM, model, serial, rating and appends extras (voltage/year/etc) to Details; you review…
- **Incident AI Assist**: new "AI assist" panel in the incident GPS review — one click gives a summary, suggested severity (with Apply button when it differs), likely root cause, and suggested corrective actions each with "+ Add" into the real…
- **Testing**: full E2E verified with a mock OpenAI-compatible server — nameplate field-fill in the browser, assist with photos routed to the vision model, vision-off fallback to the main model, persistence, and "+ Add" flow all pas…

**Quiet Hours + Vision (VLM) AI Upgrades**
- **Quiet hours**: the server sync nudge now skips workers inside their My Profile quiet hours (same window as email) and fires once the window ends — tested with per-user prefs and safe defaults
- **Vision (VLM)**: new Settings → AI/LLM "Enable vision (VLM)" toggle + optional separate vision model (blank = main model). Scanned/no-text PDFs are now rendered to page images for the VLM everywhere (report proof-check, cert/insurance…
- **Testing**: backend unit tests 5/5 + testing agent iteration_106 — 11/11 backend, 100% frontend, no defects. Note: preview has no live LLM, so real qwen3.8-VL output quality is yours to validate — point Settings → AI/LLM at your…

**Web Push + Server Nudge + Tunable Timing**
- **Closed-app push (VAPID)**: new backend push router + `core/push_service.py`, VAPID keys generated (private PEM git-ignored, public key in env), service-worker `push` handler, and `lib/push.js` opt-in. The "Remind me" button now registers a real…
- **Server nudge**: a background `sync_nudge_loop` pushes a reminder to a worker's phone when their offline sign-on stays unsynced past the threshold — even if the app is shut. The client reports its queue state (`reportQueueState`) when…
- **Tunable timing**: admins set "Nudge workers after (minutes unsynced)" in Settings → Notifications (`sync_nudge_minutes`, default 30, 5–1440), used by both the in-app nudge and the server push

**Auto-Retry Nudge + App-Tile Badge**
- **Fixed the blocker**: `window.forgeOffline` now exposes `updateAppBadge` + `oldestAgeMs` (the missing hook that caused the earlier `is not a function` test error; the real app already imported them directly). - The feature set was already…

**Tappable sync badge — details + retry**

**Offline photos + sync badge**
- **Offline photos**: the offline queue now holds an image
- **Risk photos offline**: when a worker attaches a risk photo with no signal, it's stored as a blob with a local preview; `finalize()` chains its upload before the sign-on so the photo lands with the record on sync
- **Sync badge**: a calm, generic pill on the mobile home — "{n} waiting to sync" when offline, "Syncing…" when online, hidden when nothing's queued. Verified it renders ("1 waiting to sync") and auto-clears. Kept it simple as you aske…

**Offline sign-on**

**Worker mobile app — Phase 1**

**What I built for your exact setup**

**Built all four + fixed your Mongo error's real cause**

**Clarified backup question + fixed a real backup gap**

**Both requested features**
- **Compliance timeline — insurance type**: supplier/personnel insurance records now display the actual insurance type in the timeline label (backend `compliance.py`, already in place — confirmed)
- **Editable job files**: added an Edit action + dialog to the job Files tab (`JobDetail.jsx`) driven by the existing job-scoped `PUT /api/jobs/{jid}/files/{fid}` endpoint. Managers can edit name, note/description and re-link equipment; visibi…

**1. Save default view (per‑user)**

**1. Autosave scheduling**

**Serviced Equipment — reminder rules + bulk edit + sort/filter**
- **Precedence:** most‑specific rule wins, and a rule with a **client set always beats a client‑agnostic (global)** one — verified: `ZZMTM · THYCON · MPX` got the client rule (L1@3mo, L2@12mo), while `OtherCo · THYCON · MPX` fell back to the global rule. - Each reminder **links to a Task Type** (L1/L2, selectable). - **Auto‑applies on equipment creation**; existing gear gets a manual **"Apply matching rule"** (single) or **"Apply rules"** (bulk) button. - **Never clobbers your hand‑edited reminders** — verified a manual reminder survived a rule re‑apply while the rule ones refreshed. **Bulk edit**: Select rows →
- **"Apply rules"** runs matching rules across the selection. **Table sort/filter**: Every shown column is now

**Your question: does an email go out?**
- **Licence key**: **Registry username + access token** - A 5‑step quick setup: open the guide → `docker login` (ready‑to‑paste) → configure `.env` → `docker compose up -d` → activate in Settings → Licence - A link to the

**Security Audit + Remediation**
- **SEC-001 (CRITICAL) — privilege escalation to Administrator**: any manager (or personnel-write user) could set a teammate's role to `admin`/`gps_manager` via invite or user-update and take over the platform. Fixed with a role-hierarchy guard (`_assign_role_allowed`) on both endpo…
- **SEC-002 (HIGH) — unauthenticated file-download signing oracle**: the public sign-on "attach file" endpoint needed no session and would sign a download URL for any stored file id. Fixed: attach now requires a valid job attendance, the file must have been uploaded via the public uplo…
- **SEC-003 (MEDIUM) — SSRF in webhook test**: blocked private/loopback/link-local/metadata targets + disabled redirects. Verified: metadata IP & localhost → 400. Accepted/low-risk items (CORS via env, demo seed password, admin-only regex search, self-only templat…

**Photo compression + send-history detail**
- **Compress Large Files**: the Send dialog now has a "Downscale large photos before sending" toggle (default on when photos are selected). The backend downscales image attachments to max 1600px / JPEG q80 via Pillow before sending (report PDF &…
- **Send History Detail**: each send is now logged with recipients + the exact attachment filenames, shown as a "Send history" section in the report History popover. Verified: log recorded `['report.pdf','photo.jpg']`. Backend logic verified wi…

**Report send/re-upload enhancements**
- **Re-upload Notify**: submitting a corrected version of a rejected report now notifies admins + in-house managers + the person who rejected it ("ready for review & sign-off"). Verified: notification created (2 recipients), same report id k…
- **Ignored-file Notice**: the send endpoint returns `{attached, ignored}` and the Send dialog shows a warning toast when selected files can't be attached. Verified: bogus ids → ignored=2, attached=1 (report file)
- **Attachment Size Guard**: `/jobs/{jid}/review-files` now returns each file's size; the Send dialog shows per-file MB + total, warns inline over ~15 MB, and asks to confirm before sending an oversized batch. Verified: size returned correctly. A…

**Image slimming + release automation**

**Why the build crashed**
- **Removed my duplicates:** `dist/`, `forge-compliance-app/`, the root `.dockerignore`, and `.github/workflows/build-images.yml`. Only your original **`docker-publish.yml`** remains. - **Kept two safe, non-duplicative wins**: `server.py` now imports the storefront router only when `STOREFRONT_ENABLED=1` (no behaviour change — product installs default to `0`). - Added `backend/.dockerignore` so tests/pycache/.env stay out of the backend ima…

**Confirmed — here's the clean model and what to do**

**Distribution build scaffolded — streamlined product image (no demo/welcome/Stripe/licence-gen)**

**Admin Integrations tab + Cloudflare Access diagnostics**

**Licence-server default + Forge Compliance branding**

**Cloudflare Access SSO + dedicated marketing SMTP**

**Landing form + spam protection + Licensing (model B)**

**Landing lead form — email validation + simplified consent (TESTED iter104 via testing_agent: backend 100%, frontend 100%, no issues)**
- **Email validation**: invalid emails like "test" / "test@" are now blocked on the Try-the-demo, Buy-the-licence and Stripe-checkout flows — frontend regex + backend `EmailStr` (returns 422). A valid email is required to proceed
- **Simplified form**: removed the

**Why your Stripe keys weren't in the panel**

<details><summary>Other changes in this release</summary>

- Saved both, in one place
- Added a copy‑paste **⚡ Quick start** right below "What you'll need" — four commands (registry login → clone → configure → `docker compose up -d`), then "open :8080 → Settings → Licence." The detailed sections remain below for anyone who wants the full walkthrough
- Done — and verified end‑to‑end in preview
- Done. Here's the honest summary of what I changed and why it's now genuinely a cleaner product build
- All three fixes verified
- All done and verified locally by simulating the release step. Here's what changed
- Everything's ready. Here's the summary
- The workflow will now fail fast with a clear message if the token is missing. The root cause is that the `DEPLOY_REPO_TOKEN` secret isn't set, and GitHub's built‑in `GITHUB_TOKEN` **cannot** push to a *different* repo — so cross‑repo release sync needs your own token. Here's the exact one‑time setup
- auto-commit for dd50b24a-93fc-4c43-b073-c5839b90e44c
- auto-commit for 90038171-906c-47a3-a6ed-09cb6bdf0f7f
- auto-commit for 73f1a8de-d1c2-465f-962f-3d658ca8eb14
- auto-commit for 40842568-337a-4502-9558-bcaadd966832
- auto-commit for 317ca021-7b6d-4b1f-a238-e152cb15bcbe
- auto-commit for aa828f44-40e8-4021-b5be-699c8460491c
- auto-commit for 08a76b4e-6f27-4af9-bc6f-fda789142122
- auto-commit for 15261869-52a7-482c-bb23-39d9ed83567e
- auto-commit for a1834077-4dcb-474e-9dff-3ba2b8d46dfc
- auto-commit for cee717a9-2db9-46a3-ae1b-87adeab362cd
- auto-commit for 4cc27742-0ec3-4cc0-a535-ef6e316971de
- auto-commit for 330d9b94-a627-4aa4-adf7-f701eeffbb89
- auto-commit for 7d0d7787-a6f6-43cd-b8c7-7fa7d6cfd399
- auto-commit for d00459b3-4b80-4624-98b5-70bbc1bf5536
- auto-commit for adbe6aba-2d61-4074-8c9e-22623cff2a53
- auto-commit for 707a54b9-c82b-4c38-9cc7-7e2f1f23b056
- auto-commit for 9c1ad122-6dd5-4a50-a98e-7bb910f16c89
- auto-commit for 25249b7d-4ce7-4262-a8ff-be479508edce
- auto-commit for 667aef6f-70fa-4804-bb0f-ab2ee8b3d2b7
- auto-commit for d772edfb-35fe-469f-b3b1-f980535e4e5d
- auto-commit for ec209cef-740a-40f5-80ff-b4096c3f0d11
- auto-commit for 443b736e-def3-49c2-ab9b-8418a74fff2c
- auto-commit for bd1e2856-0957-4827-9116-99ea7e3160b4
- auto-commit for ba550bc8-5f34-49f4-b277-64ab4a111a09
- auto-commit for 427723f6-5213-4d1d-bb73-f3fea7b0bdb8
- auto-commit for d8aa87d7-4014-459e-89fe-a0e1d1302596
- auto-commit for ee734092-d588-46ba-8c39-e72ce41812aa
- auto-commit for 9dfab80e-fc30-4753-99f9-ed31b2878a26
- auto-commit for b60de77e-7702-4d5d-98ce-9d3e4969e3f7
- auto-commit for 004f953a-dea1-45d7-96ea-c89ac4d498c0
- auto-commit for 24c711f4-1fe6-47c7-bdd2-78c1b17a82ee
- auto-commit for c341b6bc-8c5f-471c-814b-d7ab2e3f0885
- auto-commit for eb531240-7512-4d6c-b393-54d3785fa47f
- auto-commit for 24c577da-fa95-4323-9580-af2ef7fddeef
- auto-commit for 5c4332d5-7b96-40c2-9a17-5acae0ea716f
- auto-commit for 111e5d2c-0b9c-4a81-b0f7-616789d1ec3a
- auto-commit for dca0879c-642a-406f-9e7d-6c7ed9be4d32
- auto-commit for 50768d62-19b8-475c-9fa6-34d9f2c7d3c7
- auto-commit for 45c5a173-4a5f-44c2-8689-93ea88cdfc7d
- auto-commit for 1655b06b-bc27-4de2-add4-6a4f9b6a666d
- auto-commit for 80c1a00f-4a68-4003-99eb-f0d5a64c236b
- auto-commit for f4046475-5fb5-4495-a23d-5fa64d2fdfec
- auto-commit for e8b1b4cd-edad-488a-8bfe-d8817f33c6da
- auto-commit for 5fd874ad-31d3-484e-b4e1-e3ecc3d52308
- auto-commit for 809f3053-c1f7-4544-a951-b021826d41a6
- auto-commit for a75f66cb-7889-4baa-b98d-22407ed55d3c
- auto-commit for 1907b96b-7518-42bd-ab33-c34f774ba263
- auto-commit for 7dff893f-6e65-4449-9092-d58d8d72a178
- auto-commit for 6b0627a2-b4f7-4e98-950a-a9b510105f8b
- auto-commit for 7d0d7c64-4cbc-412e-963e-8db912d52122
- auto-commit for 2d1dd3b3-317e-48b4-9e08-b23911620d13
- auto-commit for 35bed9ae-90d6-462b-ba0a-348f708aed4b
- auto-commit for ea21377d-bfd0-4ddd-aacb-5b666a5237e9
- auto-commit for ad4aad25-5a70-4c74-8833-2f5a4edf1c14
- auto-commit for aedf0a01-b423-4ec9-a8c4-d69152889ac0
- auto-commit for b55e6dee-444b-4a16-84fe-e6dbe42392aa
- auto-commit for a6072ea2-05bc-4e68-b4b9-dd18aed15601
- auto-commit for c7932162-377a-4716-b5e9-75657d1716b6
- auto-commit for bd1176ef-076f-4534-a639-e95d1fe4ac9f
- auto-commit for 5ad5b582-f6dd-4f94-a7ed-f6f7a70cf792
- auto-commit for c59737c0-c203-45da-af06-287d8a6bb6fe
- auto-commit for 53490539-f2bf-4171-99c6-c61c5c964166
- auto-commit for c69338d4-ec2b-4f31-a666-e08ca548e40d
- auto-commit for 3952e6f4-6cd2-4ab5-8539-0ef0aa7bd994
- auto-commit for 1b42f1ba-9309-480c-821a-52ef6b9aa5e6
- auto-commit for e3f4171e-d98d-4c6b-8647-8be889fe22a3
- auto-commit for ff4f4b2b-b1d4-487d-93f6-27faa39a150c
- auto-commit for d099390d-6c3a-44a7-94c6-34e43b5d9e23
- auto-commit for 58463889-fa5e-4263-9e68-36411b4baa95
- auto-commit for 313f8408-8944-437f-95bb-9c2c907d8709
- auto-commit for ef355c84-fdb4-478e-af6f-c27c62867578
- auto-commit for 07e5ced0-e514-4a3d-98b3-f9d0c2d438ac
- auto-commit for 1d684242-5b5f-4497-82f6-750ca9a6e8fe
- auto-commit for 3e99ace1-610e-46e6-8d4d-5e2512d84775
- auto-commit for 9f27c648-fe57-44c7-9310-6b1aa51b6bf3
- auto-commit for f05c6203-3035-400c-aa16-e2994738656d
- auto-commit for 019afaa7-7b96-4a6e-8f1e-afb1dac5d1c4
- auto-commit for 69dae3d4-7d50-4888-b2db-d87fd2861520
- auto-commit for c08cee1e-2c37-419d-9ad9-f8a1c9b7b8ed
- auto-commit for 3630f303-5ca1-430d-9110-265fb3b4c988
- auto-commit for d36ca572-e123-43fd-99a8-4a7eeffbe523
- auto-commit for 0297c06b-2e3b-411c-bb67-4522f0d8d196
- auto-commit for 9c6dc734-220c-46d8-a39a-f8b5ac330698
- auto-commit for 270a62b7-f83d-4895-b82f-635b474d4129
- auto-commit for 45d165c0-6b90-41aa-b9ba-075e11fcbf10
- auto-commit for 8e91267d-e654-4871-be31-cac620d9a809
- auto-commit for 7fc464dd-0b0d-4124-b6f5-5cfca66df46a
- auto-commit for 8b426112-3b8f-4513-aba2-f8e5c5ea54c7
- auto-commit for 347832b7-cd21-4c0b-b4f0-f7cf5aa3cd05
- auto-commit for 350fe710-6e09-40ff-9d79-5c56cb595d31
- auto-commit for 160c43cd-9d25-4f11-930c-5b10972c0dc9
- auto-commit for 87d0c218-04fe-44d6-91ae-9afdadec48b4
- auto-commit for 4abe6141-4cb6-4a1f-8529-d7b29c603cbb
- auto-commit for 2c2904a7-1667-4818-82f2-6f52bf6575d7
- auto-commit for deef5c59-6de8-480b-a9eb-435ddfd0b637
- auto-commit for 1b109dd6-91e9-4fc5-b15c-9793cbb67dc2
- auto-commit for b5eca32e-e742-4c8f-bdc9-111df912a8f5
- auto-commit for 2f3580be-e688-4520-90a9-29df4adebaed
- auto-commit for 8edcf44c-982d-4b31-b178-1f6148bcf4ec
- auto-commit for a1f9d927-d9ef-4d76-9b9c-97a02a4863c0
- auto-commit for d986d94b-5829-47bc-aaa4-3cd63cb425c5
- auto-commit for 066e53fd-2e2b-4a2f-8dfb-13d9fec51e45
- auto-commit for 4e2eb8f6-4f3f-4f71-9803-dbbf27ef7b78
- auto-commit for 745a8a37-de50-4bf1-a6de-cd2ca55d6261
- auto-commit for 779c4d4d-3150-494f-a4b1-b5dfca4f94c8
- auto-commit for 8965a211-301f-444c-9526-633612cdc186
- auto-commit for c43dc4e3-d661-4aae-8430-6c2393185a39
- auto-commit for 695e77fb-40cf-4daa-b299-93d15798e3f1
- auto-commit for 279fc023-a25b-49c4-a57d-63bafc0859aa
- auto-commit for 7d28dd6b-3c9a-467d-85e0-38be7d5e776c
- auto-commit for f038e04a-47f0-4397-ab53-f692257dabe0
- auto-commit for b35ef5fd-70f3-4721-9df5-450a71895aa2
- auto-commit for bb802936-eea6-4aab-8abe-8caed93d9abb
- auto-commit for 979e8136-6d27-4d5d-8be4-6b1dc5e17dd7
- auto-commit for 08d1ce77-90a6-4a93-b9ef-a2bb75fa57fa
- auto-commit for 7ea8ab5f-ec0e-4eed-afe8-4b967a5fbc9a
- auto-commit for 778d3bd0-fc70-4447-9b83-4150efc03410
- auto-commit for 5908f804-4c8a-4dca-9023-62619456e4ba
- auto-commit for 9b409c9b-73f4-46a0-9198-477b04651474
- auto-commit for 6ad2df2c-11cb-4e94-ae2d-96a9d9f274fe
- auto-commit for 01283028-c369-4daf-8eb1-4739eff62f21
- auto-commit for 93a7d2f7-451d-4adc-ab91-466125314103
- auto-commit for e2cbf85d-4bf8-4fe3-a47e-7bdb91d0d2e2
- auto-commit for 85cd5cd1-65e2-4237-a81d-bfa79e159f39
- auto-commit for 50196493-76dc-496f-b6f5-9c5e078d030e
- auto-commit for 60fb427f-1f7c-4241-b03c-7f2d81087042
- auto-commit for 092ba65c-b98b-401d-809d-72a5d9917009
- auto-commit for 81f57196-efdd-40d7-95fb-c7a7b3d96797
- auto-commit for 3576385d-3e0c-4533-82bd-6b986bed99f8
- auto-commit for 50e313ac-2733-4562-9616-4f7fe8e9cbc4
- auto-commit for c4fbc0ee-a1c7-4bc0-9fbf-9aaf818c015b
- auto-commit for a5c86b19-6121-4b2c-a5e0-c8437c109dcc
- auto-commit for cc10b078-9d8a-49ec-b484-b8ebc6ef4c8a
- auto-commit for a400d5f0-e8a1-4f0f-9b04-f201647c20ff
- auto-commit for 7bb544e3-6e1c-4948-9bd7-6dc7a1c5a1f9
- auto-commit for 04406d68-51d2-445a-af83-38f8b59bd82c
- auto-commit for e00cb451-b1be-490c-9ad1-85ce678effd6
- auto-commit for 22c3ec85-fc50-4139-a9b0-08b1d363882f
- auto-commit for dcd3c6e8-e2e3-4ae0-b5e7-2b26f04213e3
- auto-commit for 76883d44-0c3f-4cdd-91c6-59c97b659871
- auto-commit for 72073aa6-9f93-49ba-8e9e-77630f0b285c
- auto-commit for 17f20357-982e-4bbf-bf2b-e43daef4d252
- auto-commit for 6f9374bb-0d40-4d3f-9521-a6f8e5f211fd
- auto-commit for 0f573e69-3655-4581-aebd-dc08a67cb97e
- auto-commit for b267e0b7-c396-4fc8-b829-2260a694fb02
- auto-commit for 802eb0c9-1686-44b1-9b44-2e7ccbfb0bee
- auto-commit for 01cf0ad9-7c0f-4d8e-a18b-68f8eccc2d16
- auto-commit for 9977aea9-77ec-41c1-a06e-4bfd1979ffb5
- auto-commit for 588d1ecd-c80e-4d21-9a9c-707d973db666
- auto-commit for 800d9c09-8b24-4ea3-b308-b1d090c1faa8
- auto-commit for cda2d81b-9092-462d-b118-f2e045b61948
- auto-commit for 6accae02-1659-4a6e-9840-e28055c882fc
- auto-commit for 1e183dae-818d-447f-9018-65e31337d7a3
- auto-commit for 3f1ee679-c69e-4cae-b11b-ed84b9394a72
- auto-commit for 5269a225-a8b2-4d1a-b7ce-1bc8bfddf681
- auto-commit for 84a98cc0-8a70-41a9-b0e1-448180b676c4
- auto-commit for 4ec9ee31-07dd-4e94-ae2e-ad3b9f7fc12c
- auto-commit for e920904a-774b-4564-af30-340f112a8855
- auto-commit for 9b04a3d7-7094-4d48-841d-d255d1d1e9b9
- auto-commit for 39d08377-295c-4ad6-89be-d4e5e3d7b2d9
- auto-commit for 6a75a66d-b1aa-4aad-9aae-70a4d7f905a5
- auto-commit for 8426efb2-8a93-4fb4-9d04-7edd0445be03
- auto-commit for 8be90fae-849b-4059-b39c-7f4e62de9e7b
- auto-commit for 87f9430d-1d37-46ba-8fab-8c9236b64250
- auto-commit for 877d3b5c-ce7f-4ddb-b668-2c689c6ef340
- auto-commit for ce636ed6-22fa-43db-b101-23588bf9bec2
- auto-commit for e61d95ea-47f0-434e-92c5-fe466e78e6f3
- auto-commit for 965bab17-e4b2-44f4-915a-1082b4ded5d7
- auto-commit for 121477de-68e6-46eb-b4bc-ed4885bf73b3
- auto-commit for 0ad4f229-7a3c-472d-97d6-44feead3d054
- auto-commit for ed73dc87-6f3f-435e-b444-94f0d698c785
- auto-commit for 1b1927db-b48b-409a-8b1c-b2d0751e2a38
- auto-commit for 43abd4d8-2a41-4c13-b183-dc7b736ba63e
- auto-commit for 64197907-1878-4802-893c-688115735c1e
- auto-commit for 084c8eaa-91ce-46c0-a109-5e46fe4112bd
- auto-commit for d14d07cb-1d83-4076-a829-1b85300ddb96
- auto-commit for 9832418e-74e2-492c-b499-bc5c5afd95f3
- auto-commit for 4e7e86fc-2b45-42a4-a81d-3011096f3497
- auto-commit for 932b6f93-e4ff-43d7-b7ca-3f09805309d9
- auto-commit for f3690b05-03f5-42ff-a982-a63daa05722e
- auto-commit for 656ce96f-71b7-4761-87dd-3858931be6d5
- auto-commit for 5ba1778e-3ad3-4e06-86fb-06a45a292184
- auto-commit for afe22675-44f1-45d2-9dfd-627609377489
- auto-commit for 026b4cb3-1a2f-4bc6-ab21-057135b82301
- auto-commit for 85482fcb-a543-43af-af61-b8f3a3b21e47
- auto-commit for 7a536230-0483-4192-8053-cba2e57a7a15
- auto-commit for d4df70d1-8755-4662-a6e6-e74c7ac5161e
- auto-commit for 916e0e6c-181c-413f-9361-b41896df324d
- auto-commit for 0f6c99ab-ee3a-43d7-94ea-e48da7650572
- auto-commit for aa326480-bf60-4c6d-ae87-f828f135425f
- auto-commit for ac56d2c0-5c76-424a-a275-a6e64c714693
- auto-commit for 022240ff-d135-47be-b982-cb38cb1eb8b0
- auto-commit for baa4dcb5-b519-4a4d-b49e-6c879394b58f
- auto-commit for 59f8d83c-f2f7-41bb-a47b-4980211a30eb
- auto-commit for 09fbd106-beb8-456f-a13b-57178ac21366
- auto-commit for acfd0025-6f90-4c94-bf4f-f04fe9271f4c
- auto-commit for 288b9bfe-1a63-4a84-96ea-937f5b39e92a
- auto-commit for 0a99ecd3-ad6a-453a-a2ef-cc0378a31b93
- auto-commit for c4679ceb-01ed-4c69-8c38-15297f89f346
- auto-commit for ca67c465-eeda-454b-b79e-8d1e407453bf
- auto-commit for 17934888-6663-4084-8c18-1ce3901c19e6
- auto-commit for 5820fa08-7ae9-4c20-a900-3b80278d7542
- auto-commit for 4712160b-908d-4177-a0b5-6a4903e719d5
- auto-commit for 3ad1765f-595c-404a-b9c1-5438ce389923
- auto-commit for ac2830ca-10cf-4ef0-850b-06d56e693932
- auto-commit for 834faf54-73eb-4308-af94-ef4b48fe77fb
- auto-commit for ebb6639d-dd0a-4d89-a464-b91f94fa1a7c
- auto-commit for 20b510c1-757d-40da-98d5-41ee633392c1
- auto-commit for 6f4917f5-40b2-4f3f-bd7f-b5749f1cd051
- auto-commit for 0eb7e1f5-0854-4b4f-94fc-5dd530ceefd0
- auto-commit for d5f1a0e1-8e87-4838-b916-ba18c19813e9
- auto-commit for 6eb02b01-e396-4f10-bb0a-ad6a24ab27b4
- auto-commit for 85ae4a81-85ef-47b0-8b3c-964d6f8cf8f8
- auto-commit for 46a4d2f8-7b75-4100-90c7-9e51d0ae6669
- auto-commit for b0c72605-e499-4f05-90a2-ba323a35f309
- auto-commit for 8f2c9a35-7773-471e-9b6b-6d55e9028c2c
- auto-commit for 09fde956-d5da-466e-9558-d595e54227da
- auto-commit for cd3b60bf-dfab-4f47-9f8d-dee4f02b1885
- auto-commit for 67e1d967-629e-4e0c-8ea1-d8cb9f176058
- auto-commit for e5e4ef03-18b4-44a8-821f-9cafb3334321
- auto-commit for a4b44d86-0964-4baa-8b7c-0ab6e754315f
- auto-commit for ed962cb5-9bd5-4266-b7e7-cdd81063428e
- auto-commit for 5386ef05-d2c1-4d83-924d-70eeb59e0620
- auto-commit for 1c4d6967-1261-493e-a56c-60a590b0e65e
- auto-commit for ca708073-b0ea-4fd4-b001-81baee9b27bc
- auto-commit for 3f23ce08-fa89-491b-8e8b-bc30b4f003c9
- auto-commit for df45870d-0e19-4838-990e-628c4214b939
- auto-commit for ccfb136f-7380-4d68-859b-681e9dda8a55
- auto-commit for 831b0fea-8a88-4263-b874-3576f7c2610b
- auto-commit for d38bdf72-99e3-43ea-8876-74f225f7bfa6
- auto-commit for 330da219-5552-464e-9286-e6d6aae9b0d6
- auto-commit for d2d86ca8-cd07-496a-8afe-d8cbbbb6ee15
- auto-commit for 550ef197-9a06-41cd-a885-34fc2600ea5a
- auto-commit for 6ebe5be9-9acb-40ea-8dd8-7f24ed5164ac
- auto-commit for 4f99ceb9-6212-48d8-8d6c-b9db6e8e7b57
- auto-commit for 344fc6b0-f8c2-461c-a49e-77a5c8648579
- auto-commit for 99d35861-486c-437d-b8c8-9e225774620d
- auto-commit for 88d433f4-997f-484f-bcce-609c368c6a2b
- auto-commit for 708294e6-aacb-44a6-912e-e16e3c015fd6
- auto-commit for c26ad314-dc78-44e1-b82c-03d5ce4339c2
- auto-commit for 53db3fa4-ae0e-4219-a37a-cf296c91e755
- auto-commit for d3708b79-bc28-4f03-871a-9a6fdb99e22d
- auto-commit for cffacc9b-b056-4e6c-88f9-aba15b575a3b
- auto-commit for 18ccb553-9132-40ce-adb9-abe333f3bd00
- auto-commit for cdec730d-df4b-4f02-a05b-d2c2b0946d43
- auto-commit for 7d877190-348a-4b81-baf8-dbbfbde6ac4d
- auto-commit for 81849472-9f7a-4c03-935f-8c6c023be3ec
- auto-commit for d8160d7b-7e7d-4e21-8946-348684bb2276
- auto-commit for 3b5abf61-c6d4-4750-8307-ec2de12913e4
- auto-commit for 5b287db7-cbec-4f03-bfba-eaced6012bc5
- auto-commit for dd02a861-16b9-44e7-b348-4844832c37fc
- auto-commit for ecbe9820-050b-4305-bedb-61ef787d2821
- auto-commit for c1542edb-4929-4312-8cc6-604a1061bdeb
- auto-commit for 68c47160-761e-4962-a491-cee675b27e9f
- auto-commit for f2130849-07e4-4d14-89c4-a7f544ff280f
- Initial commit

</details>

## v0.9 — 2026-08-25
- Release v0.9.

## v1.0.0
- Initial packaged release: jobs, service reports & PDF approvals, on‑site sign‑on,
  attendance, equipment/assets, incidents, clients & suppliers, document control,
  staff & training, notifications, and admin settings.
- Report delivery: choose related site photos/files as email attachments, optional
  automatic photo downscaling for large attachments, and a per‑report send history.
- Rejected reports can be corrected and re‑uploaded under the same report trail, with
  reviewers/managers notified automatically.
- Cloudflare Access SSO (Settings → Integrations) with password sign‑in fallback.
- Offline + online licence activation (Settings → Licence).
