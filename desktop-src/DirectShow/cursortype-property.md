---
description: CursorType 屬性會設定或抓取目前的資料指標類型。
ms.assetid: f362e790-a7c7-4fb6-86f3-7cd25f78fe0e
title: CursorType 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c17ae74c471bebe6da2bcef4d22d7c247f4eda1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846356"
---
# <a name="cursortype-property"></a>CursorType 屬性

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`CursorType`屬性會設定或抓取目前的資料指標類型。

``` syntax
[ iCursorType = ] MSWebDVD.CursorType
```

## <a name="return-value"></a>傳回值

傳回表示資料指標類型的整數值。

## <a name="remarks"></a>備註

這個屬性的可能值為：



| 值 | 描述 |
|-------|-------------|
| 0     | 箭號       |
| 1     | 放大     |
| 2     | 縮小    |
| 3     | 手        |
| -1    | 無        |



 

此屬性是讀取/寫入，預設值為零。 當圖片放大時，將 `CursorType` (0x3 的 **設定設** 為) 會將應用程式放入拖曳模式，讓使用者能夠在影片顯示區域內移動影像。

 

 



