---
description: UIPreview 物件的屬性（Property）屬性（Property）是讀寫屬性（property），表示指定之安裝程式屬性的字串值，如果前面加上百分比符號 (% ) ，則為目前進程的系統內容變數值。
ms.assetid: 92900426-8fb5-4a94-a982-438267ad756e
title: UIPreview 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 51ef7b4589372006241beff1e9c35180b32c4d358e817b8d380353c324ffd9a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118623201"
---
# <a name="uipreviewproperty-property"></a>UIPreview 屬性

[**UIPreview**](uipreview-object.md)物件的 **屬性（property** ）屬性（property）是讀寫屬性（property），表示指定之安裝程式屬性的字串值，如果前面加上百分比符號 (% ) ，則為目前進程的系統內容變數值。 這是為了允許適當地顯示相依于屬性值的對話方塊。 可能會提供字串或整數值。 不存在的屬性或環境變數相當於其值為 null。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```JScript
propVal = UIPreview.Property
UIPreview.Property = propVal 
```



## <a name="property-value"></a>屬性值

需要區分大小寫的屬性名稱，或前面加上百分比符號 (% ) 的環境變數名稱不區分大小寫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IUIPreview 定義為 000C109A-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




