### 🚀 v1.1.0 — Security & Stability Overhaul

This update significantly improves the bot’s moderation pipeline, security engine, and behavioral tracking reliability. Core systems have been refactored for consistency, stability, and easier future expansion.

---

## 🛡️ Security System Improvements
- Unified message dispatch system to prevent duplicate processing across security-related components
- Refactored link scanning pipeline with clearer and more reliable risk scoring
- Improved Intel tracking system for persistent user-based threat scoring
- Added external event hook support for cross-system integration (e.g., CAPTCHA and future modules)
- Enhanced defense state transitions (NORMAL / ELEVATED / LOCKDOWN) for consistent adaptive behavior

---

## ⚖️ Automated Enforcement System
- Fully implemented strike-based escalation system for link violations
- Automatic punishment scaling based on user strike history
  - First offense → short timeout
  - Repeat offenses → progressively longer timeouts
  - High severity → extended cooldown / escalation state
- Immediate hard-stop enforcement for blacklisted domains
- Consistent integration between risk scoring and punishment execution

---

## 🧑‍⚖️ Moderator Decision System (NEW)
- Added interactive moderation review panel for security incidents
- Each flagged event now generates an embed with an action dropdown
- Moderators can directly choose:
  - Ban user
  - Softban (temporary ban with automatic unban)
  - No action required
- One-click enforcement reduces response time and removes need for manual command handling
- Views automatically disable after a single selection to prevent duplicate actions

---

## 🔗 Link Protection Enhancements
- Improved URL extraction and domain parsing accuracy
- Strengthened VirusTotal integration with better error handling and fallback behavior
- Smarter safe-domain recognition system to reduce false positives
- More consistent enforcement thresholds across all defense levels

---

## 👥 Join & Behavior Monitoring
- Improved join-based risk evaluation using Intel scoring
- More reliable timeout handling for flagged new members
- Expanded and more consistent incident tracking (joins, bans, warnings, timeouts, link removals)
- Improved logging accuracy for behavioral violations

---

## 🧠 CAPTCHA & External System Integration
- Added external risk event interface for other cogs to influence security scoring
- CAPTCHA verification outcomes now dynamically affect user trust and risk levels
- Improved groundwork for modular security extensions

---

## 🧹 Cleanup & Refactors
- Removed outdated Twitch integration from Watch system
- Simplified metrics tracking for Discord-only environments
- Standardized moderation and message tracking logic across systems
- Reduced redundant JSON writes and improved config handling consistency

---

## ⚙️ Lockdown System
- Improved snapshot and restore reliability for lockdown mode
- More consistent permission restoration after lockdown ends
- Better integration readiness with external triggers and escalation systems

---

## 🧪 Stability Improvements
- Reduced duplicate event handling across multiple cogs
- Improved async safety for logging and moderation actions
- Strengthened error handling for timeouts, deletions, bans, and API failures
- More defensive handling of missing or partial configuration entries

---

## ⚠️ Notes
- This update includes structural refactors; behavioral systems may take a short period to stabilize as user metrics rebuild
- No configuration migration is required when upgrading from previous versions

**For further support and updates, join the support server, [here](https://discord.gg/dV6q6pJCUK)!**