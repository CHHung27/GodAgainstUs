# GodAgainstUs
Fun game inspired by the L4D games

Resources:
1) https://forums.unrealengine.com/t/design-structure-of-high-level-director-commander-ai/389528
2) https://developer.valvesoftware.com/wiki/L4D2_Director_Scripts
3) https://left4dead.fandom.com/wiki/The_Director

Ai Director System:
float intensity                          // goes up when player kills, player hurt, player close to zombies
int maxNumberOfZombies                   // default = 20; can go up depending on level
float difficultyMultiplyer               // default = 1.0; goes up by 0.1 per level entered. multiplier affects zombie attack and health values
array currentPhase = {1, 2, 3}                  // phase 1 = rising. phase 2 = peak. phase 3 = relax.

float weights -> for ZombieNum, BossNum, playerHealth, playerItem
Difficulty = W1 * ZombieNum + W2 * BossNum - W3 * playerHealth - W4 * playerItem             // WIP
