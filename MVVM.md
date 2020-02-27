# MVVM
MVVM 是一種架構設計模式，可拆分成三個部份，Model、View、ViewModel，

- Model: 數據模型，泛指後端各種業務邏輯理與數據處理，主要對資料庫操作。

- View: 視圖層，也指用戶介面，不會有邏輯、狀態等等，單純呈現資料的元件。

- ViewModel: 介在View跟Model的中間，像是中繼站，與視圖層雙向數據綁定，在從Model取到資料後，把資料整理好成為方便顯示的樣子，而View一看到ViewModel的資料有更新，就會跟著一起更新。

![MVVM](https://miro.medium.com/max/771/1*_DMvajfGcKQoIOWpLysa1Q.png)
