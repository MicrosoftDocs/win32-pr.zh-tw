---
description: 資料庫物件的 Import 方法會從文字封存檔匯入資料庫資料表，並卸載任何現有的資料表。
ms.assetid: 9ecc31d9-bccd-48cc-b205-9ce70aaf638a
title: Database. Import 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Import
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b931b77e6cf736bc291079532d20d9c6b48dd243
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989797"
---
# <a name="databaseimport-method"></a>Database. Import 方法

[**資料庫**](database-object.md)物件的 **Import** 方法會從 [文字](text-archive-files.md)封存檔匯入資料庫資料表，並卸載任何現有的資料表。

## <a name="syntax"></a>語法


```JScript
Database.Import(
  path,
  file
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*path* 
</dt> <dd>

存在文字檔的必要資料夾。

</dd> <dt>

*file* 
</dt> <dd>

要匯入之檔案的必要名稱。 這不包含資料夾，因為必須在 path 物件中設定。 資料表名稱是在檔案中指定的。

</dd> </dl>

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



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**資料庫**](database-object.md)
</dt> <dt>

[**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)
</dt> </dl>

 

 




