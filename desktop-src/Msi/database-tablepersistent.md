---
description: 資料庫物件的 TablePersistent 屬性會以下列其中一個參數傳回資料表的持續性狀態。
ms.assetid: c395e99c-5cdc-4d7b-ac55-a79d4e1477dc
title: TablePersistent 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.TablePersistent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f5eaf32996adef39976ba9fbaf88834c339e27dbe13c4e7fbcd1928ac1973b9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129638"
---
# <a name="databasetablepersistent-property"></a>TablePersistent 屬性

[**資料庫**](database-object.md)物件的 **TablePersistent** 屬性會以下列其中一個參數傳回資料表的持續性狀態。



| 資料表狀態               | 值 | 描述                    |
|---------------------------|-------|--------------------------------|
| msiEvaluateConditionFalse | 0     | 資料表是暫時性的。            |
| msiEvaluateConditionTrue  | 1     | 資料表是永久性的。           |
| msiEvaluateConditionNone  | 2     | 資料表不在資料庫中。  |
| msiEvaluateConditionError | 3     | 無效或遺漏資料表名稱。 |



 

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Database.TablePersistent
```



## <a name="property-value"></a>屬性值

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase 定義為 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




