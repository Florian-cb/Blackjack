# blackjack
 
Overview

This program simulates a simplified version of Blackjack. The game flow follows traditional rules, where the player is initially dealt two cards and the dealer starts with one card visible and one hidden. The game then alternates between the player’s actions (hit or stand) and the dealer’s turn.

Initial Setup

Random and Scanner Objects - The code initializes a Random object to simulate card drawing and a Scanner to capture user input.

Game Loop - A loop continuously runs, prompting the player with options to start a new game, return to the main menu, or quit.

Card Drawing and Hand Calculation

Card Generation - The drawCard function randomly selects a card number (1–13) and a suit (♠, ♥, ♦, ♣). It returns:
  An Ace ("A") if the card is 1.
  A face card ("J", "Q", or "K") if the card is 11, 12, or 13 respectively.
  Otherwise, it returns the number along with the suit.
  
Hand Value Calculation - The calculateHandValue function computes the total value of a hand:
  Face cards (J, Q, K) are each worth 10.
  Aces are initially counted as 1, but later adjusted to 11 if it benefits the hand (without causing a bust).
  Number cards contribute their face value.
  
Game Start

Dealing Cards: When the player chooses to play (by pressing "P"), two cards are dealt for the player and two for the dealer.
Dealer’s Second Card: Although two cards are generated for the dealer, the second card remains hidden at first (displayed as "??") to mimic the traditional rules where the dealer’s second card is face down.

Player’s Turn

Decision Loop - The player sees their hand and the dealer’s visible card. They are repeatedly prompted to either:
  Hit - Draw another card, update the hand total, and check for a bust (exceeding 21).
    If the player's hand exceeds 21, the game immediately ends with the player losing.
  Stand - End their turn.

Input Handling - The program validates the player’s input, prompting for a valid option if an unrecognized input is entered. The player can also quit the game at any time by pressing "Q".

Dealer’s Turn

Revealing the Hidden Card - Once the player stands, the dealer’s hidden card is revealed.
Dealer’s Drawing Logic - The dealerTurn function makes the dealer draw additional cards until their hand value reaches at least 17:
  Each new card is drawn, added to the dealer’s hand, and the hand total is recalculated.
  A message is printed each time the dealer draws a card.

Determining the Outcome

Final Comparison - After both turns are complete:
  The player’s and dealer’s hand totals are compared.
  If the dealer busts (exceeds 21) or the player’s hand is higher than the dealer’s, the player wins.
  If the dealer’s total is higher than the player’s, the player loses.
  If both totals are equal, the game ends in a tie.

--- Code in Action ---

Game Stimulation 1 - Player Wins

<img width="1077" alt="Screenshot 2025-04-08 at 2 56 37 PM" src="https://github.com/user-attachments/assets/b9ab6ec0-2578-4dcf-aa7e-2b1e95384b82" />

Game Stimulation 2 - Dealer Wins

<img width="1077" alt="Screenshot 2025-04-08 at 3 00 49 PM" src="https://github.com/user-attachments/assets/f8751203-f437-4af0-8fc9-dce4733d3bf0" />

Game Stimulation 3 - Player Busts

<img width="1077" alt="Screenshot 2025-04-08 at 3 05 48 PM" src="https://github.com/user-attachments/assets/8f5d3e1e-6a66-43bd-ad27-4a498581ef2b" />

Game Stimulation 4 - Dealer Busts

<img width="1077" alt="Screenshot 2025-04-08 at 3 06 03 PM" src="https://github.com/user-attachments/assets/d0e6959d-c3e6-4c06-90cf-f671bd93e21f" />

Game Stimulation 5 - It's a tie

<img width="1077" alt="Screenshot 2025-04-08 at 2 53 22 PM" src="https://github.com/user-attachments/assets/9e914dd9-6f5d-4734-a345-8e8146fe0d8e" />


