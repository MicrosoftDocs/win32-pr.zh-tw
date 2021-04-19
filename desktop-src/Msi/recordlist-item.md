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
ms.openlocfilehash: 4c7b9332393c4055cb8052b2b759b93781c0fd73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993368"
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
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecordList 定義為000C1096-0000-0000-C000-000000000046<br/>                                                                                                                                                                          |



 

 




