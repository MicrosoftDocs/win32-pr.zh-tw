---
description: ICE02 會驗證元件、檔案和登錄資料表之間的特定參考是否互相交互。 這些參考必須是交互的，才能讓安裝程式正確地判斷元件的安裝狀態。
ms.assetid: 864404f1-439d-49a2-973d-4e6e1618863e
title: ICE02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1975203825d079d5eeb1ec5e4183767dd68625bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689744"
---
# <a name="ice02"></a>ICE02

ICE02 會驗證[元件](component-table.md) [、檔案和登錄](file-table.md)[資料表之間](registry-table.md)的特定參考是否互相交互。 這些參考必須是交互的，才能讓安裝程式正確地判斷元件的安裝狀態。

安裝程式會使用元件資料表的 KeyPath 資料行，來偵測元件資料行中所列的元件是否存在。 KeyPath 資料行包含登錄或檔案資料表中的索引鍵。 這兩個數據表都有一個元件資料 \_ 行，其中包含索引鍵的元件資料表，指向控制登錄專案或檔案的元件。 這些參考必須是相互參考。

## <a name="result"></a>結果

如果 ICE02 發現的參考應該是交互且不是，則會張貼錯誤訊息。

## <a name="example"></a>範例

ICE02 會針對包含所顯示資料庫專案的 .msi 檔案張貼下列錯誤訊息。

``` syntax
File: 'Red_File' cannot be the key file for Component: 'Blue'. The file belongs to Component: 'Red'
```

[元件資料表](component-table.md) (部分) 



| 元件 | KeyPath   |
|-----------|-----------|
| 紅色       | Red \_ File |
| 藍色      | Red \_ File |



 

[檔資料表](file-table.md) (部分) 



| File 資料行 | 元件\_ |
|-------------|-------------|
| Red \_ File   | 紅色         |
| Blue \_ 檔案  | 藍色        |



 

元件 Blue 參考紅色檔案 \_ ，但紅色檔案 \_ 不是由元件藍色所控制，因此不能是 KeyPath 檔。 如果呼叫安裝程式以取得藍色的安裝狀態，則會不正確地檢查是否已 \_ 安裝 Red File。 將元件資料表中藍色的 KeyPath 欄位變更為 Blue \_ File 可修正錯誤。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



