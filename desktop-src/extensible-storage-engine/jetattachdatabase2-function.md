---
description: 深入瞭解： JetAttachDatabase2 函數
title: JetAttachDatabase2 函式
TOCTitle: JetAttachDatabase2 Function
ms:assetid: 8667f3fc-d178-49f1-9474-f09352614f92
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269322(v=EXCHG.10)
ms:contentKeyID: 32765612
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAttachDatabase2A
- JetAttachDatabase2
- JetAttachDatabase2W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 02f896d41c5804fd85a3cb5f31b6c509c3099357
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983521"
---
# <a name="jetattachdatabase2-function"></a>JetAttachDatabase2 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetattachdatabase2-function"></a>JetAttachDatabase2 函式

**JetAttachDatabase2** 函式會附加資料庫檔案，以便與資料庫實例搭配使用，並指定該資料庫的大小上限。 若要使用資料庫，就必須使用 [JetOpenDatabase](./jetopendatabase-function.md)來開啟它。

```cpp
    JET_ERR JET_API JetAttachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          const unsigned long cpgDatabaseSizeMax,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

將用於 API 呼叫的資料庫會話內容。

*szFilename*

要附加的資料庫名稱。

*cpgDatabaseSizeMax*

資料庫的大小上限（資料庫頁面）。 預設資料庫頁面大小為 4 kb，在建立資料庫之前，可以使用 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 函數來變更。

傳遞零表示資料庫引擎沒有強制執行的最大值。

*grbit*

位群組，其中包含要用於此呼叫的選項，其中包含零或多個下列各項：


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitDbDeleteCorruptIndexes</p> | <p>如果已設定 <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> ，將會刪除 Unicode 資料上的所有索引。 如需詳細資訊，請參閱＜備註＞一節。</p> | 
| <p>JET_bitDbDeleteUnicodeIndexes</p> | <p>無論 <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>的設定為何，都將刪除所有 Unicode 資料的索引。 如需詳細資訊，請參閱＜備註＞一節。</p> | 
| <p>JET_bitDbReadOnly</p> | <p>防止修改資料庫。</p> | 
| <p>JET_bitDbUpgrade</p> | <p>保留供未來使用。</p> | 



### <a name="return-value"></a>傳回值

函數會傳回其中一個 [JET_ERR](./jet-err.md) 錯誤碼。 以下是最常傳回的。  (如需此 API 的完整錯誤清單，請參閱[可擴展儲存體引擎錯誤碼](./extensible-storage-engine-error-codes.md)。 ) 


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errBackupInProgress</p> | <p>在備份期間，不允許附加資料庫。</p> | 
| <p>JET_errDatabaseFileReadOnly</p> | <p><em>SzFilename</em>所指定的資料庫檔案必須是可寫入的。 不能設定 Read-Only 屬性，而且執行中的進程必須有足夠的許可權可寫入檔案。</p> | 
| <p>JET_errDatabaseInUse</p> | <p>資料庫檔案已經由另一個進程開啟。</p> | 
| <p>JET_errDatabaseInvalidPath</p> | <p><em>SzFilename</em>中提供了不正確路徑。 <em>szFilename</em> 必須為非 Null，並參考有效的路徑。</p> | 
| <p>JET_errDatabaseSharingViolation</p> | <p>已由不同的會話附加資料庫檔案。</p> | 
| <p>JET_errFileNotFound</p> | <p><em>SzFilename</em>中提供的檔案不存在。</p> | 
| <p>JET_errPrimaryIndexCorrupted</p> | <p>主要索引發生錯誤。 這可能是因為物理損毀 (例如磁片或記憶體損毀) 。 當附加資料庫上次修改較舊的作業系統，而且主要索引是在具有 Unicode 資料的資料行上時，也可能會傳回它。 如需 Unicode 資料之索引的詳細資訊，請參閱備註。</p> | 
| <p>JET_errSecondaryIndexCorrupted</p> | <p>次要索引發生錯誤。 這可能是因為物理損毀 (例如磁片或記憶體損毀) 。 當附加資料庫上次修改于較舊的作業系統上，而且次要索引是在具有 Unicode 資料的資料行上時，也可能會傳回它。 如需 Unicode 資料之索引的詳細資訊，請參閱備註。 使用下列命令，以離線公用程式重新整理資料庫時，會完整重建次要索引： <strong>esentutl-d</strong>。</p> | 
| <p>JET_errTooManyAttachedDatabases</p> | <p>每個實例只能附加有限數量的資料庫。 限制目前為每個實例七個資料庫。</p> | 
| <p>JET_wrnDatabaseAttached</p> | <p>非嚴重警告，指出此會話已附加資料庫檔案。</p> | 



#### <a name="remarks"></a>備註

使用 [JetDetachDatabase](./jetdetachdatabase-function.md) 或 [JetDetachDatabase2](./jetdetachdatabase2-function.md)卸離資料庫檔案。

如需備註，請參閱 [JetAttachDatabase](./jetattachdatabase-function.md) 。

#### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 
| <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | 
| <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 
| <p><strong>Unicode</strong></p> | <p>實作為 <strong>JetAttachDatabase2W</strong> (Unicode) 和 <strong>JetAttachDatabase2A</strong> (ANSI) 。</p> | 



#### <a name="see-also"></a>另請參閱

[可擴充的儲存體引擎檔案](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
