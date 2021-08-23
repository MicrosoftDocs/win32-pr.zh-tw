---
description: ICEM09 會驗證合併模組是否安全地處理預先定義的目錄。
ms.assetid: 747ae5ee-adc1-4aa7-8239-2379f76bfd0f
title: ICEM09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e4d2af38903d2e704d49b48f932818d8dfaeeb1e12588c007d4af05c297642c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894488"
---
# <a name="icem09"></a>ICEM09

ICEM09 會驗證合併模組是否安全地處理預先定義的目錄。 它是藉由確認模組中的任何元件，將目錄安裝到預先定義的系統目錄（例如 "ProgramFilesFolder" 或 "StartMenuFolder"）來完成這項工作。 相反地，模組應該使用具有唯一名稱的目錄， (使用合併模組命名慣例來建立) 並使用自訂動作將目標設為適當的目標目錄。 這種方法可防止模組與最終資料庫中現有的目錄結構衝突。 ICEM09 會檢查這項技術是否 (所需的自訂動作是否存在，讓合併工具可以) 或以正確的格式 (產生這些動作，以) 的方式運作。

若無法修正 ICEM09 回報的警告或錯誤，可能會導致合併模組的用戶端發生問題。 具有主鍵的目錄資料表資料列（例如 ProgramFilesFolder）通常存在於資料庫中;因此，如果您模組中的元件會直接安裝到預先定義的目錄（例如 ProgramFilesFolder），則模組中的目錄專案可能會與現有的資料列相衝突。 這種情況會要求您的模組使用者必須從您的模組分割原始程式檔，才能符合現有的來原始目錄。

## <a name="result"></a>結果

當模組元件將目錄安裝到預先定義的系統目錄時，ICEM09 會報告錯誤或警告，導致可能與現有目錄結構發生名稱衝突。

## <a name="example"></a>範例

ICEM09 會針對包含所顯示資料庫專案的模組張貼下列警告。

``` syntax
Warning: The component 'Component1.<GUID>' installs directly into the pre-defined 
directory 'ProgramFilesFolder'. It is recommended that merge modules alias 
all such directories to unique names.
```

重新命名合併模組目錄，使其不符合 Windows Installer 屬性，因此是唯一的。 然後，將相同名稱的屬性設定為 Windows Installer 目錄的值。 進行目錄解析時，目錄具有相同名稱的屬性，因此目錄的安裝位置是屬性的值。 檔案會從相異來源位置移至相同的目標位置。 此程式應完全移除合併衝突。

``` syntax
Warning: The 'ModuleInstallExecuteSequence' table contains a type 51 action 
(StartMenuFolder.<GUID>) for a pre-defined directory, but this action 
does not have sequence number '1'
```

如果動作沒有序號1，它可能不會在順序中提早合併到目標資料庫，以便有效地運作。

若要修正此警告，請將序號設為1。 請注意，最新的合併工具 (但不是某些舊版的) 將會在合併時間產生這些自訂動作，因此不一定需要明確地將動作撰寫到合併模組。

``` syntax
Warning: The 'CustomAction' table contains a type 51 action (MyAppDataFolderAction) 
for a pre-defined directory, but the name is not the same as the target directory. 
Many merge tools will generate duplicate actions."
```

由於 CustomAction 資料行是 CustomAction 資料表的主要索引鍵，因此某些合併工具可能會產生重複的動作，因為預先撰寫的動作名稱是不同的。

若要修正此警告，請將動作命名為與目標目錄相同的名稱。 請注意，最新的合併工具 (但不是某些較舊的版本) 在合併時間產生這些自訂動作，因此不一定需要明確地將動作撰寫到合併模組。

[目錄資料表](directory-table.md)



| 目錄          | 目錄 \_ 父系 | DefaultDir |
|--------------------|-------------------|------------|
| ProgramFilesFolder | Directory1        | A          |
| StartMenuFolder    | Directory2        | B:C        |
| AppDataFolder      | Directory3        | D          |
| MyPicturesFolder   | Directory4        | E          |



 

[元件資料表](component-table.md)



| 元件               | 目錄          |
|-------------------------|--------------------|
| Component1.<GUID> | ProgramFilesFolder |
| Component2.<GUID> | StartMenuFolder    |
| Component3.<GUID> | AppDataFolder      |
| Component4.<GUID> | MyPicturesFolder   |



 

[CustomAction 資料表](customaction-table.md)



| CustomAction                 | 類型 | 來源                       | 目標              |
|------------------------------|------|------------------------------|---------------------|
| StartMenuFolder.<GUID> | 51   | StartMenuFolder.<GUID> | \[StartMenuFolder\] |
| MyAppDataFolderAction        | 51   | AppDataFolder.<GUID>   | \[AppDataFolder\]   |



 

[ModuleInstallExecuteSequence 資料表](moduleinstallexecutesequence-table.md)



| 動作                       | 順序 | BaseAction | After | 條件 |
|------------------------------|----------|------------|-------|-----------|
| StartMenuFolder.<GUID> | 100      |            |       |           |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Merge Module ICE 參考](merge-module-ice-reference.md)
</dt> </dl>

 

 



