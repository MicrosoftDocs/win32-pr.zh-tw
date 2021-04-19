---
description: 記錄物件的 IsNull 屬性是唯讀屬性，如果指定的欄位為 Null，則會傳回 True，如果欄位包含資料，則會傳回 False。
ms.assetid: f36240fa-d4a2-461f-a404-ba867b5f2950
title: 'Record 屬性 (實例 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.IsNull
- IRecord000C1093-0000-0000-C000-000000000046.get_IsNull
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 027d5f818b63ca1883034ae0dfc12b46ef47b005
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982640"
---
# <a name="recordisnull-property"></a>Record 屬性

[**記錄**](record-object.md)物件的 **IsNull** 屬性是唯讀屬性，如果指定的欄位為 Null，則會傳回 True，如果欄位包含資料，則會傳回 False。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Record.IsNull
```



## <a name="property-value"></a>屬性值

記錄中值的必要欄位編號（以1為基礎）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| 標頭<br/>  | <dl> <dt>實例。h</dt> </dl>                                                                                                                                                                   |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord 定義為000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




