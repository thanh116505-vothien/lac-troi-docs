# Privacy Policy for Lạc Trôi~,~

**Effective Date:** November 18, 2026  
**Developer:** VoThien (thanh116505-vothien)  
**Application Name:** Lạc Trôi~,~

---

## 1. Introduction
This Privacy Policy explains how the Discord bot **Lạc Trôi~,~** ("the Bot"), created and operated by **VoThien**, collects, uses, processes, and protects user data and interactions. By using the Bot or inviting it to your Discord server, you agree to the practices outlined in this policy.

---

## 2. Information We Collect and Process
The Bot is designed with a strict privacy-first principle. To provide its core features, the Bot processes only the following data:

### a. Opt-in Mention Notifications (DM Alerts)
- **Data processed:** User IDs, author display names, channel names, and real-time message snippet snippets containing mentions.
- **Purpose:** When a user explicitly opts in using the `/dangky` command, their Discord User ID is stored in a local database (`dm_subscribers`). When someone mentions that user in a server channel, the Bot delivers a private Direct Message (DM) alert with a link jumping directly to the message.
- **Opt-out:** Users can cancel anytime using `/huydangky`, which immediately removes their User ID from the database.

### b. Scheduled & On-Demand Game Recommendations
- **Data processed:** User IDs and publicly available forum/game thread titles.
- **Purpose:** Users who opt in via `/dangkygoiy` have their User ID stored in `suggest_subscribers` to receive 5 random game recommendations via 1-on-1 private DM every 3 hours. On-demand suggestions (`/goiy`) do not require subscription.
- **Opt-out:** Users can turn off recommendations anytime using `/huygoiy`.

### c. Watched Channels (`watched_channels`)
- **Data processed:** Server (Guild) IDs and Channel IDs.
- **Purpose:** Server administrators use `/dangkykenh` to select forum or game channels as sources for recommendations. The Bot reads thread titles and URLs in memory to provide game recommendations without modifying or reopening archived threads.

### d. In-Memory Game Search
- **Data processed:** Search query keywords entered by users in private DMs.
- **Purpose:** Queries are processed in runtime memory using fuzzy search and acronym resolution to return relevant game threads. Search queries are not written to disk or permanent databases.

### e. Automated DM Self-Cleanup
- **Protection:** All recommendation and notification messages sent by the Bot to users via 1-on-1 DMs are scheduled to automatically delete themselves after a configurable time window (default 3 hours) to keep user direct message boxes clean and clutter-free.

### f. Anti-Spam Protection
- **Data processed:** User IDs and timestamp of command execution.
- **Purpose:** Temporary rate-limiting records (`spam_locks`) are maintained to prevent bot abuse, denial of service, and spam attacks.

---

## 3. Data We Do NOT Collect
- We **do not** collect, store, or log general chat message histories or private user conversations.
- We **do not** collect personal information such as real names, passwords, email addresses, IP addresses, or payment credentials.
- We **do not** sell, trade, rent, or share any user data with external advertisers, brokers, or third parties.

---

## 4. Data Storage and Security
- All user preferences and channel configurations are stored exclusively in a secure, local SQLite database (`bot_data.db`) on a private host server.
- No data is transmitted to external cloud databases, analytics providers, or unauthenticated remote endpoints.

---

## 5. User Rights and Data Deletion
Users retain full control over their data at all times:
- Use `/huydangky` to immediately remove your User ID from mention notifications.
- Use `/huygoiy` to immediately remove your User ID from periodic game recommendations.
- Server administrators can remove indexed channels anytime using `/huydangkykenh` or by removing the Bot from their server.
- You can contact the developer directly to request complete manual deletion of any remaining cached preferences.

---

## 6. Contact Information
If you have any questions, concerns, or requests regarding this Privacy Policy, please contact:
- **Developer:** VoThien
- **Discord Tag / Username:** `vothien0143`
- **GitHub:** [https://github.com/thanh116505-vothien](https://github.com/thanh116505-vothien)
