# Go Proverb Telegram Bot 🤖

A GitHub Actions-powered bot that automatically posts Go (the board game) proverbs to a Telegram channel on a schedule.

## Features

- 📅 **Scheduled posting**: Automatically posts proverbs twice a week (Monday & Thursday at 09:00 UTC)
- 🎮 **Manual triggering**: Can be manually triggered anytime via GitHub Actions
- 📝 **Proverb rotation**: Cycles through proverbs sequentially from a text file
- 🔄 **Auto-commit**: Automatically updates the proverbs file after each post
- 🌐 **Multi-language**: Supports proverbs in any language

## Setup Instructions

### 1. Repository Setup

1. **Fork or create** this repository
2. **Add your proverbs** to `proverbs.txt` file (one proverb per line)

### 2. Telegram Bot Setup

1. **Create a Telegram Bot**:
   - Message `@BotFather` on Telegram
   - Send `/newbot` command
   - Follow instructions to get your bot token

2. **Get Chat ID**:
   - Add your bot to your Telegram group/channel
   - Send a message in the chat
   - Visit: `https://api.telegram.org/bot<YOUR_BOT_TOKEN>/getUpdates`
   - Find the `chat.id` in the response

### 3. GitHub Secrets Configuration

Go to your repository **Settings → Secrets and variables → Actions** and add these secrets:

| Secret Name | Value | Description |
|-------------|-------|-------------|
| `TG_TOKEN` | `123456:ABC-DEF1234ghIkl-zyx57W2v1u123ew11` | Your Telegram bot token |
| `CHAT_ID` | `-1001234567890` | Your Telegram chat/channel ID |

### 4. Repository Permissions

Go to **Settings → Actions → General** and set:

- **Workflow permissions**: "Read and write permissions"
- **Allow GitHub Actions to create and approve pull requests**: Optional (not required)

## File Structure
