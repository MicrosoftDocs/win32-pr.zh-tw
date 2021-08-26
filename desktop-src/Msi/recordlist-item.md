---
description: Item 屬性是唯讀屬性，會傳回 RecordList 物件集合中的記錄。
ms.assetid: 59646aa8-811c-4658-8b47-42f70abfdfdb
title: RecordList 專案屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecordList.Item
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7df19a26fd4e8464963f09ffdf227ac88f4376624a88df84d6245efa3c5fd927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041808"
---
# <a name="recordlistitem-property"></a>RecordList 專案屬性

**Item** 屬性是唯讀屬性，會傳回 [**RecordList**](recordlist-object.md)物件集合中的記錄。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = RecordList.Item
```



## <a name="property-value"></a>屬性值

具有字串集合之專案的索引編號。 需要索引。

## <a name="remarks"></a>備註

用戶端必須先確認 [**RecordList**](recordlist-object.md) 物件存在且不是空的，然後再參考專案屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecordList 定義為000C1096-0000-0000-C000-000000000046<br/>                                                                                                                                                                          |



 

 




