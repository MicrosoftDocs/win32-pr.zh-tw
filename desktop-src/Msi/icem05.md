---
description: ICEM05 會驗證合併模組是否已正確與模組中的元件相關聯。 元件與模組的關聯不正確，導致元件與目標資料庫的關聯不正確。
ms.assetid: 1bf4041e-b198-4897-8719-8505fd8180ec
title: ICEM05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e62ca481ef836c2675c381817fe2242e37384818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026636"
---
# <a name="icem05"></a>ICEM05

ICEM05 會驗證合併模組是否已正確與模組中的元件相關聯。 元件與模組的關聯不正確，導致元件與目標資料庫的關聯不正確。

Merge module 會儲存在合併模組中，名為 Mergemod 的 .cub 檔中，而不是在包含用於封裝驗證的 Ices-003 的 .cub 檔案中。

## <a name="result"></a>結果

如果模組資料庫不正確地關聯元件和模組，ICEM05 會張貼錯誤。

## <a name="example"></a>範例

ICEM05 會針對包含如下所示資料庫專案的模組，張貼下列錯誤訊息。

``` syntax
The component Component2.OtherModule.GUID2.1033 in the 
ModuleComponents table does not belong to this Merge Module.
The component Component1.MyModule.GUID1.1033 in the ModuleComponents 
table is not listed in the Component table.
The component 'Component3' in the Component table is not listed in the 
ModuleComponents table.
```

[ModuleSignature 資料表](modulesignature-table.md)



| ModuleID         | 語言 | 版本 |
|------------------|----------|---------|
| MyModule.*GUID1* | 1033     | 1.0     |



 

[**ModuleComponents 資料表**](modulecomponents-table.md)



| 元件  | ModuleID            | 語言 |
|------------|---------------------|----------|
| Component1 | MyModule.*GUID1*    | 1033     |
| Component2 | OtherModule.*GUID2* | 1033     |



 

[元件資料表](component-table.md) (部分) 



| 元件  | ComponentID |
|------------|-------------|
| Component3 | *GUID4*     |
| Component2 | *GUID5*     |



 

Merge module ICE 會報告第一個錯誤，因為 ModuleComponents 資料表會嘗試將元件與另一個不是 ModuleSignature 資料表中指定之模組的模組產生關聯。 若要修正此問題，請將 Component2 的 ModuleComponents 記錄的 ModuleID 和 Language 資料行變更為目前模組 MyModule 的。*GUID1*。

Merge module ICE 會報告第二個錯誤，因為 ModuleComponents 資料表中的第一筆記錄嘗試將 Component1 與模組產生關聯。 此元件不存在於合併模組的元件資料表中。 模組只能與存在於模組中的元件相關聯。 若要修正此問題，請移除不存在元件的記錄。

Merge module ICE 會回報第三個錯誤，因為此模組會嘗試將 Component3 新增至目標資料庫。 這個元件尚未與 ModuleComponents 資料表中的模組相關聯。 若要修正這個錯誤，請將 Component3 的記錄新增至 ModuleComponents 資料表。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Merge Module ICE 參考](merge-module-ice-reference.md)
</dt> </dl>

 

 



