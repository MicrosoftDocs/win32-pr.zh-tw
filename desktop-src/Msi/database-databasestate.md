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
ms.openlocfilehash: a44fcc9e082878077533edafcd44c9f5a5f26e76bddd3ddb5619fb2842ec0d3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745638"
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
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase 定義為 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




