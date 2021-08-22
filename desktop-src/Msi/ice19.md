---
description: ICE19 會驗證公告的元件是否參考元件資料表的 KeyPath 資料行中的檔案，以及公告的快捷方式是否參考此資料行中的目錄。
ms.assetid: 438153c1-bc4b-4ecf-ab85-d66ad69c987c
title: ICE19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1a706999744762a930a800326cb8d38487f19c1c4ea3e01b6b1f8aeae4ca2dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529108"
---
# <a name="ice19"></a>ICE19

ICE19 會驗證公告的元件是否參考 [元件資料表](component-table.md) 的 KeyPath 資料行中的檔案，以及公告的快捷方式是否參考此資料行中的目錄。

ICE19 會驗證公告的元件或快捷方式是否有元件。 [PublishComponent 資料表](publishcomponent-table.md)中不是在另一個資料表中公告的元件，只會檢查其是否有一個元件。

## <a name="result"></a>結果

如果在已公告的快捷方式中，如果元件資料表的 KeyPath 資料行未參考檔案或目錄，ICE19 會張貼錯誤訊息。 如果任何公告的元件或快捷方式沒有元件，ICE19 會張貼錯誤訊息。

## <a name="example"></a>範例

ICE19 會針對所顯示的範例張貼下列錯誤訊息：

-   擴充功能 flp 會參考元件 [資料表](component-table.md)中沒有指定元件的元件 Comp1。
-   擴充 exe 參考參考目錄作為其 KeyPath 的元件 Comp4。 元件資料表中的 KeyPath 為 Null。
-   快速鍵 Shortcut2 會參考參考登錄專案做為金鑰路徑的元件 Comp3。 元件資料表中的 [屬性] 資料行值為4。

[元件資料表](component-table.md) (部分) 



| 元件 | ComponentId                            | 屬性 | KeyPath |
|-----------|----------------------------------------|------------|---------|
| Comp1     | Null                                   | 0          | File1   |
| Comp2     | {00000002-0003-0000-0000-624474736554} | 0          | File2   |
| Comp3     | {00000003-0003-0000-0000-624474736554} | 4          | Reg3    |
| Comp4     | {00000004-0003-0000-0000-624474736554} | 0          | Null    |



 

[延伸模組資料表](extension-table.md) (部分) 



| 延伸模組 | 元件\_ |
|-----------|-------------|
| flp       | Comp1       |
| Tst       | Comp2       |
| exe       | Comp4       |



 

 (部分) 的[快捷方式資料表](shortcut-table.md)



| 快速鍵  | 元件\_ | 特徵\_      |
|-----------|-------------|----------------|
| Shortcut1 | Comp4       | ProductFeature |
| Shortcut2 | Comp3       | ProductFeature |



 

[功能表](feature-table.md) (部分) 



| 功能        |
|----------------|
| ProductFeature |



 

> [!Note]  
> 如果延伸模組 flp 和 exe 都參考相同的元件，則開啟它們的 EXE 或 COM 伺服器必須相同。 這個 EXE 通常是元件的 KeyPath。 針對 OFFICE，延伸模組檔和 xls 無法參考相同的元件，因為相同的 EXE 不會同時開啟這兩個延伸模組。 您需要 winword.exe 開啟檔副檔名，而且需要 excel.exe 來開啟 xls 擴充功能。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



