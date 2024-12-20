This plugin allows your player to bet money or points to become a rich man or a naked guy.

## Dependency
[Economics](https://umod.org/plugins/economics)

## Permissions

- `lottery.canuse` -- Allows players to use the lottery
- `lottery.canconfig` -- Allows players to configure the lottery

## Chat Commands

- `/lot` -- Open the lottery GUI
- `/lot add` -- Add NPC you are looking to the list of NPCs
- `/lot remove` -- Remove NPC you are looking to the list of NPCs

## Configuration

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

## Server Rewards

* MinBetJackpot => Here you set the minimum bet required to be able to win the jackpot.
* Jackpot => How many points have the jackpot.
* JackpotMatch => Roll number match to win a jackpot.
* WinPoint => How many points does each match have (see [Economics](https://umod.org/plugins/economics) part).
* Match => roll match (see Economics part)
* MinBet => Minimum bet
* Enabled => Enable ServerRewards support

## Economics

* Jackpot => How many $ has the jackpot.
* JackpotMatch => Roll number match to win a jackpot.
* RollMinRange => Min roll range must be less than RollMaxRange
* RollMaxRange => Max roll rang must be superior or equal to RollMinRange
* WinRate => (see below part)

111x is the number the player rolls where "x" means a random number and the "1" after the double dot is the percent of the win rate.

For example, if a player places a bet of 100 with a multiplier of 4 and rolls 1111 he will win 100*(1/100)*4

The "-" " " are both bet multipliers.

The **Bet modifiers button** is here to put how much money you want to place in a bet.

The **place bet** button allows you to make the roll and get a chance to win.

The **`<< and >>`** arrow allows you to switch the win rate, this part is only for information.

## Human NPC

* Enabled => Turn NPCOnly option on/off (when true, the command is disabled)
* npcID => List of NPC you want to use to display UI

## User Interface

* BackgroundMainColor => Allows you to change the main background color and transparency
* BackgroundMainURL => Allows you to set image as background to the main UI(setting to "" will remove image)
* BackgroundWinColor => Allows you to change the win background color and transparency
* BackgroundWinURL => Allow you to set image as background to the win UI(setting to "" will remove image)
* anchorMin, anchorMax => Size and placement of the UI
