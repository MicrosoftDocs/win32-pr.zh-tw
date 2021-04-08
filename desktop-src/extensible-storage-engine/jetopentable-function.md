---
description: 深入瞭解： JetOpenTable 函數
title: JetOpenTable 函式
TOCTitle: JetOpenTable Function
ms:assetid: ded6348c-a82a-49bc-8a5d-e40ed5d6315c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294118(v=EXCHG.10)
ms:contentKeyID: 32765732
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTable
- JetOpenTableW
- JetOpenTableA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7a3ffe9490b75606910c5867d3e8b59d9a8c520d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689531"
---
# <a name="jetopentable-function"></a>JetOpenTable 函式


_**適用于：** Windows |Windows Server_

## <a name="jetopentable-function"></a>JetOpenTable 函式

**JetOpenTable** 函數會在先前建立的資料表上開啟資料指標。

```cpp
    JET_ERR JET_API JetOpenTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in_opt      const void* pvParameters,
      __in          unsigned long cbParameters,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid
    );
```

### <a name="parameters"></a>參數

*sesid*

要使用的資料庫會話內容。

*dbid*

用來尋找資料表的資料庫識別碼。

*szTableName*

要開啟之資料表的名稱。

*pvParameters*

已取代。 設定為 **Null**。

*cbParameters*

已取代。 設定為 0 (零) 。

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
<td><p>JET_bitTableDenyRead</p></td>
<td><p>資料表無法由另一個資料庫會話開啟以供讀取存取。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableDenyWrite</p></td>
<td><p>資料表無法由另一個資料庫會話開啟以供寫入存取。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableNoCache</p></td>
<td><p>不要快取此資料表的頁面。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTablePermitDDL</p></td>
<td><p>允許對標示為 FixedDDL 的資料表進行 DDL 修改。 此選項必須與 JET_bitTableDenyRead 選項搭配使用。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTablePreread</p></td>
<td><p>提供資料表可能不在緩衝區快取中的提示，而且預先讀取可能會對效能有所説明。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableReadOnly</p></td>
<td><p>要求資料表的唯讀存取權。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableSequential</p></td>
<td><p>因為應用程式會依序掃描，所以資料表應該非常積極地從磁片中預先提取。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableUpdatable</p></td>
<td><p>要求資料表的寫入存取權。</p></td>
</tr>
</tbody>
</table>


*ptableid*

成功時，指向資料表的識別碼。 失敗時， *ptableid* 的內容是未定義的。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>傳回碼</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>作業已成功完成。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabaseId</p></td>
<td><p><em>dbid</em> 不是有效的資料庫識別碼。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>傳入了不正確的 <em>grbit</em> 組合。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p><em>SzTableName</em>中提供的名稱無效。</p>
<p>如需有效資料表名稱的詳細資訊，請參閱<a href="gg269210(v=exchg.10).md">JetCreateTable</a>中的<em>szTableName</em>參數。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errObjectNotFound</p></td>
<td><p>嘗試開啟不存在於資料庫中的資料表。</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfCursors</p></td>
<td><p>作業失敗，因為引擎無法配置開啟新資料指標所需的資源。 請參閱＜備註＞一節。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableInUse</p></td>
<td><p>資料表正由另一個資料庫作業使用中。</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnTableInUseBySystem</p></td>
<td><p>非嚴重警告，指出系統正在使用該資料表。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableLocked</p></td>
<td><p>資料表已由另一個資料庫操作鎖定。</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenTables</p></td>
<td><p>嘗試一次開啟太多唯一資料表。 請參閱＜備註＞一節。</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>備註

使用 **JetOpenTable** 開啟的資料表通常應該以 [JetCloseTable](./jetclosetable-function.md)關閉。 在交易中呼叫 **JetOpenTable** 時，就會發生此規則的例外狀況，且會使用 [JetRollback](./jetrollback-function.md)) 將交易回復 (。 回復交易時，資料表會自動關閉。 在此情況下，使用 [JetCloseTable](./jetclosetable-function.md)關閉資料表是錯誤的。

以 **JetOpenTable** (（例如 MSysObjects、MSysUnicodeFixup) ）來開啟系統資料表是合法的。 系統資料表的架構可能會變更，因此不建議存取系統資料表。 可以同時開啟的唯一資料表數目，會直接受到 *JET_paramMaxOpenTables* 的影響。 如果資料表目前為開啟狀態，則會在資料表上建立新的資料指標。 資料指標資源是使用 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 搭配 *JET_paramMaxCursors* 進行設定。 另請參閱 [JetDupCursor](./jetdupcursor-function.md)。

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
<td><p>需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</p></td>
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
<td><p>實作為 <strong>JetOpenTableW</strong> (Unicode) 和 <strong>JetOpenTableA</strong> (ANSI) 。</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetDupCursor](./jetdupcursor-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[資源參數](./resource-parameters.md)
