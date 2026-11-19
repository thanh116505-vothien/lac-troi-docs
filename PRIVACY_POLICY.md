# Privacy Policy for Lạc Trôi

Last updated: November 20, 2026

Application ID: `1572430859955474503`  
Operator: VoThien  
Contact on Discord: `vothien0143`

## 1. What the bot does

Lạc Trôi helps a Vietnamese Discord community discover game translation posts, submit and track translation requests, manage registered bot accounts, and use activity points and virtual items. It also supports optional donation receipts and administrator mention alerts.

Users initiate registration and personal workflows through one-to-one direct messages and buttons. Registration uses Discord identity; the bot does not ask users to create a password. Scheduled game suggestions are posted in a configured server channel. The current version does not send periodic game recommendation DMs to a subscriber list.

## 2. Data processed and why

### Discord identity and access information

The bot processes Discord user IDs, usernames/display names, guild and channel IDs, roles, and membership information. It uses server permissions, private-thread membership, and configured bot account levels to determine available features and catalog results. Role and membership events invalidate cached permission information. Certain administrators and translators have additional access under the bot's account-level rules.

Registered account IDs, usernames, account levels, registration status, and registration timestamps are stored in a local SQLite database. Role/member objects and permission caches are used in application memory.

### Configured game catalog and searches

Administrators select the server channels and forums used as catalog sources. The bot reads thread titles and original post links. In supported text channels, it can use the first line of a member-authored message as an entry title. It reads image attachments and image embeds from source posts and, when needed, early thread messages to display an image in a game card.

Catalog metadata, image URLs, and search queries are processed in memory. Search query text is not intentionally written to a search-history table. The points system does store limited records of game IDs explored by a registered user on a given day. Donation-receipt channels are excluded from catalog sources.

The bot receives Discord message events and uses a bounded message cache. It does not maintain a general archive of server conversations.

### Translation requests and community features

The bot stores request/thread IDs, requester and translator IDs, requested game titles, processing status, and completion-notification progress. User-submitted request text, links, and images are used to create the requested forum post. Upload images are temporarily saved on disk while a posting session is active and are removed when that session is completed, cancelled, or expires during normal operation.

Activity points and virtual items require stored balances, point events and dates, explored game IDs, inventory records, game titles in item orders, order status, and the user IDs involved. Points are not a cash balance. Leaderboards, forum requests, and completed actions may be visible to other Discord users through the bot's corresponding features.

### Optional donations and receipt images

Donation-recipient profiles contain the recipient's display/account name, account number or payment reference, QR image, Discord username, and configured acknowledgement channel. These details are displayed when a user chooses that recipient.

Users may voluntarily submit a receipt image in a DM after choosing a recipient. Such an image can contain personal or financial details. The bot downloads it to local storage for validation and image processing. Where Tesseract is installed, OCR is performed locally. The bot attempts to obscure receipt details before posting the processed image and a donor acknowledgement in the selected recipient's configured server channel. Automated redaction can make mistakes, so users should obscure information they do not want shared before submitting an image.

The original receipt file is removed from active application storage after successful publication or processing rejection. Images awaiting delivery can remain queued through retries; there is no guaranteed 30-day expiry for every pending receipt. Minimal metadata, including donor ID, recipient key, timestamps, filename/hash, and status, can remain for acknowledgement, duplicate detection, and operational records. Copies posted on Discord have a separate lifecycle.

The bot does not execute bank transfers or request a banking password, OTP, or payment-card credential.

### Optional mention alerts and abuse prevention

Registered bot administrators can enable or disable their own mention alerts using the administrator controls or the DM messages `bật mention` and `tắt mention`. An enabled alert forwards the mentioning message's available text snippet, author/channel information, and original-message link to that administrator, subject to the implemented access checks.

Rate limiting and abuse prevention process user IDs, action times, strike counts, lock status, and reasons. Diagnostic logs can include Discord IDs, processing errors, and error context. The application log is rotated by size; hosting-system logs have a separately administered lifecycle.

## 3. Storage, retention, and security

Persistent bot data is stored in SQLite and local files on the operator's host. Some operational records can remain longer than 30 days. The current application does not enforce automatic 30-day deletion for all accounts, requests, point records, orders, receipt metadata, or pending files.

The bot attempts to delete its own DM messages after the configured cleanup interval when that feature is enabled. Cleanup can be delayed by outages or Discord permissions/API errors. It does not delete the user's incoming DM messages, and it does not replace deletion of database records.

The current application does not implement its own encryption of the SQLite database or stored upload/receipt files. This policy does not claim that hosting volumes or backups are encrypted; that must be separately established by the operator. Older manual backups, if present, require separate handling when processing a deletion request.

## 4. Disclosure and external services

The bot uses Discord's API and media infrastructure to receive messages and deliver results. Content intentionally posted through a feature is visible according to the destination channel or DM. Donation acknowledgements can include the donor's Discord identity and a processed receipt. Translation requests can include the requester's Discord identity and the content they chose to submit.

The current application does not use message data to train AI or machine-learning models, sell data, or provide it to advertising/data-broker services. Receipt OCR, when available, runs locally rather than through an external OCR API. External links in catalog entries lead to independently operated services with their own privacy practices.

## 5. Choices and deletion requests

Users can choose not to register, stop initiating personal bot workflows, cancel an active input session with `hủy`, and avoid optional donation uploads. Eligible administrators can disable their own mention notifications. Administrators can remove channels from the configured catalog sources or remove the bot to stop its future access to their server.

There is currently no automatic per-author exclusion setting for messages in an indexed catalog channel and no automated command that erases all stored account data. Stopping use or removing the bot does not automatically erase all existing records or content already posted on Discord.

To request deletion or discuss a catalog/privacy concern, send a Discord DM to **`vothien0143`**. Include your Discord user ID, identify Lạc Trôi with application ID **`1572430859955474503`**, and specify the records or content concerned. Requests are handled manually by the operator. Identity or scope may need to be confirmed before changing records. Records connected to other users, shared completed transactions, abuse prevention, existing Discord posts, and older backups may require separate review and handling; the operator will explain any limitations rather than promise automatic or immediate erasure.

## 6. Changes and contact

The operator updates this policy when the bot's data practices change. Questions and requests can be sent to **`vothien0143`** on Discord.
