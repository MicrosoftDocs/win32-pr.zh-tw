---
description: ICE10 會驗證子功能的通告狀態是否符合其父項功能的狀態。
ms.assetid: b0e0d837-245e-4c38-a7c4-06dda0eea25c
title: ICE10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80071bdb7f219904c03d7c6b5b947a1bd818af2c3ebc270b0bfb17f2cf185280
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581208"
---
# <a name="ice10"></a>ICE10

ICE10 會驗證子功能的通告狀態是否符合其父項功能的狀態。

子功能可能不允許廣告，但其父功能允許廣告。 因此，父系和子屬性的下列組合是不正確。

``` syntax
parent = msidbFeatureAttributesFavorAdvertise 
child = msidbFeatureAttributesDisallowAdvertise
```

這種組合無效，因為它會在每次應通告父系時關閉父系。 不過，允許反向。 當父系標示為不允許公告時，可以將子系標示為優先使用公告。

ICE10 自訂動作會從 [功能](feature-table.md) 資料表的 [屬性] 資料行中，決定父項和子功能的狀態。 請注意，將功能的狀態設定為0，並將其父系或子系設定為偏好或不允許公告是有效的。

## <a name="result"></a>結果

如果 [功能](feature-table.md) 資料表的 [屬性] 資料行包含 [公告] 狀態的不符，ICE10 會張貼錯誤。

## <a name="example"></a>範例

ICE10 會針對所顯示的範例張貼下列錯誤訊息。

``` syntax
Conflicting states, one favors, one disallows. Child: Word differs in advertise state 
from Parent: Office.
```

請注意，在此範例中，Microsoft Excel 和 Microsoft Word 是 Microsoft Office 的子功能。

[功能](feature-table.md) 表 (部分) 



| 功能 | 功能 \_ 父系 | 屬性 |
|---------|-----------------|------------|
| Office  | Null            | 4          |
| Excel   | Office          | 4          |
| Word    | Office          | 8          |



 

在此範例中，Word 設定為 [不允許公告]，這會與父項的 [允許公告] 狀態 Office 衝突。

在某些情況下，ICE10 會張貼下列錯誤：

``` syntax
Parent feature: 'Parent' not found for child feature: 'Child'. This error means 
that for the child feature 'Child', the feature 'Parent' is not listed in the 
Feature table.
```

這是指不正確外鍵參考。 修正方法是讓「子系」指向其正確的父功能，或將父項功能 ' Parent ' 的專案加入至 [功能](feature-table.md) 資料表。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



