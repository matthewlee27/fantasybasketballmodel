# **Background**

I am playing in my Fantasy Basketball league with little knowledge of basketball. However, I am a Statistics major at the very lovely University of Chicago, and I do really like the subject, so I’m going to undergo building a statistical model to inform my strategy for when to lock players\! If you guys are unfamiliar with the Sleeper Fantasy lock-in mode rules, you can read them here: [ta-da](https://support.sleeper.com/en/articles/6522833-lock-in-mode-details)

# **Setup**

On every team, and on my team, there are 5 types of positions, and 9 slots for players.

### **The 9 slots**

| Slot | Eligible Positions |
| :---- | :---- |
| PG | PG |
| SG | SG |
| PF | PF |
| SF | SF |
| C | C |
| G | PG, SG |
| F | PF, SF |
| UTIL | PG, SG, PF, SF, C |
| UTIL | PG, SG, PF, SF, C |

### **Players**

Each player *i* has the following attributes:

* One or more positions  
* Ni games a week  
* An expected number E\[Pi, j\] points at game j  
* We assume for simplicity, and from sports precedent, that each   
  ${}$


\*But that this expected number of points/game can have some kind of unknown error, and that across the course of the season I want my model to uncover this error and give me a better version of this but anyways that’s somewhere down the line

For instance, we might have the following player Lebron James, who is eligible for three slots\! PG, SG, and SF positions:

| E\[PJames, 1\] | E\[PJames, 2\] | E\[PJames, 3\] | E\[PJames, 4\] |
| :---- | :---- | :---- | :---- |
| 31.96 | 35.43 | 35.33 | 32.41 |

### **Motivating / Simple Case**

Let’s say we have two players, Devin Booker and Ja Morant, who are the only two eligible players that a team has for shooting guard; yes unfortunately I did not draft carefully.

*Devin Booker*

| E\[PBooker, 1\] | E\[PBooker, 2\] |
| :---- | :---- |
| 40.1 | 40.2 |

*Ja Morant*

| E\[PBooker, 1\] | E\[PBooker, 2\] |
| :---- | :---- |
| 29.2 | 29.2 |

Our dilemma is: whether we should lock the players after their day one performances, and how should we decide that? This is probably dependent on how everyone else is contributing, but for simplicity let’s just treat this like an isolated case.

(did you like this? read the full documentation of the progress in the project overview file)
