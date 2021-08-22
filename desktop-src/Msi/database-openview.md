---
description: 資料庫物件的 OpenView 方法會傳回 View 物件，該物件代表 SQL 字串所指定的查詢。
ms.assetid: 6afb2fdb-0e6a-468f-8faf-e48d8d1960b6
title: '資料庫. .h 方法 (Certview .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.OpenView
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ccc37b72dd44064172672d1067dae293da30048853f3ca83f82fb50b0a90cfaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947521"
---
# <a name="databaseopenview-method"></a>資料庫. OpenView 方法

[**資料庫**](database-object.md)物件的 **OpenView** 方法會傳回 [**View**](view-object.md)物件，該物件代表 SQL 字串所指定的查詢。

## <a name="syntax"></a>語法


```JScript
Database.OpenView(
  sql
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*sql* 
</dt> <dd>

需要 SQL 查詢字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如需安裝程式中所執行之 SQL 語法的詳細資訊，請參閱[SQL 語法](sql-syntax.md)。

如果方法失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| 標頭<br/>  | <dl> <dt>Certview。h</dt> </dl>                                                                                                                                                                   |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase 定義為 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**資料庫**](database-object.md)
</dt> <dt>

[SQL語法](sql-syntax.md)
</dt> </dl>

 

 




