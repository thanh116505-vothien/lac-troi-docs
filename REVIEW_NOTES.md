# Notes for publishing the updated privacy policy

This is a local draft based on the current `bot.py`, `community.py`, and project README. It has not replaced the public GitHub file.

The existing public policy was checked while signed out on November 20, 2026. It still describes removed slash commands and periodic recommendation DMs and omits current registration, community-point/order, and donation-receipt processing.

Before publishing, the operator should confirm that the deployed VPS uses the same version, that the contact account can receive deletion requests, and that the storage/backup description reflects the actual host. The draft explicitly avoids claiming verified encryption at rest or universal automatic deletion within 30 days.

Replace the content of `PRIVACY_POLICY.md` in the public repository with the reviewed draft. The existing URL can remain the same:

https://github.com/thanh116505-vothien/lac-troi-docs/blob/main/PRIVACY_POLICY.md

For the Developer Portal field asking where the policy is published, use:

> The privacy policy is published in a public GitHub repository and can be viewed without signing in or joining the Discord server.

There is no verified privacy-policy link in the current bot source or menu, so do not claim that users can already open it through a bot command or profile link.
