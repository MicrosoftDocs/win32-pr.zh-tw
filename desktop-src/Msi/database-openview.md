---
description: 資料庫物件的 OpenView 方法會傳回 View 物件，該物件表示 SQL 字串所指定的查詢。
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
ms.openlocfilehash: 8dc62ca38bfe28980da71ecf63eda8e6c39aaf0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984446"
---
# <a name="databaseopenview-method"></a>資料庫. OpenView 方法

[**資料庫**](database-object.md)物件的 **OpenView** 方法會傳回 [**View**](view-object.md)物件，該物件表示 SQL 字串所指定的查詢。

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

必要的 SQL 查詢字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如需安裝程式中所執行 SQL 語法的詳細資訊，請參閱 [Sql 語法](sql-syntax.md)。

如果方法失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| 標頭<br/>  | <dl> <dt>Certview。h</dt> </dl>                                                                                                                                                                   |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase 定義為 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**資料庫**](database-object.md)
</dt> <dt>

[SQL 語法](sql-syntax.md)
</dt> </dl>

 

 




