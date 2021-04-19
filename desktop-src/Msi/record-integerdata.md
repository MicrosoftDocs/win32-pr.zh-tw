---
description: 這是記錄物件的 IntegerData 屬性。 此讀寫屬性會將32位整數資料傳入或傳出記錄內的指定欄位。 如果域值無法轉換成整數，則會傳回 msiDatabaseNullInteger。
ms.assetid: abc291cd-31ba-409f-b010-8b3a71cbdc77
title: IntegerData 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.IntegerData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ed816c75ab6adc98b3ac19984079d840a4a447b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987149"
---
# <a name="recordintegerdata-property"></a>IntegerData 屬性

這是 [**記錄**](record-object.md)物件的 **IntegerData** 屬性。 此讀寫屬性會將32位整數資料傳入或傳出記錄內的指定欄位。 如果域值無法轉換成整數，則會傳回 msiDatabaseNullInteger。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```JScript
propVal = Record.IntegerData
Record.IntegerData = propVal 
```



## <a name="property-value"></a>屬性值

記錄中值的必要欄位編號（以1為基礎）。

## <a name="remarks"></a>備註

若要將記錄整數位段設定為 null，請使用 msiDatabaseNullInteger。 不存在的欄位傳回的值為 msiDatabaseNullInteger。 嘗試在不存在的欄位中儲存值會導致錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord 定義為000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




