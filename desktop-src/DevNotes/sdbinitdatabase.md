---
description: 開啟填充碼資料庫。
ms.assetid: ece1bd39-20a1-42e6-8e2b-1d38f7223d42
title: SdbInitDatabase 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbInitDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 0504b12254658250820cb3ecac3e9e47ee2a6ca242b15600fa69241b597bb0dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666378"
---
# <a name="sdbinitdatabase-function"></a>SdbInitDatabase 函式

開啟填充碼資料庫。

## <a name="syntax"></a>語法


```C++
HSDB WINAPI SdbInitDatabase(
  _In_ DWORD   dwFlags,
  _In_ LPCTSTR pszDatabasePath
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwFlags* \[在\]
</dt> <dd>

此參數會在 *pszDatabasePath* 參數中指定路徑的格式。 它可以是下列值之一。



| 值                                                                                                                                                                                                                                                      | 意義                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="HID_DOS_PATHS"></span><span id="hid_dos_paths"></span><dl> <dt>**HID \_DOS \_ 路徑**</dt> <dt>0x00000001</dt> </dl>                             | MS-DOS 樣式路徑。<br/>                                                                       |
| <span id="HID_DATABASE_FULLPATH"></span><span id="hid_database_fullpath"></span><dl> <dt>**HID \_資料庫 \_ FULLPATH**</dt> <dt>0x00000002</dt> </dl>     | 完整路徑。<br/>                                                                                |
| <span id="HID_NO_DATABASE"></span><span id="hid_no_database"></span><dl> <dt>**HID \_無 \_ 資料庫**</dt> <dt>0x00000004</dt> </dl>                       | *PszDatabasePath* 參數會被忽略，且不會開啟任何資料庫。<br/>                       |
| <span id="HID_DATABASE_TYPE_MASK"></span><span id="hid_database_type_mask"></span><dl> <dt>**HID \_資料庫 \_ 類型 \_ 遮罩**</dt> <dt>0xF00F0000</dt> </dl> | 此參數會指定預先定義的資料庫。 *PszDatabasePath* 參數會被忽略。<br/> |



 

如果 *dwFlags* 包含 **隱藏的 \_ 資料 \_ 類型 \_ 遮罩**，此參數也可以包含下列其中一個值。



| 值                                                                                                                                                                                                                                                               | 意義                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <dt>**SDB \_資料庫 \_ 主要 \_ 填充碼**</dt> <dt>0x80030000</dt> </dl>          | 應用程式填充碼資料庫。<br/>         |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <dt>**SDB \_資料庫 \_ 主要 \_ MSI**</dt> <dt>0x80020000</dt> </dl>             | MSI 資料庫。<br/>                      |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <dt>**SDB \_資料庫 \_ 主要 \_ 驅動程式**</dt> <dt>0x80040000</dt> </dl> | 要封鎖之驅動程式的資料庫。<br/> |



 

</dd> <dt>

*pszDatabasePath* \[在\]
</dt> <dd>

資料庫的路徑。 如果 *dwFlags* 參數指定預先定義的資料庫，則此參數可以是 **Null** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

函數會傳回已開啟資料庫的控制碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SdbGetAppPatchDir**](sdbgetapppatchdir.md)
</dt> <dt>

[**SdbGetMatchingExe**](sdbgetmatchingexe.md)
</dt> <dt>

[**SdbReleaseMatchingExe**](sdbreleasematchingexe.md)
</dt> <dt>

[**SdbTagRefToTagID**](sdbtagreftotagid.md)
</dt> </dl>

 

 




