---
description: 深入瞭解： JetAttachDatabase 函數
title: JetAttachDatabase 函式
TOCTitle: JetAttachDatabase Function
ms:assetid: bc4c9a76-203c-424a-ac17-f096e3a6e04e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294074(v=EXCHG.10)
ms:contentKeyID: 32765689
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAttachDatabase
- JetAttachDatabaseW
- JetAttachDatabaseA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b07312cbfce36b450fe39a39810813adc2d0fd4
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987701"
---
# <a name="jetattachdatabase-function"></a>JetAttachDatabase 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetattachdatabase-function"></a>JetAttachDatabase 函式

**JetAttachDatabase** 函數會附加資料庫檔案，以便與資料庫實例搭配使用。 若要使用資料庫，就必須使用 [JetOpenDatabase](./jetopendatabase-function.md)來開啟它。

```cpp
    JET_ERR JET_API JetAttachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

要用於 API 呼叫的資料庫會話內容。

*szFilename*

要附加的資料庫名稱。

*grbit*

指定零或多個下列選項的位群組。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitDbDeleteCorruptIndexes</p> | <p>如果已設定 <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> ，將會刪除 Unicode 資料上的所有索引。 如需詳細資訊，請參閱＜備註＞一節。</p> | 
| <p>JET_bitDbDeleteUnicodeIndexes</p> | <p>無論 <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>的設定為何，都將刪除所有 Unicode 資料的索引。 如需詳細資訊，請參閱＜備註＞一節。</p> | 
| <p>JET_bitDbUpgrade</p> | <p>已過時。 請勿使用。</p> | 
| <p>JET_bitDbReadOnly</p> | <p>防止修改資料庫。</p> | 



### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errBackupInProgress</p> | <p>在備份期間，不允許附加資料庫。</p> | 
| <p>JET_errDatabaseFileReadOnly</p> | <p><em>SzFilename</em>所指定的資料庫檔案必須是可寫入的。 不能設定 Read-Only 屬性，而且執行中的進程必須有足夠的許可權可寫入檔案。</p> | 
| <p>JET_errDatabaseInUse</p> | <p>資料庫檔案已經由另一個進程開啟。</p> | 
| <p>JET_errDatabaseInvalidPath</p> | <p><em>SzFilename</em>中提供了不正確路徑。 <em>szFilename</em> 必須為非 Null，並參考有效的路徑。</p> | 
| <p>JET_errDatabaseSharingViolation</p> | <p>已由不同的會話附加資料庫檔案。</p> | 
| <p>JET_errFileAccessDenied</p> | <p>資料庫引擎無法開啟資料庫檔案。 檔案可能由另一個進程使用中，或呼叫者可能沒有足夠的許可權可以開啟檔案。</p> | 
| <p>JET_errFileNotFound</p> | <p><em>SzFilename</em>中提供的檔案不存在。</p> | 
| <p>JET_errPrimaryIndexCorrupted</p> | <p>主要索引發生錯誤。 這可能是因為物理損毀 (例如磁片或記憶體損毀) 。 當附加資料庫上次修改較舊的作業系統，而且主要索引是在具有 Unicode 資料的資料行上時，也可能會傳回它。 如需 Unicode 資料之索引的詳細資訊，請參閱備註。</p> | 
| <p>JET_errSecondaryIndexCorrupted</p> | <p>次要索引發生錯誤。 這可能是因為物理損毀 (例如磁片或記憶體損毀) 。 當附加資料庫上次修改于較舊的作業系統上，而且次要索引是在具有 Unicode 資料的資料行上時，也可能會傳回它。 如需 Unicode 資料之索引的詳細資訊，請參閱備註。 使用下列命令，以離線公用程式重新整理資料庫時，會完整重建次要索引： <strong>esentutl-d</strong>。</p> | 
| <p>JET_errTooManyAttachedDatabases</p> | <p>每個實例只能附加有限數量的資料庫。 限制目前為每個實例七個資料庫。</p> | 
| <p>JET_wrnDatabaseAttached</p> | <p>非嚴重警告，指出此會話已附加資料庫檔案。</p> | 



#### <a name="remarks"></a>備註

呼叫 **JetAttachDatabase** 相當於呼叫 [JetAttachDatabase2](./jetattachdatabase2-function.md) 並傳遞零值，這表示 *cpgDatabaseSizeMax* 參數沒有限制。

附加可寫入的資料庫 (也就是，如果未在 *grbit* 參數中指定 JET_bitDbReadOnly) 將會以獨佔方式在作業系統層級開啟檔案。 沒有其他進程可以開啟檔案。 多個進程可以在唯讀模式中開啟單一資料庫，以附加單一資料庫。

使用 [JetDetachDatabase](./jetdetachdatabase-function.md) 或 [JetDetachDatabase2](./jetdetachdatabase2-function.md)卸離資料庫檔案。

索引檢查參數

不同版本的 Windows 會以不同的方式將 Unicode 文字標準化。 這表示在某個 Windows 版本下建立的索引可能無法在其他版本上運作。

在 Windows Server 2003 之前，當作業系統版本變更 (包括) 安裝 Service Pack 時，每個 Unicode 資料的索引都處於可能已損毀的狀態。

在 Windows Server 2003 和更新版本中建立的索引，會以用來建立它們的 Unicode 正規化版本來標示。 較舊的索引不含任何版本資訊。 大部分的 Unicode 正規化變更都包含新增字元，先前未定義的程式碼點現在已定義並以不同的方式進行標準化。 因此，如果二進位資料儲存在 Unicode 資料行中，則在定義新的程式碼點時，它會以不同的方式進行標準化。

從 Windows Server 2003，ESE 資料庫引擎會追蹤包含未定義程式碼點的 Unicode 索引項目。 當定義的 Unicode 字元集合變更時，可以使用這些方法來修正索引。

這些參數可控制當 ESE 資料庫引擎連接到最後在不同的作業系統組建下使用的資料庫時，會發生什麼事。 系統會在資料庫標頭中將作業系統版本加上戳記。

如果 [JET_paramEnableIndexChecking](./database-parameters.md) 設定為 **TRUE**，且資料庫包含可能已損毀的索引：

  - 如果 *grbit* 包含 JET_bitDbDeleteCorruptIndexes， **JetAttachDatabase** 會刪除可能損毀的索引

  - 如果 *grbit* 不包含 JET_bitDbDeleteCorruptIndexes，且有需要刪除的索引， **JetAttachDatabase** 會傳回錯誤。

如果 [JET_paramEnableIndexChecking](./database-parameters.md) 設定為 **FALSE**：

  - **JetAttachDatabase** 會忽略可能損毀的索引，並傳回 JET_errSuccess (假設沒有其他錯誤) 。

Windows伺服器2003和更新版本：如果[JET_paramEnableIndexChecking](./database-parameters.md)尚未重設，則會使用內部修復表格來修復索引項目。 這可能無法修正所有索引損毀，但對應用程式而言會是透明的。

如果資料庫附加為唯讀，則無法修正或刪除索引。 在此情況下，API 會改為傳回錯誤，例如 JET_errSecondaryIndexCorrupted 或 JET_errPrimaryIndexCorrupted。

#### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 
| <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | 
| <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 
| <p><strong>Unicode</strong></p> | <p>實作為 <strong>JetAddColumnW</strong> (Unicode) 和 <strong>JetAddColumnA</strong> (ANSI) 。</p> | 



#### <a name="see-also"></a>另請參閱

[可擴充的儲存體引擎檔案](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetDetachDatabase](./jetdetachdatabase-function.md)  
[JetDetachDatabase2](./jetdetachdatabase2-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
