---
description: 深入瞭解： JetCreateDatabase2 函數
title: JetCreateDatabase2 函式
TOCTitle: JetCreateDatabase2 Function
ms:assetid: 267ac69f-49d3-4741-b324-d8510d7a36d3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269208(v=EXCHG.10)
ms:contentKeyID: 32765511
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateDatabase2A
- JetCreateDatabase2W
- JetCreateDatabase2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b362b7ada2c0cc2924ce178adda2368faef770bf
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479204"
---
# <a name="jetcreatedatabase2-function"></a>JetCreateDatabase2 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetcreatedatabase2-function"></a>JetCreateDatabase2 函式

**JetCreateDatabase2** 函式會建立並附加資料庫檔案，以便與具有指定資料庫大小上限的 ESE 資料庫引擎一起使用。 將 *cpgDatabaseSizeMax* 設定為零的呼叫 **JetCreateDatabase2** 等同于呼叫 [JetCreateDatabase](./jetcreatedatabase-function.md) ，並將 *szConnect* 設定為 Null。 目前最多可為每個實例建立7個資料庫。

```cpp
    JET_ERR JET_API JetCreateDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          const unsigned long cpgDatabaseSizeMax,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

要用於 API 呼叫的資料庫會話內容。

*szFilename*

要建立之資料庫的名稱。

*cpgDatabaseSizeMax*

資料庫的大小上限（資料庫頁面）。 預設資料庫頁面大小為 4 kb，在建立資料庫之前，您可以使用 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 加以變更。

傳遞零表示資料庫引擎沒有強制執行的最大值。

*pdbid*

在成功呼叫時，緩衝區的指標，其中包含資料庫的識別碼。 失敗時，值為未定義。

*grbit*

指定零或多個下列選項的位群組。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitDbOverwriteExisting</p> | <p>根據預設，如果呼叫 <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> 或 <strong>JetCreateDatabase2</strong> ，而且資料庫已存在，則 API 呼叫將會失敗，而且不會覆寫原始資料庫。 JET_bitDbOverwriteExisting 變更這種行為，舊資料庫將會以新的資料庫覆寫。 WindowsXP 和更新版本。</p> | 
| <p>JET_bitDbRecoveryOff</p> | <p>JET_bitDbRecoveryOff 關閉記錄功能。 如此一來，在發生重大事件之後，就無法重新執行記錄檔並將資料庫復原到一致的可用狀態。</p> | 
| <p>JET_bitDbShadowingOff</p> | <p>設定 JET_bitDbShadowingOff 將會停用部分內部資料庫結構 (遮蔽) 的複製。 這些結構的複製是為了復原而完成，因此設定 JET_bitDbShadowingOff 將會移除該復原。</p> | 



### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errDatabaseDuplicate</p> | <p><em>SzFilename</em>中名為的資料庫已經存在。 傳回此錯誤時，就不會附加資料庫。</p> | 
| <p>JET_errDatabaseInUse</p> | <p>如果要求獨佔存取權，但無法授與，或是其他會話已獨佔開啟資料庫，則可以傳回。</p> | 
| <p>JET_errDatabaseInvalidPages</p> | <p>當 <em>cpgDatabaseSizeMax</em> 大於資料庫中允許的最大頁面數目時傳回。 目前的最大值為 2147483646 (0x7ffffffe) 。</p> | 
| <p>JET_errDatabaseInvalidPath</p> | <p><em>SzFilename</em>中提供了不正確路徑。 <em>szFilename</em> 必須為非 Null。 根據預設， <em>szFilename</em> 必須指向存在的目錄。 如果設定 <em>JET_paramCreatePathIfNotExist</em> ，則會建立路徑 (請參閱 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>) 。</p> | 
| <p>JET_errDatabaseLocked</p> | <p>指出另一個會話已 (使用 JET_bitDbExclusive) ，以獨佔方式開啟資料庫。</p> | 
| <p>JET_errDatabaseNotFound</p> | <p>先前尚未附加資料庫 (請參閱 <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>) 。</p> | 
| <p>JET_errDatabaseSharingViolation</p> | <p>已由不同的會話附加資料庫檔案。</p> | 
| <p>JET_errInTransaction</p> | <p>嘗試在交易中建立資料庫。</p> | 
| <p>JET_errInvalidDatabase</p> | <p>嘗試開啟的檔案不是有效的資料庫檔案。</p> | 
| <p>JET_errOneDatabasePerSession</p> | <p>嘗試開啟一個以上的資料庫，並已設定 JET_paramOneDatabasePerSession。 請參閱 <a href="gg294139(v=exchg.10).md">系統參數</a>。</p> | 
| <p>JET_errOutOfMemory</p> | <p>系統資源不足。</p> | 
| <p>JET_errTooManyAttachedDatabases</p> | <p>每個實例只能附加有限數量的資料庫。 限制目前為每個實例七個資料庫。</p> | 
| <p>JET_wrnDatabaseAttached</p> | <p>非嚴重警告，指出此會話已附加資料庫檔案。</p> | 
| <p>JET_wrnFileOpenReadOnly</p> | <p>JET_wrnFileOpenReadOnly 指出檔案已附加唯讀，但 <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> 未傳遞 JET_bitDbReadOnly。 資料庫仍會以唯讀存取權開啟。</p> | 



#### <a name="remarks"></a>備註

如果 *szFilename* 中指定的資料庫存在，而且未傳入 JET_BITDBOVERWRITEEXISTING，API 呼叫將會失敗。 如果傳入了 JET_bitDbOverwriteExisting，將會先刪除舊的資料庫檔案。

如果 API 建立資料庫檔案，然後遇到另一個錯誤，則會清除並刪除該檔案。

**JetCreateDatabase2** 會以隱含方式開啟資料庫。 然後不需要呼叫 [JetOpenDatabase](./jetopendatabase-function.md)。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | | <p><strong>Unicode</strong></p> | <p>實作為 <strong>JetCreateDatabase2W</strong> (Unicode) 和 <strong>JetCreateDatabase2A</strong> (ANSI) 。</p> | 



#### <a name="see-also"></a>另請參閱

[可擴充的儲存體引擎檔案](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_DBID](./jet-dbid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[系統參數](./extensible-storage-engine-system-parameters.md)
