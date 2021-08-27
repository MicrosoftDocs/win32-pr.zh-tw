---
description: 深入瞭解： JetOpenTempTable 函數
title: JetOpenTempTable 函式
TOCTitle: JetOpenTempTable Function
ms:assetid: 29261333-a1bc-4159-9046-c32c36f47410
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269211(v=EXCHG.10)
ms:contentKeyID: 32765514
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTempTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a94af3f142fb7449a95ddf67ad9a0d16f2e37c43
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982401"
---
# <a name="jetopentemptable-function"></a>JetOpenTempTable 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetopentemptable-function"></a>JetOpenTempTable 函式

**JetOpenTempTable** 函式會建立具有單一索引的臨時表。 臨時表會儲存和抓取記錄，就像使用 [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)建立的一般資料表一樣。 不過，臨時表的速度會比一般資料表快許多，因為它們是暫時性的本質。 它們也可用來在以純粹順序存取的方式存取記錄集時，非常快速地排序和執行重複的移除。

```cpp
    JET_ERR JET_API JetOpenTempTable(
      __in          JET_SESID sesid,
      __in          const JET_COLUMNDEF* prgcolumndef,
      __in          unsigned long ccolumn,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid,
      __out         JET_COLUMNID* prgcolumnid
    );
```

### <a name="parameters"></a>參數

*sesid*

要使用的會話。

*prgcolumndef*

在臨時表中建立之資料行的資料行定義。

用於臨時表的資料行定義選項有 **重要** 的限制。 如需詳細資訊，請參閱＜備註＞一節。

除了一般資料行定義選項之外，也可以指定零或多個下列選項，這些選項只與臨時表的內容有關。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitColumnTTDescending</p> | <p>臨時表之索引鍵資料行的排序次序應該是遞減的，而不是遞增的。 如果指定這個選項但未指定 JET_bitColumnTTKey 則會忽略此選項。</p> | 
| <p>JET_bitColumnTTKey</p> | <p>資料行將是臨時表的索引鍵資料行。</p><p>在輸入陣列中指定此選項的資料行定義順序，將會決定臨時表的每個索引鍵資料行的優先順序。 陣列中具有這個選項組的第一個資料行定義將是最重要的索引鍵資料行，依此類推。 如果要求的索引鍵資料行數目超過 database engine 所能支援的數量，則會忽略不受支援索引鍵資料行的這個選項。</p> | 



*ccolumn*

請參閱 *prgcolumndef*。

*grbit*

指定零或多個下列選項的位群組。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitTTErrorOnDuplicateInsertion</p> | <p>任何嘗試插入具有與先前所插入記錄相同索引鍵的記錄，都會立即失敗，並 JET_errKeyDuplicate。 如果未要求這個選項，則會立即偵測到重複的情況，並會失敗，或根據資料庫引擎根據所要求的功能來執行臨時表所選擇的策略，以無訊息方式移除。</p><p>如果這項功能不是必要的，則最好不要要求它。 如果未要求這項功能，則臨時表管理員可能會選擇管理臨時表的策略，而這會導致效能改進。</p> | 
| <p>JET_bitTTForceMaterialization</p> | <p>強制臨時表管理員放棄搜尋，以使用管理將會導致效能提高的臨時表的最佳策略。</p> | 
| <p>JET_bitTTForwardOnly</p> | <p>只有當臨時表管理員可以使用針對中繼查詢結果優化的執行時，才會建立臨時表。 如果臨時表的任何特性會防止使用這項優化，則作業會失敗並 JET_errCannotMaterializeForwardOnlySort。</p><p>此選項的副作用是允許臨時表包含具有重複索引鍵的記錄。 如需詳細資訊，請參閱 JET_bitTTUnique。</p><p>此選項僅適用于 Windows Server 2003 和更新版本。</p> | 
| <p>JET_bitTTIndexed</p> | <p>此選項會要求臨時表具有足夠的彈性，可允許使用 <a href="gg294103(v=exchg.10).md">JetSeek</a> 依據索引鍵來查閱記錄。</p><p>如果這項功能不是必要的，則最好不要要求它。 如果未要求這項功能，則臨時表管理員可能會選擇管理臨時表的策略，而這會導致效能改進。</p> | 
| <p>JET_bitTTUnique</p> | <p>會從臨時表的最後一組記錄中，移除具有重複索引鍵的記錄。</p><p>在 Windows Server 2003 之前，資料庫引擎一律會假設這個選項有作用，因為所有叢集索引也必須是主鍵，因此必須是唯一的。 從 Windows Server 2003 開始，當也指定了 JET_bitTTForwardOnly 選項時，現在可以建立不會移除重複專案的臨時表。</p><p>一般情況下，不可能知道哪些複製成功，以及哪些重複專案會被捨棄。 不過，當要求 JET_bitTTErrorOnDuplicateInsertion 選項時，具有要插入至臨時表之指定索引鍵的第一個記錄一律會成功。</p> | 
| <p>JET_bitTTUpdatable</p> | <p>要求臨時表有足夠的彈性，可讓之前插入的記錄之後變更。 如果這項功能不是必要的，則最好不要要求它。</p><p>如果未要求這項功能，則臨時表管理員可能會選擇管理臨時表的策略，而這會導致效能改進。</p> | 
| <p>JET_bitTTScrollable</p> | <p>要求臨時表具有足夠的彈性，可讓您以任意順序和使用 <a href="gg294117(v=exchg.10).md">JetMove</a>的方向來掃描記錄。</p><p>如果不需要這項功能，最好不要要求。 如果未要求這項功能，則臨時表管理員可能會選擇管理臨時表的策略，而這會導致效能改進。</p> | 
| <p>JET_bitTTSortNullsHigh</p> | <p>要求 Null 索引鍵資料行值的排序比非 Null 索引鍵資料行值更接近索引的結尾。</p><p></p> | 
| <p>JET_bitTTIntrinsicLVsOnly</p> | <p>要求只允許內建的 long 值。</p><p><strong>Windows 7</strong>： <strong>JET_bitTTIntrinsicLVsOnly</strong>是 Windows 7 中引進的。</p> | 



