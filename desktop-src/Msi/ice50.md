---
description: ICE50 會檢查是否已指定快速鍵圖示，以正確顯示並符合其目標檔案的副檔名。
ms.assetid: 19288c87-fddb-46c9-8145-59e1b870a261
title: ICE50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b9dd81c84c52738ee58c023ba5727cd6d5766bf7c40db97b6459483d7f53d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635149"
---
# <a name="ice50"></a>ICE50

ICE50 會檢查是否已指定快速鍵圖示，以正確顯示並符合其目標檔案的副檔名。

## <a name="result"></a>結果

如果圖示和目標檔案的副檔名不相符，ICE50 會張貼錯誤訊息。 如果圖示儲存在沒有 .exe 或 .ico 副檔名的檔案中，ICE50 會張貼警告。

## <a name="example"></a>範例

ICE50 會針對所顯示的範例報告下列錯誤。



| ICE50 錯誤或警告                                                                                                              | Description                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 快速鍵 ' Shortcut2 ' 的圖示 ' Icon2 ' 副檔名不符合元件 ' Component2 ' 的金鑰檔延伸。 | 如果圖示和目標檔案的副檔名不相符，則在公告元件時，快捷方式將不會有正確的內容功能表。 若要修正這個錯誤，請將圖示重新命名以符合目標檔案的副檔名。<br/> |
| 快速鍵 ' Shortcut1 ' 的圖示 ' Icon1.bat ' 副檔名不是 "exe" 或 ".ico"。 圖示將不會正確顯示。         | 並非所有版本的 shell 都正確地顯示儲存在沒有 "exe" 或 ".ico" 副檔名之檔案中的圖示。 若要修正此警告，請將圖示重新命名為 "exe" 或 ".ico" 的副檔名。<br/>                                      |



 

[檔資料表](file-table.md) (部分) 



| 檔案  | FileName  |
|-------|-----------|
| File1 | File1.bat |
| File2 | File2.pl  |



 

[功能表](feature-table.md) (部分) 



| 功能  |
|----------|
| Feature1 |



 

[元件資料表](component-table.md) (部分) 



| 元件  | KeyPath |
|------------|---------|
| Component1 | File1   |
| Component2 | File2   |



 

[圖示表](icon-table.md)



| Name      | 資料            |
|-----------|-----------------|
| Icon1.bat | \[Binary Data\] |
| Icon2 .dat | \[Binary Data\] |



 

 (部分) 的[快捷方式資料表](shortcut-table.md)



| 快速鍵  | 元件  | 目標   | 圖示\_    |
|-----------|------------|----------|-----------|
| Shortcut1 | Component1 | Feature1 | Icon1.bat |
| Shortcut2 | Component2 | Feature1 | Icon2 .dat |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 




