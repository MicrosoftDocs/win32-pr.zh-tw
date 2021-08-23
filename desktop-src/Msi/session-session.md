---
description: 會話物件的屬性（Property）屬性（Property）是讀寫屬性（property），這個屬性（property）（property）（Property）（Property）（Property）是由 Session 物件維護，
ms.assetid: 15ce8264-2573-428c-98d9-690cfaae5144
title: Session. Property 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7f47efd603f10378e6cf5b09144d57776a42cd515f3bd6194174d94bc2583514
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628828"
---
# <a name="sessionproperty-property"></a>Session. Property 屬性

[**Session**](session-object.md)物件的 property 屬性（ **property** ）是讀寫屬性（property），這個屬性（property）表示指定之安裝程式屬性的字串值（由記憶體內部屬性工作表中的 **Session** 物件維護），或者，如果前面加上百分比符號 (% ) ，則為目前進程的系統內容變數值。 可能會提供字串或整數值。 不存在的屬性或環境變數相當於其值為 Null。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```JScript
propVal = Session.Property
Session.Property = propVal 
```



## <a name="property-value"></a>屬性值

需要區分大小寫的屬性名稱，或前面加上百分比符號 (% ) 的環境變數名稱不區分大小寫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




