# Crimson-Desert-Duo-FiveCard-Calculator
Odds calculator for Duo and Five-Card — the card gambling minigames in Crimson Desert.  
Input your hand and your opponents’ visible cards to instantly see win/loss probabilities and betting advice.

The user leumas152000 is the original creator of the app Crimson-Desert-Duo-Calculator-  
https://github.com/leumas152000/Crimson-Desert-Duo-Calculator-  
I have fixed some issues and added the other card game Five-Card.  
I think both calculators are working correctly now. Please let me know if you have any issues or suggestions.  
I have been using AI to help me with the code on this project.







# Changes made from the original


__New Feature: Five-Card Mode__  
A second game mode is now available via the tab bar at the top of the app. Five-Card uses its own distinct ruleset:

- Enter all 5 cards in your hand. The calculator finds every valid trio (three cards whose values sum to 10, 20, or 30) and evaluates the best 2-card hand from the remaining pair.  
- If no valid trio exists, your hand is marked as a Bust.  
- All valid groupings can be expanded to see every possible trio split, with the optimal one starred.  
- Odds are calculated via Monte Carlo simulation (6,000 samples) to handle the larger deck and hidden card space. Results are marked Estimated to reflect this.  
- Five-Card uses a 40-card deck (two copies of each card), and known cards are removed from the deck before simulation.  

__New Hand: Judge (3 + 7)__  
The Judge has been added to the Duo hand hierarchy at rank −2. It beats all regular point hands and standard pairs, but loses to Ten Pair, Superior Pair, and Prime Pair. It forces a rematch against Wardens and ties against another Judge.  

__Balance & Rule Changes__  
Warden vs. Pair — Previously always resulted in a rematch. The Warden's fallback value is now compared directly against the pair's fallback score, allowing for a decisive win or loss.  
High Warden — Removed the special case where high-ranking pairs (rank ≥ 79, i.e. pairs of 9s and 10s) could beat the High Warden outright. Only named premium hands (Prime Pair, Superior Pair, Ten Pair) now defeat it.   All other matchups remain a rematch.  
Executor vs. Judge — Executor's rank comparisons now correctly treat the Judge's effective value as 0, consistent with the Judge's position in the hierarchy.  

__Improvements__  
Opponent limit increased — The Duo calculator now supports up to 3 opponents, up from 2.  
Combined odds — When facing 2 or more opponents in Duo mode, the combined "beat all" odds calculation now supports the full 3-opponent scenario via recursive enumeration.