*ptableid*

輸出緩衝區，會接收新建立的臨時表上開啟的新資料指標。

*prgcolumnid*

輸出緩衝區，接收在建立臨時表期間所產生的資料行識別碼陣列。

此陣列中的資料行識別碼，將會完全對應至資料行定義的輸入陣列。 因此，這個緩衝區的大小必須對應到輸入陣列的大小。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errCannotMaterializeForwardOnlySort</p> | <p><strong>JetOpenTempTable</strong> 失敗，因為指定了 JET_bitTTForwardOnly，而且無法使用順向優化來建立指定的臨時表。 只有 Windows Server 2003 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>無法建立索引，因為指定了不正確索引定義。</p><p><strong>JetOpenTempTable</strong> 會在下列情況傳回此錯誤：</p><ul><li><p>指定了中性語言的地區設定。</p></li><li><p>指定了不正確正規化旗標集合。</p></li></ul><p>只有 Windows 2000 才會傳回此錯誤。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errInvalidCodePage</p> | <p><a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>的 [cp] 欄位未設定為有效的字碼頁。 Text 資料行的唯一有效值是英文 (1252) 和 Unicode (1200) 。 0值表示預設值將使用 (英文、1252) 。</p> | 
| <p>JET_errInvalidColumnType</p> | <p><a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>的<em>coltyp</em>欄位未設定為有效的資料行類型。</p> | 
| <p>JET_errInvalidLanguageId</p> | <p>無法建立索引，因為嘗試使用不正確地區設定識別碼。 地區設定識別碼可能完全無效，或可能未安裝相關聯的語言套件。</p> | 
| <p>JET_errInvalidLCMapStringFlags</p> | <p>無法建立索引，因為嘗試使用一組不正確正規化旗標。 只有 Windows XP 和更新版本才會傳回此錯誤。 在 Windows 2000 上，不正確正規化旗標會改為產生 JET_errIndexInvalidDef。</p> | 
| <p>JET_errInvalidSesid</p> | <p>會話控制碼無效或參考已關閉的會話。</p><p><strong>注意</strong>  在所有情況下，都不會傳回此錯誤。 控制碼只會根據最大努力進行驗證。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errOutOfCursors</p> | <p>作業失敗，因為引擎無法配置開啟新資料指標所需的資源。 資料指標資源是使用 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 搭配 <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>進行設定。</p> | 
| <p>JET_errOutOfMemory</p> | <p>作業失敗，因為無法配置足夠的記憶體來完成。</p><p>如果主機進程的位址空間變得太分散， <strong>JetOpenTempTable</strong>可能會傳回 JET_errOutOfMemory。 無論要儲存的資料量為何，臨時表管理員一律會為每個建立的臨時表配置1MB 的位址空間區塊。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>相同的會話無法同時用於一個以上的執行緒。</p><p>只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 
| <p>JET_errTooManyColumns</p> | <p>嘗試將過多的資料行新增至資料表。 資料表不能超過 JET_ccolFixedMost 固定資料行，不能超過 JET_ccolVarMost 的可變長度資料行，且不能超過 JET_ccolTaggedMost 標記的資料行。</p> | 
| <p>JET_errTooManyOpenIndexes</p> | <p>作業失敗，因為引擎無法配置快取資料表索引所需的資源。 您可以使用 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 搭配 <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>，設定可以快取架構的索引數目。</p> | 
| <p>JET_errTooManyOpenTables</p> | <p>作業失敗，因為引擎無法配置快取資料表架構所需的資源。 您可以使用 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 搭配 <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>，設定可以快取架構的資料表數目。</p> | 
| <p>JET_errTooManySorts</p> | <p>作業失敗，因為引擎無法配置建立臨時表所需的資源。 臨時表資源是使用 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 搭配 <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>進行設定。</p> | 



