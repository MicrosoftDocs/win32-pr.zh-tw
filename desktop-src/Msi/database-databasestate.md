---
description: 資料庫物件的 DatabaseState 屬性是唯讀屬性。
ms.assetid: 0a466e53-4ff5-4b95-b754-1aac0af16805
title: DatabaseState 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.DatabaseState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 12a667bf145ea00f7a881c8219987f21c99af4ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987050"
---
# <a name="databasedatabasestate-property"></a>DatabaseState 屬性

[**資料庫**](database-object.md)物件的 **DatabaseState** 屬性是唯讀屬性。

這個屬性會以下列其中一個參數傳回資料庫的持續性狀態。



| 資料庫狀態        | 值 | 描述                                                                                                |
|-----------------------|-------|------------------------------------------------------------------------------------------------------------|
| msiDatabaseStateRead  | 0     | 資料庫會以唯讀方式開啟。 不允許變更持續性資料，也不會儲存暫存資料。 |
| msiDatabaseStateWrite | 1     | 資料庫可完全運作以進行讀取和寫入。                                                          |



 

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Database.DatabaseState
```



## <a name="property-value"></a>屬性值

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase 定義為 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




