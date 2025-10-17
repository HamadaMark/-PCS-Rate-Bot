cat > README.md << 'EOF'
# 🤖 ProCrypto Signals Activity Tracker Bot

Advanced Telegram bot for tracking user contributions and managing community engagement in ProCrypto Signals.

---

## 📊 Overview

This bot automatically tracks user activity, assigns ratings, and manages community participation through an intelligent tier-based system.

## ✨ Key Features

### 🎯 Activity Tracking
- **Message tracking** - Every contribution is recorded
- **Point system** - Quality + Quantity = Higher rating
- **Rating scale** - 0-10 based on total contributions
- **Tier progression** - Beginner → Expert (5 tiers)

### 👥 User Management
- **8 Sectors** - Trader, Investor, TA Expert, Alerter, Scalper, FA Expert, Watcher, Newbie
- **VIP whitelist** - Special users exempt from tracking
- **Auto-kick system** - 24h deadline to set sector
- **Warning system** - Low rating, no sector, inactivity alerts

### 🔄 API Integration
- **Bidirectional sync** - Bot ↔️ Website API
- **Pagination support** - Handles large user datasets
- **Duplicate prevention** - Smart username normalization
- **Real-time updates** - Auto-sync every 5 minutes

### 🛡️ Security & Admin
- **Admin-only commands** - Restricted bot management
- **Invite link generation** - One-time, expiring links
- **Bot ban system** - 48h timeout for repeat violations

### 📈 Engagement Features
- **Daily trading quotes** - Motivational messages
- **Leaderboard** - Top 10 contributors
- **Personal stats** - /me command for user insights
- **Community stats** - Overall group analytics

---

## 🎮 User Commands

| Command | Description |
|---------|-------------|
| `/start` | Welcome message |
| `/setsector` | Choose your role (REQUIRED within 24h) |
| `/me` | View your profile & stats |
| `/top` | Top 10 contributors leaderboard |
| `/stats` | Community overview |
| `/help` | List all commands |

---

## 🔧 Admin Commands

**Restricted to authorized admins only:**

| Command | Description |
|---------|-------------|
| `/api_status` | Check API connection |
| `/force_sync` | Manual bidirectional sync |
| `/sync_diagnostic` | Detailed sync analysis |
| `/check_duplicates` | Find duplicate users |
| `/fix_duplicates` | Merge duplicate entries |
| `/check_pending_kicks` | View users pending removal |
| `/force_kick_check` | Run kick check immediately |
| `/create_invite` | Generate invite link |
| `/whitelist_add @user` | Add to VIP whitelist |
| `/whitelist_remove @user` | Remove from whitelist |
| `/whitelist_list` | Show all whitelisted users |

---

## 📋 User Sectors

| Sector | Emoji | Role |
|--------|-------|------|
| Trader | 📈 | Share trading insights & tips |
| Alerter | 🔔 | Share market sentiment & alerts |
| Investor | 💰 | Share investment opportunities |
| Watcher | 👁️ | Observe and learn |
| Scalper | ⚡ | Share quick profit opportunities |
| TA Expert | 📊 | Provide technical analysis |
| FA Expert | 📚 | Share fundamental analysis |
| Newbie | 🌱 | Learn and share understanding |

---

## 🎯 Rating System

### Tier Progression
- **Beginner** (0-19 messages) - 0.20 points/message
- **Active** (20-49 messages) - 0.30 points/message
- **Contributor** (50-99 messages) - 0.40 points/message
- **Veteran** (100-199 messages) - 0.50 points/message
- **Expert** (200+ messages) - 0.60 points/message

### Quality Multipliers
- Short message (<10 chars): 0.5x
- Normal (10-100 chars): 1.0x
- Detailed (100-500 chars): 1.5x
- Comprehensive (500+ chars): 2.0x

---

## ⚠️ Rules & Enforcement

### New User Requirements
- ⏰ Set sector within **24 hours** of joining
- 1st violation: Removed (can rejoin)
- 2nd violation: Removed + **48h bot ban**

### Warning System
- **Low rating warning** - Below 5.0 with 50+ messages
- **No sector warning** - After 3 days without sector
- **Inactivity warning** - After 7 days of no messages

---

## 🔄 Automated Jobs

- **Auto-sync** - Every 5 minutes (API ↔️ Bot)
- **Daily quotes** - Every day at 9:00 AM
- **Warning checks** - Every hour
- **Kick checks** - Every 30 minutes

---

## 💻 Technical Stack

- **Language:** Python 3.8+
- **Framework:** python-telegram-bot 20.7
- **API:** Requests library
- **Storage:** JSON (local)
- **Deployment:** Systemd service (auto-restart)
- **Server:** Ubuntu 22.04 LTS

---

## 📦 Dependencies

- `python-telegram-bot==20.7`
- `requests==2.31.0`
- `python-dotenv==1.0.0`

---

## 🚀 Deployment

Bot runs 24/7 as systemd service with:
- ✅ Auto-start on boot
- ✅ Auto-restart on crash
- ✅ Persistent background operation

---

## 📊 Statistics

- **Active tracking** since October 2025
- **Multi-sector system** - 8 roles
- **VIP members** - 5 whitelisted users
- **Auto-moderation** enabled

---

## 🔐 Privacy & Security

- **Private repository** - Code not publicly accessible
- **Admin restrictions** - Only authorized users can manage
- **API authentication** - Token-based security
- **Data protection** - Sensitive files excluded from version control

---

## 📞 Support

For bot issues or questions, contact: **@HamadaMark**

---

## 📄 License

**Private & Confidential** - ProCrypto Signals Community

All rights reserved. This bot is proprietary software developed exclusively for ProCrypto Signals.

---

**Last Updated:** October 2025
EOF
