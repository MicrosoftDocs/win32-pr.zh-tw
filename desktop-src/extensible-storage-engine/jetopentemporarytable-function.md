---
description: 深入瞭解： JetOpenTemporaryTable 函數
title: JetOpenTemporaryTable 函式
TOCTitle: JetOpenTemporaryTable Function
ms:assetid: feacd0b8-2298-4ec6-aa59-0fede08474bc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294144(v=EXCHG.10)
ms:contentKeyID: 32765758
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTemporaryTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2335f6d6426b321d5db55b4ed005c6220484d509
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975813"
---
# <a name="jetopentemporarytable-function"></a>JetOpenTemporaryTable 函式


_**適用于：** Windows |Windows Server_

## <a name="jetopentemporarytable-function"></a>JetOpenTemporaryTable 函式

**JetOpenTemporaryTable** 函式會建立一個具有單一索引的 volatile 資料表，可用來儲存和取出記錄，就像透過 [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)建立的一般資料表一樣。

**Windows vista：**  **JetOpenTemporaryTable** 是在 windows vista 中引進的。

臨時表比一般資料表快很多，因為它們是暫時性的本質。 當記錄集以純粹順序的方式存取時，它們可以快速排序並執行重複的移除。

```cpp
    JET_ERR JET_API JetOpenTemporaryTable(
      __in          JET_SESID sesid,
      __in          JET_OPENTEMPORARYTABLE* popentemporarytable
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫將使用的會話。

*popentemporarytable*

[JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-structure.md)結構的指標，其中包含要在輸入上建立之臨時表的描述。 在成功呼叫之後，結構會包含臨時表和資料行標識的控制碼。

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
<td><p>JET_errOutOfMemory</p></td>
<td><p>作業失敗，因為無法配置足夠的記憶體來完成。</p>
<p>如果主機進程的位址空間變得太分散， <strong>JetOpenTemporaryTable</strong>可能會傳回 JET_errOutOfMemory。 無論儲存的資料量為何，臨時表管理員都會為每個建立的臨時表配置 1 MB 的位址空間區塊。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>其中一個提供的參數包含未預期的值，或數個參數值的組合導致非預期的結果。</p>
<p>在下列情況下， <strong>JetOpenTemporaryTable</strong> 會傳回此錯誤：</p>
<ul>
<li><p><a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a>結構的<strong>cbStruct</strong>成員未對應到該版本的 database engine 所支援的這個結構版本</p></li>
<li><p><a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a>結構的<strong>cbKeyMost</strong>成員小於 JET_cbKeyMostMin。</p></li>
<li><p><a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a>結構的<strong>cbKeyMost</strong>成員大於實例 (JET_paramDatabasePageSize) 之資料庫頁面大小的最大支援值。 如需詳細資訊，請參閱 <a href="gg269241(v=exchg.10).md">資訊參數</a> 清單中的 JET_paramKeyMost 參數。</p></li>
<li><p><a href="gg269206(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a>結構的 cbVarSegMac 成員大於<strong>cbKeyMost</strong>成員。</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p>
<p><strong>WINDOWS XP：</strong>  只有 Windows XP 和更新版本才會傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在關閉中。</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>作業無法完成，因為與會話相關聯的實例正在進行還原作業。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>相同的會話無法同時用於一個以上的執行緒。</p>
<p><strong>WINDOWS XP：</strong>  只有 Windows XP 和更新版本才會傳回此錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSesid</p></td>
<td><p>會話控制碼無效或參考已關閉的會話。</p>
<p><strong>注意</strong>  在所有情況下，都不會傳回此錯誤。 控制碼只會根據最大努力進行驗證。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfCursors</p></td>
<td><p>作業失敗，因為引擎無法配置開啟新資料指標所需的資源。 資料指標資源是使用 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 搭配 <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>進行設定。</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManySorts</p></td>
<td><p>作業失敗，因為引擎無法配置建立臨時表所需的資源。 臨時表資源是使用 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 搭配 <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>進行設定。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotMaterializeForwardOnlySort</p></td>
<td><p><strong>JetOpenTemporaryTable</strong> 失敗，因為指定了 JET_bitTTForwardOnly，而且無法使用順向優化來建立指定的臨時表。</p>
<p><strong>Windows Server 2003：</strong>  只有 Windows Server 2003 和更新版本才會傳回此錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyColumns</p></td>
<td><p>嘗試將過多的資料行新增至資料表。 資料表不能超過 JET_ccolFixedMost 固定資料行，不能超過 JET_ccolVarMost 的可變長度資料行，且不能超過 JET_ccolTaggedMost 標記的資料行。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenTables</p></td>
<td><p>作業失敗，因為引擎無法配置快取資料表架構所需的資源。 若要設定具有可快取之架構的資料表數目，請使用 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 搭配 <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCodePage</p></td>
<td><p><a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>結構的<strong>cp</strong>成員未設定為有效的字碼頁。 Text 資料行的唯一有效值是英文 (1252) 和 Unicode (1200) 。 0值表示預設值將使用 (英文、1252) 。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p><a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>的<strong>coltyp</strong>成員未設定為有效的資料行類型。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>無法建立索引，因為嘗試使用不正確地區設定識別碼。 地區設定識別碼可能完全無效，或可能未安裝相關聯的語言套件。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidLCMapStringFlags</p></td>
<td><p>無法建立索引，因為嘗試使用一組不正確正規化旗標。</p>
<p><strong>WINDOWS XP：</strong>  只有 Windows XP 和更新版本才會傳回此錯誤。</p>
<p><strong>Windows 2000：</strong>  在 Windows 2000 上，不正確正規化旗標會導致 JET_errIndexInvalidDef。</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInvalidDef</p></td>
<td><p>無法建立索引，因為指定了不正確索引定義。 <strong>JetOpenTemporaryTable</strong> 會在下列情況下傳回此錯誤：</p>
<ul>
<li><p>指定了中性語言的地區設定。</p></li>
<li><p>指定了不正確正規化旗標集合。</p></li>
</ul>
<p><strong>Windows 2000：</strong>  此錯誤只會由 Windows 2000 傳回。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenIndexes</p></td>
<td><p>作業失敗，因為引擎無法配置快取資料表索引所需的資源。 若要設定具有可快取之架構的索引數目，請使用 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 搭配 <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>。</p></td>
</tr>
</tbody>
</table>


成功時，會傳回在新建立的臨時表上開啟的資料指標。 暫存資料庫的狀態將準備好包含新的臨時表。 資料庫引擎所使用之任何一般資料庫的狀態將保持不變。

失敗時，將不會建立臨時表，也不會傳回資料指標。 暫存資料庫的狀態可以變更。 資料庫引擎所使用之任何一般資料庫的狀態將保持不變。

#### <a name="remarks"></a>備註

臨時表不支援資料庫引擎通常支援之資料行定義選項的完整補充。 事實上，只支援 JET_bitColumnFixed 和 JET_bitColumnTagged。 這表示不可能在臨時表中建立自動遞增、版本或多重值資料行。 最後，不支援保管更新資料行，因為一次只能由一個會話使用。 如果要求這些選項中的任何一項，則會忽略這些選項。

臨時表不支援預設值。 如果提供的資料行定義包含預設值規格，則會忽略該規格。

由於許多不同的 ESE 函數，臨時表會傳回給呼叫端。 例如，JET_IdxInfo 選項組的 [JetGetIndexInfo](./jetgetindexinfo-function.md) 會傳回臨時表，其中包含給定索引中所有索引鍵資料行的清單。 臨時表會遵循與一般臨時表相同的生命週期規則，如下所述。

資料庫引擎也會在內部使用臨時表來進行許多工。 這些工作中最重要的就是在現有的資料表上建立索引。 臨時表將用來排序用來建立索引的索引鍵。

所有臨時表都會儲存在暫存資料庫中。 暫存資料庫是一個特殊的資料庫檔案，會在 ESE 實例的存留期內進行維護，當該實例關閉或重新開機時，就會將其刪除。 您可以使用 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 搭配 [JET_paramTempPath](./temporary-database-parameters.md)來設定暫存資料庫的位置。 如果您的應用程式大量使用臨時表或經常建立索引，則相對於交易記錄檔和資料庫檔案的暫存資料庫放置在磁片上可能很重要。

臨時表的生命週期會系結至參考它的資料指標。 如果參考臨時表的所有資料指標都是以隱含或明確的方式關閉，則會刪除臨時表。 如果在交易內建立臨時表，而且之後復原該交易，則會刪除該臨時表，因為此時參考該資料表的任何資料指標都會以隱含方式關閉。 新的資料指標只能透過使用 [JetDupCursor](./jetdupcursor-function.md)來參考臨時表。 在此情況下，新的資料指標將定位於臨時表的第一個索引項目目。 [JetDupCursor](./jetdupcursor-function.md) 僅適用于臨時表的特定使用階段。 如需詳細資訊，請參閱關於臨時表資料指標功能的備註。 一次只能從一個以上的會話參考臨時表。

**注意** [JetDupCursor](./jetdupcursor-function.md) 中有一個會影響臨時表的重要問題。 如果嘗試複製處於順向模式的臨時表，則會無法正確建立產生的資料指標，而且會發生故障。 在具體化的臨時表上重復資料指標仍然是安全的。

臨時表管理員可以用三種方式來執行臨時表。 第一個方法是維護記憶體中的資料表。 這是最快的策略，但只能用於小型、簡單的臨時表。 第二種方法是建立以磁片為基礎的排序，該排序可使用順向反覆運算器驅動。 這項策略只能在特定情況下使用，而且是從非常大的資料集排序和移除重複專案的最快速方式。 第三種方法是在暫存資料庫中建立 B + 樹狀結構，以保存臨時表。 這個策略是最慢的，但最多用途，而且稱為具體化臨時表。 這些策略可以組合使用，以最終達成臨時表所要求的功能。

當臨時表未具體化時，主要是在兩個主要階段中使用。 第一個階段是插入階段，其中資料表會填入其初始資料集。 在這個階段中，只允許插入資料。 當嘗試使用 [JetMove](./jetmove-function.md) 或 [JetSeek](./jetseek-function.md)移動資料指標時，就會結束這個階段。 第二個階段是資料解壓縮階段。 在這個階段中，您可以根據建立臨時表時所要求的功能，來解壓縮儲存在臨時表中的資料。

**臨時表資料指標功能**

當臨時表具體化時，資料指標有下列功能，但可能會進一步受要求的選項限制：

  - [JetCloseTable](./jetclosetable-function.md)

  - [JetDelete](./jetdelete-function.md)

  - [JetDupCursor](./jetdupcursor-function.md)

  - [JetEnumerateColumns](./jetenumeratecolumns-function.md)

  - [JetEscrowUpdate](./jetescrowupdate-function.md)

  - [JetGetBookmark](./jetgetbookmark-function.md)

  - [JetGetCursorInfo](./jetgetcursorinfo-function.md)

  - [JetGetLS](./jetgetls-function.md)

  - [JetGetRecordSize](./jetgetrecordsize-function.md)

  - [JetGetTableInfo](./jetgettableinfo-function.md)

  - [JetGotoBookmark](./jetgotobookmark-function.md)

  - [JetMakeKey](./jetmakekey-function.md)

  - [JetMove](./jetmove-function.md)

  - [JetPrepareUpdate](./jetprepareupdate-function.md)

  - [JetRetrieveColumn](./jetretrievecolumn-function.md)

  - [JetRetrieveColumns](./jetretrievecolumns-function.md)

  - [JetRetrieveKey](./jetretrievekey-function.md)

  - [JetSeek](./jetseek-function.md)

  - [JetSetColumn](./jetsetcolumn-function.md)

  - [JetSetColumns](./jetsetcolumns-function.md)

  - [JetSetIndexRange](./jetsetindexrange-function.md)

  - [JetSetLS](./jetsetls-function.md)

  - [JetUpdate](./jetupdate-function.md)

當臨時表未具體化且在插入階段時，資料指標有下列功能，但可能會進一步受要求的選項限制：

  - [JetCloseTable](./jetclosetable-function.md)

  - [JetEscrowUpdate](./jetescrowupdate-function.md)

  - [JetMakeKey](./jetmakekey-function.md)

  - [JetMove](./jetmove-function.md)
    
    **注意**  導致轉換成解壓縮階段。

  - [JetPrepareUpdate](./jetprepareupdate-function.md)

  - [JetRetrieveKey](./jetretrievekey-function.md)

  - [JetSeek](./jetseek-function.md)
    
    **注意**  導致轉換成解壓縮階段。

  - [JetSetColumn](./jetsetcolumn-function.md)

  - [JetSetColumns](./jetsetcolumns-function.md)

  - [JetUpdate](./jetupdate-function.md)

當臨時表未具體化而且在解壓縮階段時，資料指標有下列功能，但可能會進一步受要求的選項限制：

  - [JetCloseTable](./jetclosetable-function.md)

  - [JetDupCursor](./jetdupcursor-function.md)
    
    **注意**  如果嘗試複製處於順向模式的臨時表，則會無法正確建立產生的資料指標，而且會發生故障。 在具體化的臨時表上重復資料指標仍然是安全的。

  - [JetEnumerateColumns](./jetenumeratecolumns-function.md)

  - [JetGetBookmark](./jetgetbookmark-function.md)

  - [JetGetLS](./jetgetls-function.md)

  - [JetGetRecordSize](./jetgetrecordsize-function.md)

  - [JetGetTableInfo](./jetgettableinfo-function.md)

  - [JetGotoBookmark](./jetgotobookmark-function.md)

  - [JetMakeKey](./jetmakekey-function.md)

  - [JetMove](./jetmove-function.md)

  - [JetRetrieveColumn](./jetretrievecolumn-function.md)

  - [JetRetrieveColumns](./jetretrievecolumns-function.md)

  - [JetRetrieveKey](./jetretrievekey-function.md)

  - [JetSeek](./jetseek-function.md)

  - [JetSetIndexRange](./jetsetindexrange-function.md)

  - [JetSetLS](./jetsetls-function.md)

#### <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>用戶端</strong></p></td>
<td><p>需要 Windows Vista。</p></td>
</tr>
<tr class="even">
<td><p><strong>伺服器</strong></p></td>
<td><p>需要 Windows Server 2008。</p></td>
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
</tbody>
</table>


#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-structure.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetDupCursor](./jetdupcursor-function.md)  
[JetMove](./jetmove-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[資訊參數](./informational-parameters.md)  
[暫存資料庫參數](./temporary-database-parameters.md)
