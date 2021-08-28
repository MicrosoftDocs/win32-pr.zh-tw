---
description: 深入瞭解： JetOpenTempTable3 函數
title: JetOpenTempTable3 函式
TOCTitle: JetOpenTempTable3 Function
ms:assetid: 58d6e264-705e-402b-928f-96eefe5e9771
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269255(v=EXCHG.10)
ms:contentKeyID: 32765557
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenTempTable3
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a1005f9804e0ccf9c4aa5080b3985906471b1386
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988911"
---
# <a name="jetopentemptable3-function"></a>JetOpenTempTable3 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetopentemptable3-function"></a>JetOpenTempTable3 函式

**JetOpenTempTable3** 函式會建立一個臨時表，其中包含可用於儲存和取出記錄的單一索引，就像使用 [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)建立的一般資料表一樣。 不過，臨時表的速度會比一般資料表快許多，因為它們是暫時性的本質。 它們也可用來在以純粹順序存取的方式存取記錄集時，非常快速地排序和執行重複的移除。

```cpp
    JET_ERR JET_API JetOpenTempTable3(
      __in          JET_SESID sesid,
      __in          const JET_COLUMNDEF* prgcolumndef,
      __in          unsigned long ccolumn,
      __in_opt      JET_UNICODEINDEX* pidxunicode,
      __in          JET_GRBIT grbit,
      __out         JET_TABLEID* ptableid,
      __out         JET_COLUMNID* prgcolumnid
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*prgcolumndef*

識別要在臨時表中建立之資料行的資料行定義。

適用于臨時表的資料行定義選項會有重要的限制。 如需詳細資訊，請參閱＜備註＞一節。

除了一般的資料行定義選項之外，也可以指定零或多個下列選項，這些選項只能與臨時表的內容相關。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitColumnTTDescending</p> | <p>此選項指出臨時表之索引鍵資料行的排序次序應該是遞減的，而不是遞增的。 如果指定這個選項但未指定 JET_bitColumnTTKey 則會忽略此選項。</p> | 
| <p>JET_bitColumnTTKey</p> | <p>此選項表示資料行將會是臨時表的索引鍵資料行。</p><p>在輸入陣列中指定此選項的資料行定義順序，將會決定臨時表的每個索引鍵資料行的優先順序。 使用這個選項組的陣列中的第一個資料行定義將是最重要的索引鍵資料行，依此類推。 如果要求的索引鍵資料行數目超過 database engine 所能支援的數量，則會忽略不受支援索引鍵資料行的這個選項。</p> | 



*ccolumn*

請參閱 *prgcolumndef*。

*pidxunicode*

地區設定識別碼和正規化旗標，將用來比較臨時表中的任何 Unicode 索引鍵資料行資料。

如果這個參數不存在，則會使用預設的 LCID 來比較臨時表中的任何 Unicode 索引鍵資料行。 預設的 LCID 是美國英文地區設定。

如果這個參數不存在，則會使用預設正規化旗標來比較臨時表中的任何 Unicode 索引鍵資料行資料。 預設正規化旗標為： NORM_IGNORECASE、NORM_IGNOREKANATYPE 和 NORM_IGNOREWIDTH。

*grbit*

位群組，其中包含要用於此呼叫的選項，包括下列零或多個。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitTTErrorOnDuplicateInsertion</p> | <p>此選項會要求任何嘗試插入具有與先前所插入記錄相同索引鍵的記錄，但 JET_errKeyDuplicate 會立即失敗。 如果未要求這個選項，則可能會立即偵測到重複的情況，也可能會在稍後根據資料庫引擎根據所要求的功能來執行臨時表所選擇的策略，而失敗或以無訊息方式移除。</p><p>如果這項功能不是必要的，則最好不要要求它。 如果未要求這項功能，則臨時表管理員可能會選擇管理臨時表的策略，而這會導致效能改進。</p> | 
| <p>JET_bitTTForceMaterialization</p> | <p>此選項會強制臨時表管理員放棄任何嘗試選擇聰明的策略來管理臨時表，以產生增強的效能。</p> | 
| <p>JET_bitTTForwardOnly</p> | <p>如果臨時表管理員可以使用針對中繼查詢結果優化的執行，此選項會要求只建立臨時表。 如果臨時表的任何特性會防止使用這項優化，則作業會失敗並 JET_errCannotMaterializeForwardOnlySort。</p><p>此選項的副作用是允許臨時表包含具有重複索引鍵的記錄。 如需詳細資訊，請參閱 JET_bitTTUnique。</p><p>此選項僅適用于 Windows Server 2003 和更新版本。</p> | 
| <p>JET_bitTTIndexed</p> | <p>此選項會要求臨時表具有足夠的彈性，可允許使用 <a href="gg294103(v=exchg.10).md">JetSeek</a> 依據索引鍵來查閱記錄。</p><p>如果這項功能不是必要的，則最好不要要求它。 如果未要求這項功能，則臨時表管理員可能會選擇管理臨時表的策略，而這會導致效能改進。</p> | 
| <p>JET_bitTTUnique</p> | <p>此選項會要求從臨時表的最後一組記錄中，移除具有重複索引鍵的記錄。</p><p>在 Windows Server 2003 之前，資料庫引擎一律會假設這個選項有作用，因為所有叢集索引也必須是主鍵，因此必須是唯一的。 從 Windows Server 2003 開始，當也指定了 JET_bitTTForwardOnly 選項時，現在可以建立不會移除重複專案的臨時表。</p><p>您無法知道哪些重複專案會獲勝，哪些重複專案會在一般情況下捨棄。 不過，當要求 JET_bitTTErrorOnDuplicateInsertion 選項時，會永遠贏得具有指定索引鍵的第一個記錄插入臨時表中。</p> | 
| <p>JET_bitTTUpdatable</p> | <p>此選項會要求臨時表具有足夠的彈性，可讓之前插入的記錄之後變更。 如果這項功能不是必要的，則最好不要要求它。</p><p>如果未要求這項功能，則臨時表管理員可能會選擇管理臨時表的策略，而這會導致效能改進。</p> | 
| <p>JET_bitTTScrollable</p> | <p>此選項會要求臨時表具有足夠的彈性，可讓您以任意順序和使用 <a href="gg294117(v=exchg.10).md">JetMove</a>的方向來掃描記錄。</p><p>如果這項功能不是必要的，則最好不要要求它。 如果未要求這項功能，則臨時表管理員可能會選擇管理臨時表的策略，而這會導致效能改進。</p> | 
| <p>JET_bitTTSortNullsHigh</p> | <p>此選項會要求 Null 索引鍵資料行值的排序比非 Null 索引鍵資料行值更接近索引的結尾。</p> | 
| <p>JET_bitTTIntrinsicLVsOnly</p> | <p>要求只允許內建的 long 值。</p><p><strong>Windows 7</strong>： <strong>JET_bitTTIntrinsicLVsOnly</strong>是 Windows 7 中引進的。</p> | 



*ptableid*

將接收新建立的臨時表上開啟之新資料指標的輸出緩衝區。

*prgcolumnid*

輸出緩衝區，將會接收建立臨時表時所產生之資料行識別碼的陣列。

此陣列中的資料行識別碼，將會完全對應至資料行定義的輸入陣列。 因此，這個緩衝區的大小必須對應到輸入陣列的大小。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errCannotMaterializeForwardOnlySort</p> | <p><strong>JetOpenTempTable3</strong> 失敗，因為指定了 JET_bitTTForwardOnly，而且無法使用順向優化來建立指定的臨時表。 只有 Windows Server 2003 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>無法建立索引，因為指定了不正確索引定義。 <strong>JetOpenTempTable3</strong> 會在下列情況傳回此錯誤：</p><ul><li><p>指定了中性語言的地區設定。</p></li><li><p>指定了不正確正規化旗標集合。</p></li></ul><p>只有 Windows 2000 才會傳回此錯誤。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errInvalidCodePage</p> | <p><a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>結構的<strong>cp</strong>成員未設定為有效的字碼頁。 Text 資料行的唯一有效值是英文 (1252) 和 Unicode (1200) 。 0值表示預設值將使用 (英文、1252) 。</p> | 
| <p>JET_errInvalidColumnType</p> | <p><a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a>結構的<strong>coltyp</strong>成員未設定為有效的資料行類型。</p> | 
| <p>JET_errInvalidLanguageId</p> | <p>無法建立索引，因為嘗試使用不正確地區設定識別碼。 地區設定識別碼可能完全無效，或可能未安裝相關聯的語言套件。</p> | 
| <p>JET_errInvalidLCMapStringFlags</p> | <p>無法建立索引，因為嘗試使用一組不正確正規化旗標。 只有 Windows XP 和更新版本才會傳回此錯誤。 在 Windows 2000 上，不正確正規化旗標會改為產生 JET_errIndexInvalidDef。</p> | 
| <p>JET_errInvalidSesid</p> | <p>會話控制碼無效或參考已關閉的會話。 在所有情況下，都不會傳回此錯誤。 控制碼只會根據最大努力進行驗證。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errOutOfCursors</p> | <p>作業失敗，因為引擎無法配置開啟新資料指標所需的資源。 資料指標資源是使用 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 搭配 <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>進行設定。</p> | 
| <p>JET_errOutOfMemory</p> | <p>作業失敗，因為無法配置足夠的記憶體來完成。</p><p>如果主機進程的位址空間變得太分散， <strong>JetOpenTempTable3</strong>可能會傳回 JET_errOutOfMemory。 無論要儲存的資料量為何，臨時表管理員一律會為每個建立的臨時表配置1MB 的位址空間區塊。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>相同的會話無法同時用於一個以上的執行緒。</p><p>只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 
| <p>JET_errTooManyColumns</p> | <p>嘗試將過多的資料行新增至資料表。 資料表不能超過 JET_ccolFixedMost 固定資料行，不能超過 JET_ccolVarMost 的可變長度資料行，且不能超過 JET_ccolTaggedMost 標記的資料行。</p> | 
| <p>JET_errTooManyOpenIndexes</p> | <p>作業失敗，因為引擎無法配置快取資料表索引所需的資源。 您可以使用 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 搭配 <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>，設定可以快取架構的索引數目。</p> | 
| <p>JET_errTooManyOpenTables</p> | <p>作業失敗，因為引擎無法配置快取資料表架構所需的資源。 您可以使用 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 搭配 <a href="gg269201(v=exchg.10).md">JET_paramMaxOpenTables</a>，設定可以快取架構的資料表數目。</p> | 
| <p>JET_errTooManySorts</p> | <p>作業失敗，因為引擎無法配置建立臨時表所需的資源。 臨時表資源是使用 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 搭配 <a href="gg294140(v=exchg.10).md">JET_paramMaxTemporaryTables</a>進行設定。</p> | 



成功時，會傳回在新建立的臨時表上開啟的資料指標。 暫存資料庫的狀態將準備好包含新的臨時表。 資料庫引擎所使用之任何一般資料庫的狀態將保持不變。

失敗時，將不會建立臨時表，也不會傳回資料指標。 暫存資料庫的狀態可能會變更。 資料庫引擎所使用之任何一般資料庫的狀態將保持不變。

#### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 
| <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | 
| <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[可擴充的儲存體引擎錯誤](./extensible-storage-engine-errors.md)  
[錯誤處理參數](./error-handling-parameters.md)  
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
[JetOpenTempTable](./jetopentemptable-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[系統參數](./extensible-storage-engine-system-parameters.md)
