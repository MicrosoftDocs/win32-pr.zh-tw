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
ms.openlocfilehash: b3593f31d8f8cea6278346e8c99bb9c9b880aed273ae7ab70614ade112cd8c8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912918"
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
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord 定義為000C1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



 

 




