---
description: Item 屬性是唯讀屬性，會傳回 StringList 物件集合中的字串。
ms.assetid: 5c654927-41cf-4e47-9d4f-76524f8bbc97
title: StringList 專案屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringList.Item
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ebd32af433fd932cb05d062fbc515a3245113343
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984790"
---
# <a name="stringlistitem-property"></a>StringList 專案屬性

**Item** 屬性是唯讀屬性，會傳回 [**StringList 物件**](stringlist-object.md)集合中的字串。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = StringList.Item
```



## <a name="property-value"></a>屬性值

具有字串集合之專案的索引編號。 此為必要參數。

## <a name="remarks"></a>備註

用戶端必須先確認 [**StringList 物件**](stringlist-object.md) 存在且不是空的，然後再參考 **專案** 屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IStringList 定義為000C1095-0000-0000-C000-000000000046<br/>                                                                                                                                                                          |



 

 




