# ユーザー Library の作り方

## Library の作成

PLC > Project で右クリックする。  
Properties を選択する。  
![Solution_ProjectProperties](assets/Solution_ProjectProperties.png)

太字の項目は必須項目です。  
Project Infomation に Library の情報を入力します。  
![Properties_Common](assets/Properties_Common.png)

PLC > Project で右クリックする。  
Save as library ... を選択する。  
![Solution_SaveLibrary](assets/Solution_SaveLibrary.png)

Library ファイルとして保存する。  
![Dialog_SaveLibrary](assets/Dialog_SaveLibrary.png)

## Library の使用方法

### Library を TwinCAT に登録する

PLC > Project > References を開く。  
Library Manager が表示される。  
Library repository を選択する。  
![LibraryManager_Main](assets/LibraryManager_Main.png)

Install を開く。  
ダイアログが表示されるので、インストールしたい library ファイルを選択する。  
![LibraryRepository_Main](assets/LibraryRepository_Main.png)

作成した Library が TwinCAT に登録される。  
![LibraryRepository_InstalledLibrary](assets/LibraryRepository_InstalledLibrary.png)

### Library を PLC Project に適用する

Library Manager > Add library を開く。  
![LibraryManager_AddLibrary](assets/LibraryManager_AddLibrary.png)

登録した Library を追加する。  
![AddLibrary_UseLibrary](assets/AddLibrary_UseLibrary.png)

登録した Library が References に追加される。  
![Solution_References](assets/Solution_References.png)
