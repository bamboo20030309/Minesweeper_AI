# Minesweeper_AI
我寫了一個模擬遊戲的演算法，來訓練一個CNN模型，讓他學會踩地雷。

Minesweeper_Game.ipynb 是遊戲展示的code，如要使用請更改當中呼叫模型的路徑。
![image](https://github.com/user-attachments/assets/4719d9d7-3f2a-4c63-8e08-15cbd9a3a0cc)
此為高級模式成功例子的展示圖

Minesweeper_AI_CNN.ipynb 是主要模型訓練的code，裡面包含遊戲本身的class、模擬遊戲的演算法、資料增強、模型訓練、模型測試。

演算法已可解決一些簡單的高級邏輯，但困難的高級邏輯則無法，我透過這模擬遊戲的演算法訓練出來的模型在Beginner mode已經有93%勝率，由於檔案過大無法放上來，但是如果要訓練出相同的模型的話，請用演算法模擬50000局遊戲產生出的資料集，切記不要做資料增強，直接拿去模型訓練，batch_size=2048、epochs=50，丟下去給他跑，約一小時後就可以測試了，模型測試中有 可顯示模型機率高低的漸層機率圖 可以讓你從中觀察模型的成效。
![image](https://github.com/user-attachments/assets/6a9b62cf-e6f3-4db1-bd77-3f784ee15e43)

製作過程的投影片報告https://www.canva.com/design/DAGaxg03trA/9zOHUqB6ehBDixvazkCyyg/view?utm_content=DAGaxg03trA&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=hbe834dc513

模型結構參考 https://github.com/sdlee94/Minesweeper-AI-Reinforcement-Learning/blob/master/README.md

一些函數參數的調整：
Print_board = -1 只印出失敗的最後一步
Print_board =  0 完全不輸出
Print_board =  1 印出每一步
Print_board >  1 印出更多過程 (debug)

first_step = 0 遊戲的第一步可能包含地雷
first_step = 1 遊戲的第一步不可能包含地雷
first_step = 2 遊戲的第一步一定是0 (盡可能的好開局)