成功時，會傳回在新建立的臨時表上開啟的資料指標。 暫存資料庫的狀態將準備好包含新的臨時表。 資料庫引擎所使用之任何一般資料庫的狀態將保持不變。

失敗時，將不會建立臨時表，也不會傳回資料指標。 暫存資料庫的狀態可能會變更。 資料庫引擎所使用之任何一般資料庫的狀態將保持不變。

#### <a name="remarks"></a>備註

臨時表不支援資料庫引擎通常支援之資料行定義選項的完整補充。 事實上，只支援 JET_bitColumnFixed 和 JET_bitColumnTagged。 這表示不可能在臨時表中建立自動遞增、版本或多重值資料行。 最後，不支援保管更新資料行，因為它們在臨時表中並不實用，因為它們一次只能由一個會話使用。 如果要求這些選項中的任何一項，則會忽略這些選項。

臨時表不支援預設值。 如果提供的資料行定義包含預設值規格，則會忽略該規格。

由於許多不同的 ESE 函數，臨時表會傳回給呼叫端。 例如，在 *InfoLevel* 參數中設定 JET_IdxInfo 選項的 [JetGetIndexInfo](./jetgetindexinfo-function.md) ，將會傳回臨時表，其中包含給定索引中所有索引鍵資料行的清單。 臨時表會遵循與一般臨時表相同的生命週期規則，如下所述。

資料庫引擎也會在內部使用臨時表來進行許多工。 這些工作中最重要的就是在現有的資料表上建立索引。 臨時表將用來排序用來建立索引的索引鍵。

所有臨時表都會儲存在暫存資料庫中。 暫存資料庫是一個特殊的資料庫檔案，會在 ESE 實例的存留期內進行維護，當該實例關閉或重新開機時，就會將其刪除。 您可以使用 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 搭配 [JET_paramTempPath](./temporary-database-parameters.md)來設定暫存資料庫的位置。 如果您的應用程式大量使用臨時表或經常建立索引，則相對於交易記錄檔和資料庫檔案的暫存資料庫放置在磁片上可能很重要。

臨時表的生命週期會系結至參考它的資料指標。 如果參考臨時表的所有資料指標都是以隱含或明確的方式關閉，則會刪除臨時表。 如果在交易內建立臨時表，而且之後復原該交易，則會刪除該臨時表，因為此時參考該資料表的任何資料指標都會以隱含方式關閉。 新的資料指標可能只會透過使用 [JetDupCursor](./jetdupcursor-function.md)來參考臨時表。 在此情況下，新的資料指標將定位於臨時表的第一個索引項目目。 [JetDupCursor](./jetdupcursor-function.md) 僅適用于臨時表的特定使用階段。 如需詳細資訊，請參閱關於臨時表資料指標功能的備註。 一次只能從一個以上的會話參考臨時表。

[JetDupCursor](./jetdupcursor-function.md)中有一個會影響臨時表的重要問題。 如果嘗試複製處於順向模式的臨時表，則會無法正確建立產生的資料指標，而且會發生故障。 在具體化的臨時表上重復資料指標仍然是安全的。

臨時表管理員可能會選擇以三種方式來執行臨時表。 第一個方法是維護記憶體中的資料表。 這是最快的策略，但只能用於小型、簡單的臨時表。 第二種方法是建立以磁片為基礎的排序，該排序可使用順向反覆運算器驅動。 這項策略只能在特定情況下使用，而且是從非常大的資料集排序和移除重複專案的最快速方式。 第三種方法是在暫存資料庫中建立 B + 樹狀結構，以保存臨時表。 這個策略是最慢的，但最多用途，而且稱為具體化臨時表。 這些策略可組合使用，以最終達成臨時表所要求的功能。

當臨時表未具體化時，主要是用於兩個主要階段。 第一個階段是插入階段，其中資料表會填入其初始資料集。 在這個階段中，只允許插入資料。 當嘗試使用 [JetMove](./jetmove-function.md) 或 [JetSeek](./jetseek-function.md)移動資料指標時，就會結束這個階段。 第二個階段是資料解壓縮階段。 在這個階段，儲存在臨時表中的資料，可能會根據建立臨時表時所要求的功能進行解壓縮。

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

當臨時表未具體化且在插入階段時，資料指標有下列功能，但可能會進一步限制要求的選項：

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


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 
| <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | 
| <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetDupCursor](./jetdupcursor-function.md)  
[JetMove](./jetmove-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[暫存資料庫參數](./temporary-database-parameters.md)
