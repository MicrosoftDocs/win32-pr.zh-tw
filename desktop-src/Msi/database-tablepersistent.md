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
ms.openlocfilehash: 1a1e91e1c01ca3fe2efc45855583031e84dc2b47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999521"
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
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase 定義為 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




