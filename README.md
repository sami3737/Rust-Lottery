
# Lottery Plugin

This plugin allows players to bet money or points to become a rich man or a naked guy.

## Dependencies
- [Economics](https://umod.org/plugins/economics)

## Permissions

- `lottery.canuse` — Allows players to use the lottery.
- `lottery.canconfig` — Allows players to configure the lottery.

## Chat Commands

- `/lot` — Open the lottery GUI.
- `/lot add` — Add an NPC to the list of NPCs.
- `/lot remove` — Remove an NPC from the list of NPCs.

## Configuration

### Global Configuration
```json
{
  "Global": {
    "Jackpot": 50000,
    "JackpotMatch": 1058,
    "RollMaxRange": 9999,
    "RollMinRange": 9998,
    "WinRate": {
      "111x": 1,
      "222x": 10,
      "333x": 50,
      "444x": 10,
      "555x": 75,
      "666x": 5,
      "777x": 75,
      "888x": 56,
      "999x": 420,
      "99x9": 52,
      "99xx": 86,
      "9x99": 57,
      "9xxx": 86,
      "x999": 85
    }
  },
  "HumanNPC": {
    "Enabled": false,
    "npcID": [
      "577616100"
    ]
  },
  "ServerRewards": {
    "Enabled": true,
    "Jackpot": 10,
    "JackpotMatch": 1869,
    "Match": [
      "111x",
      "222x",
      "333x",
      "444x",
      "555x",
      "666x",
      "777x",
      "888x",
      "999x",
      "99x9",
      "9x99",
      "x999",
      "99xx",
      "9xxx"
    ],
    "MinBet": 1,
    "MinBetJackpot": 100,
    "WinPoint": {
      "Match1Number": 1,
      "Match2Number": 2,
      "Match3Number": 3,
      "Match4Number": 4
    }
  },
  "UI": {
    "BackgroundMainColor": "0.1 0.1 0.1 1",
    "BackgroundMainURL": "http://wac.450f.edgecastcdn.net/80450F/kool1079.com/files/2016/05/RS2397_126989085.jpg",
    "BackgroundWinColor": "0.1 0.1 0.1 1",
    "BackgroundWinURL": "http://wac.450f.edgecastcdn.net/80450F/kool1079.com/files/2016/05/RS2397_126989085.jpg"
  }
}
```

### Configuration Breakdown

#### **Global Settings**
- `Jackpot` — The amount of points in the jackpot.
- `JackpotMatch` — The roll number that must match to win the jackpot.
- `RollMinRange` — The minimum roll range (must be less than `RollMaxRange`).
- `RollMaxRange` — The maximum roll range (must be greater than or equal to `RollMinRange`).
- `WinRate` — The win rates for various roll matches. Example: `"111x": 1` means a 1% chance of winning if "111x" is rolled.

#### **Human NPC Configuration**
- `Enabled` — Enable or disable NPC-only mode.
- `npcID` — List of NPCs you want to use to display the UI.

#### **Server Rewards**
- `MinBetJackpot` — Minimum bet required to be eligible for the jackpot.
- `Jackpot` — The amount of points in the jackpot.
- `JackpotMatch` — Roll number match to win the jackpot.
- `WinPoint` — Points awarded for matching rolls (see the [Economics](https://umod.org/plugins/economics) plugin).
- `Match` — List of roll matches.
- `MinBet` — The minimum bet amount.
- `Enabled` — Enable ServerRewards support.

#### **UI Customization**
- `BackgroundMainColor` — Background color and transparency for the main UI.
- `BackgroundMainURL` — Set an image as the background for the main UI (leave blank to remove the image).
- `BackgroundWinColor` — Background color and transparency for the win UI.
- `BackgroundWinURL` — Set an image as the background for the win UI (leave blank to remove the image).
- `anchorMin`, `anchorMax` — Controls the size and placement of the UI.

## Gameplay

Players can place bets using the lottery system. They will either win or lose based on the win rates and roll results. The **Bet Modifiers** button allows you to adjust how much money you want to place on a bet.

The **Place Bet** button allows the player to make the roll and get a chance to win.

The **`<< and >>`** arrows allow you to switch between different win rates. This is for information only.

### Example Win Calculation
If a player places a bet of 100 with a multiplier of 4 and rolls `1111`, the winnings would be calculated as:

```
100 * (1 / 100) * 4 = 4 points/money
```

## Human NPC

- **Enabled**: Turns on/off the NPC-only mode.
- **npcID**: List of NPCs you want to use to display the lottery UI.

## User Interface

- `BackgroundMainColor`: Controls the main background's color and transparency.
- `BackgroundMainURL`: Set an image URL for the main background (set to `""` to remove).
- `BackgroundWinColor`: Controls the win screen background color and transparency.
- `BackgroundWinURL`: Set an image URL for the win screen (set to `""` to remove).

---
