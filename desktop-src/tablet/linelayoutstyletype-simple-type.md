---
description: 定義 LineLayout 元素之 Style 屬性的有效值。
ms.assetid: b257f0da-1bee-4d1b-9829-70f91cdcabe0
title: LineLayoutStyleType 簡單類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LineLayoutStyleType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d2aa0a42ca2f295cdcccad05931ba651d4018ba377d8d10f09f85b82dcaaea8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031836"
---
# <a name="linelayoutstyletype-simple-type"></a>LineLayoutStyleType 簡單類型

定義 [LineLayout 元素](linelayout-element.md)之 **Style** 屬性的有效值。

``` syntax
<xs:simpleType name="LineLayoutStyleType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="None|Solid|Dash|Dot|DashDot|DashDotDot|Double"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>模式

**LineLayoutStyleType** 簡單類型是以下列模式限制的字串：

-   `None|Solid|Dash|Dot|DashDot|DashDotDot|Double`

## <a name="remarks"></a>備註

[LineLayout 元素](linelayout-element.md)的 **Style** 屬性有效值為：

-   無
-   實線
-   虛線
-   點
-   DashDot
-   DashDotDot
-   Double

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                                     |



 

 




