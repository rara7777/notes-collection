# Data Structures

## Arrays (陣列)
是由相同類型的元素 (element) 的集合所組成的資料結構，儲存於一塊連續的記憶體，可藉由元素的索引 (index) 可以計算出該元素相對應的儲存位址。
又可分為靜態陣列與動態陣列，靜態陣列在程式編譯時，就已經決定陣列記憶體的位置及大小，動態陣列在程式執行時才做記憶體空間的配置。

<p align="center">
  <img src="https://beginnersbook.com/wp-content/uploads/2018/10/array.jpg" alt="Array">
</p>

## Hash Table (雜湊表; 哈希表)
是根據鍵 (Key) 而直接查詢在記憶體儲存位置的資料結構。通過計算一個關於鍵值的函數(雜湊函數; Hash Function)，將所需查詢的數據映射到表中一個位置來查詢記錄，這加快了查找速度，這個函數稱做雜湊函數，存放記錄的數組稱做雜湊表。

### 衝突
對不同的關鍵字可能得到同一雜湊地址，這種現象稱為衝突 (Collision)。

為了知道衝突產生的相同雜湊函數地址所對應的關鍵字，必須選用另外的雜湊函數，或者對衝突結果進行處理。而不發生衝突的可能性是非常之小的，所以通常對衝突進行處理。常用方法有以下幾種：
- 開放定址法 (open addressing)
- 分離鏈結 (Separate chaining)

## Linked List (連結串列)

## Stack (堆疊)

## Queues

## Trees

## Graphs
