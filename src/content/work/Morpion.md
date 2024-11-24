---
title: Ultimate Tic Tac Toe
publishDate: 2022-05-06 00:00:00
img: /assets/TicTacToe.jpg
img_alt: Image manipulation
description: |
  I used C# to manipulate an image and generate a QR code from a sentence.
tags:
  - C#
  - Windows Forms
  - Qr Code
---

## Subject

> What is this all about ?

This project was about creating an AI that I had to train to choose the best move to win a game of tic-tac-toe. But how did I do it? Well, I had to implement the famous minimax algorithm, which allowed me to find the best possible move. Here is the result below, and I created the graphical interface using pygame.



<iframe src="/assets/TicTacToeGame2.mp4" width="100%" height="360" frameborder="0" allowfullscreen></iframe>


However, it wasn't over yet. My goal was to apply this concept to <a href="https://en.wikipedia.org/wiki/Ultimate_tic-tac-toe">Ultimate Tic Tac Toe</a>.

The challenge was that, for this game, reaching the final state was not possible as the possibilities tree was way too large. Additionally, time played a role in our final score because we had to compete with all the AIs in the class. We needed to balance speed and a good result to achieve the highest score. Il a donc fallu chercher la meilleur heuristic possible pour ce projet

That's why I decided to implement alpha-beta pruning with memoization, a more advanced approach than minimax. Here's an example in the terminal:
<div style="text-align: center;">
  <img src="/assets/ultimatetictactoe.jpg" alt="Ultimate tic tac toe" />
</div>

