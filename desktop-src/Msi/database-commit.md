---
description: 資料庫物件的 Commit 方法會完成資料庫的持續性形式。
ms.assetid: 39253ccd-08f1-4a6f-87cb-3678ae5221a4
title: Database. Commit 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Commit
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d62c998a70e0a4a036695be10b2bf1d983044241
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001150"
---
# <a name="databasecommit-method"></a>Database. Commit 方法

[**資料庫**](database-object.md)物件的 **Commit** 方法會完成資料庫的持續性形式。 所有持續性資料都會寫入至可寫入的資料庫，而且不會寫入任何暫存資料行或資料列。 這個方法不會影響以唯讀方式開啟的資料庫。 您可以多次呼叫這個方法，以儲存載入記憶體之資料表的目前狀態。 當資料庫最後關閉時，最後一次 **認可** 之後所做的任何變更都會復原。 當所有資料庫變更都已完成時，通常會在關閉之前呼叫這個方法。

## <a name="syntax"></a>語法


```JScript
Database.Commit()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果方法失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase 定義為 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




