---
description: ICEM06 會檢查模組對功能的直接參考是否無效。
ms.assetid: 63e63a60-53e5-4881-ad71-efeceb73a70e
title: ICEM06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5150e511e6f8018e51ab537b52ccc6c32645d09c80110129f040d6a329335ec5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828878"
---
# <a name="icem06"></a>ICEM06

ICEM06 會檢查模組對功能的直接參考是否無效。

Merge module 會儲存在合併模組中，名為 Mergemod 的 .cub 檔中，而不是在包含用於封裝驗證的 Ices-003 的 .cub 檔案中。

## <a name="result"></a>結果

當模組資料庫包含功能的直接參考時，ICEM06 會張貼錯誤。 功能資訊必須由模組的使用者提供。

## <a name="example"></a>範例

ICEM06 會針對包含如下所示資料庫專案的模組，張貼下列錯誤訊息。

``` syntax
The target of shortcut Shortcut1.GUID1 is not a property and not a null GUID. 
Modules may not directly reference features.
The row GUID2.LocalServer32.Component2 in the Class table has a feature reference 
that is not a null GUID. Modules may not directly reference features.
```

 (部分) 的[快捷方式資料表](shortcut-table.md)



| 快速鍵          | 目標                                 |
|-------------------|----------------------------------------|
| Shortcut1.*GUID1* | cmd.exe                                |
| Shortcut2.*GUID1* | \[MyProp\]                             |
| Shortcut3.*GUID1* | {00000000-0000-0000-0000-000000000000} |



 

[類別表](class-table.md) (部分) 



| CLSID   | Context       | 元件\_ | 特徵\_                              |
|---------|---------------|-------------|----------------------------------------|
| *GUID1* | LocalServer32 | Component1  | {00000000-0000-0000-0000-000000000000} |
| *GUID2* | LocalServer32 | Component2  | MyFeature                              |



 

ICEM06 會報告第一個錯誤，因為快捷方式資料表中的第一筆記錄在目標欄位中有一個專案，而該專案不是屬性或 null GUID。 模組無法直接參考功能。 功能資訊必須由模組的使用者提供。 若要修正這個錯誤，應該以 null GUID 取代功能的參考。

ICEM06 會報告第二個錯誤，因為類別資料表中的第二筆記錄在功能欄位中有一個不是 null GUID 的專案。 模組無法直接參考功能。 功能資訊必須由模組的使用者提供。 若要修正這個錯誤，應該以 null GUID 取代功能的參考。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Merge Module ICE 參考](merge-module-ice-reference.md)
</dt> </dl>

 

 



