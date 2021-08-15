---
description: 深入瞭解： JetCreateDatabase 函數
title: JetCreateDatabase 函式
TOCTitle: JetCreateDatabase Function
ms:assetid: 2b13b038-1694-46d8-b903-9be64384cb06
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269212(v=EXCHG.10)
ms:contentKeyID: 32765515
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateDatabase
- JetCreateDatabaseA
- JetCreateDatabaseW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 788c8e9fcc97d834843f42752d59cd6c8754fd49b99eac829ed5a68ae18cf287
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119358297"
---
# <a name="jetcreatedatabase-function"></a>JetCreateDatabase 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetcreatedatabase-function"></a>JetCreateDatabase 函式

**JetCreateDatabase** 函式會建立和附加資料庫檔案，以搭配 ESE 資料庫引擎使用。 將 *cpgDatabaseSizeMax* 設定為零的呼叫 [JetCreateDatabase2](./jetcreatedatabase2-function.md)等同于呼叫 **JetCreateDatabase** ，並將 *szConnect* 設定為 Null。 目前，每個實例最多可以建立七個資料庫。

```cpp
    JET_ERR JET_API JetCreateDatabase(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szFilename,
      __in_opt      JET_PCSTR szConnect,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

要用於 API 呼叫的資料庫會話內容。

*szFilename*

要建立之資料庫的名稱。

*szConnect*

保留供未來使用。 設定為 NULL。

*pdbid*

在成功呼叫時，緩衝區的指標，其中包含資料庫的識別碼。 失敗時，值為未定義。

*grbit*

指定零或多個下列選項的位群組。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>值</p></th>
<th><p>意義</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitDbOverwriteExisting</p></td>
<td><p>根據預設，如果呼叫 <strong>JetCreateDatabase</strong> ，而且資料庫已存在，則 API 呼叫將會失敗，而且不會覆寫原始資料庫。 JET_bitDbOverwriteExisting 變更這種行為，舊資料庫將會以新的資料庫覆寫。 WindowsXP 和更新版本。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDbRecoveryOff</p></td>
<td><p>JET_bitDbRecoveryOff 關閉記錄功能。 如此一來，在發生重大事件之後，就無法重新執行記錄檔並將資料庫復原到一致的可用狀態。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitDbShadowingOff</p></td>
<td><p>設定 JET_bitDbShadowingOff 將會停用部分內部資料庫結構 (遮蔽) 的複製。 這些結構的複製是為了復原而完成，因此設定 JET_bitDbShadowingOff 將會移除該復原。</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>傳回碼</p></th>
<th><p>描述</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>作業已成功完成。</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseDuplicate</p></td>
<td><p><em>SzFilename</em>中名為的資料庫已經存在。 傳回此錯誤時，就不會附加資料庫。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInUse</p></td>
<td><p>如果要求獨佔存取權，但無法授與，或是其他會話已獨佔開啟資料庫，則可以傳回。</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInvalidPages</p></td>
<td><p>當 <em>cpgDatabaseSizeMax</em> 大於資料庫中允許的最大頁面數目時傳回。 目前的最大值為 2147483646 (0x7ffffffe) 。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidPath</p></td>
<td><p><em>SzFilename</em>中提供了不正確路徑。 <em>szFilename</em> 必須為非 Null。 根據預設， <em>szFilename</em> 必須指向存在的目錄。 如果設定 <em>JET_paramCreatePathIfNotExist</em> ，則會建立路徑 (請參閱 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>) 。</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseLocked</p></td>
<td><p>指出另一個會話已 (使用 JET_bitDbExclusive) ，以獨佔方式開啟資料庫。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseNotFound</p></td>
<td><p>先前尚未附加資料庫 (請參閱 <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>) 。</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseSharingViolation</p></td>
<td><p>已由不同的會話附加資料庫檔案。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction</p></td>
<td><p>嘗試在交易中建立資料庫。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabase</p></td>
<td><p>嘗試開啟的檔案不是有效的資料庫檔案。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOneDatabasePerSession</p></td>
<td><p>嘗試開啟一個以上的資料庫，並已設定 JET_paramOneDatabasePerSession。 請參閱 <a href="gg269337(v=exchg.10).md">資料庫參數</a>。</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>因為無法配置記憶體，所以操作失敗。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyAttachedDatabases</p></td>
<td><p>每個實例只能附加有限數量的資料庫。 限制目前為每個實例七個資料庫。</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDatabaseAttached</p></td>
<td><p>非嚴重警告，指出此會話已附加資料庫檔案。</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnFileOpenReadOnly</p></td>
<td><p>JET_wrnFileOpenReadOnly 指出檔案已附加唯讀，但 <strong>JetCreateDatabase</strong> 未傳遞 JET_bitDbReadOnly。 資料庫仍會以唯讀存取權開啟。</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>備註

如果 *szFilename* 中指定的資料庫存在，而且未傳入 JET_BITDBOVERWRITEEXISTING，API 呼叫將會失敗。 如果傳入了 JET_bitDbOverwriteExisting，將會先刪除舊的資料庫檔案。

如果 API 建立資料庫檔案，然後遇到另一個錯誤，則會清除並刪除該檔案。

**JetCreateDatabase** 會以隱含方式開啟資料庫。 這不一定會再呼叫 [JetOpenDatabase](./jetopendatabase-function.md)。

#### <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>用戶端</strong></p></td>
<td><p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p></td>
</tr>
<tr class="even">
<td><p><strong>伺服器</strong></p></td>
<td><p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p></td>
</tr>
<tr class="odd">
<td><p><strong>標頭</strong></p></td>
<td><p>宣告于 Esent. h 中。</p></td>
</tr>
<tr class="even">
<td><p><strong>程式庫</strong></p></td>
<td><p>使用 ESENT。</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>需要 ESENT.dll。</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>實作為 <strong>JetCreateDatabaseW</strong> (Unicode) 和 <strong>JetCreateDatabaseA</strong> (ANSI) 。</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>另請參閱

[可擴充的儲存體引擎檔案](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_DBID](./jet-dbid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCreateDatabase2](./jetcreatedatabase2-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[系統參數](./extensible-storage-engine-system-parameters.md)
