---
description: Database 物件的 Export 方法會將指定之資料表的結構和資料複製到文字封存檔案。
ms.assetid: b724595f-ef28-456e-bf0b-5df65c659d17
title: Database. Export 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Export
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: faa5e2459eb0fe4ba04fd548bc478c9a0e2c85267e1df8e3d318f4a3f6a082ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745608"
---
# <a name="databaseexport-method"></a>Database. Export 方法

[**Database**](database-object.md)物件的 **Export** 方法會將指定之資料表的結構和資料複製到 [文字](text-archive-files.md)封存檔案。

## <a name="syntax"></a>語法


```JScript
Database.Export(
  table,
  path,
  file
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*table* 
</dt> <dd>

資料庫資料表的必要名稱。 如果使用安裝程式資料庫，則區分大小寫。

</dd> <dt>

*path* 
</dt> <dd>

必要的字串，也就是放置文字檔的資料夾路徑。

</dd> <dt>

*file* 
</dt> <dd>

要建立之檔案的必要名稱。 這不包含資料夾，因為必須在 path 物件中設定。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果方法失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase 定義為 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




