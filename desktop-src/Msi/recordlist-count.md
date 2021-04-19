---
description: Count 屬性是唯讀屬性，會傳回 RecordList 物件中的專案數。
ms.assetid: df384d5c-931f-4a31-af55-d013f010e100
title: RecordList Count 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecordList.Count
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 01d1ee815140b86acefd6d8fee10ca7827eba9ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984334"
---
# <a name="recordlistcount-property"></a>RecordList Count 屬性

**Count** 屬性是唯讀屬性，會傳回 [**RecordList**](recordlist-object.md)物件中的專案數。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = RecordList.Count
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

用戶端必須先確認 [**RecordList**](recordlist-object.md) 物件存在，而且在參考 Count 屬性之前不是空的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecordList 定義為000C1096-0000-0000-C000-000000000046<br/>                                                                                                                                                                          |



 

 




