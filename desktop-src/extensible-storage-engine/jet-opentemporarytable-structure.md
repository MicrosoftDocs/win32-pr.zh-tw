---
description: 深入瞭解： JET_OPENTEMPORARYTABLE 結構
title: JET_OPENTEMPORARYTABLE 結構
TOCTitle: JET_OPENTEMPORARYTABLE Structure
ms:assetid: 23f4fb0f-ca60-498b-9b8e-14de6188eb87
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269206(v=EXCHG.10)
ms:contentKeyID: 32765509
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 625de51bf265be02fa48beb2872797cd5bd6ba26
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986911"
---
# <a name="jet_opentemporarytable-structure"></a>JET_OPENTEMPORARYTABLE 結構


_**適用于：** Windows |Windows伺服器_

## <a name="jet_opentemporarytable-structure"></a>JET_OPENTEMPORARYTABLE 結構

**JET_OPENTEMPORARYTABLE** 結構包含可輕鬆擴充的 **JET_OPENTEMPORARYTABLE** 函式參數集合。 此結構是與 [JET_TABLECREATE](./jet-tablecreate-structure.md) 結構相等的臨時表。

**Windows Vista：** Windows Vista 引進了 **JET_OPENTEMPORARYTABLE** 結構。

```cpp
    typedef struct tagJET_OPENTEMPORARYTABLE {
      unsigned long cbStruct;
      const JET_COLUMNDEF* prgcolumndef;
      unsigned long ccolumn;
      JET_UNICODEINDEX* pidxunicode;
      JET_GRBIT grbit;
      JET_COLUMNID* prgcolumnid;
      unsigned long cbKeyMost;
      unsigned long cbVarSegMac;
      JET_TABLEID tableid;
    } JET_OPENTEMPORARYTABLE;
```

### <a name="members"></a>成員

**cbStruct**

此結構的大小，以位元組為單位， (未來的擴充) 。 它必須設定為 sizeof ( JET_TABLECREATE ) （以位元組為單位）。

**prgcolumndef**

在臨時表中建立之資料行的資料行定義。

用於臨時表的資料行定義選項有 **重要** 的限制。 如需詳細資訊，請參閱＜備註＞一節。

除了一般資料行定義選項之外，也可以指定零或多個下列選項，這些選項只與臨時表的內容有關。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitColumnTTDescending</p> | <p>臨時表之索引鍵資料行的排序次序應該是遞減的，而不是遞增的。 如果指定這個選項但未指定 JET_bitColumnTTKey 則會忽略此選項。</p> | 
| <p>JET_bitColumnTTKey</p> | <p>資料行將是臨時表的索引鍵資料行。</p><p>在輸入陣列中指定此選項的資料行定義順序，將會決定臨時表的每個索引鍵資料行的優先順序。 陣列中具有這個選項組的第一個資料行定義將是最重要的索引鍵資料行，依此類推。 如果要求的索引鍵資料行數目超過 database engine 所能支援的數量，則會忽略不受支援索引鍵資料行的這個選項。</p> | 



**ccolumn**

請參閱 *prgcolumndef*。

**pidxunicode**

用來比較臨時表中任何 Unicode 索引鍵資料行資料的地區設定識別碼和正規化旗標。

當這個參數不存在，而且沒有 *lcid* 參數時，就會使用預設的 lcid 來比較臨時表中的任何 Unicode 索引鍵資料行。 預設的 LCID 是美國英文地區設定。

如果這個參數不存在，則會使用預設正規化旗標來比較臨時表中的任何 Unicode 索引鍵資料行資料。 預設正規化旗標為： NORM_IGNORECASE、NORM_IGNOREKANATYPE 和 NORM_IGNOREWIDTH。

**grbit**

指定零或多個下列選項的位群組。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitTTIndexed</p> | <p>此選項會要求臨時表具有足夠的彈性，可允許使用 <a href="gg294103(v=exchg.10).md">JetSeek</a> 依據索引鍵來查閱記錄。</p><p>如果這項功能不是必要的，則最好不要要求它。 如果未要求這項功能，則臨時表管理員可能會選擇管理臨時表的策略，而這會導致效能改進。</p> | 
| <p>JET_bitTTUnique</p> | <p>會從臨時表的最後一組記錄中，移除具有重複索引鍵的記錄。</p><p>在 Windows Server 2003 之前，資料庫引擎一律會假設這個選項有作用，因為所有叢集索引也必須是主鍵，因此必須是唯一的。 從 Windows Server 2003 開始，當也指定了 JET_bitTTForwardOnly 選項時，現在可以建立不會移除重複專案的臨時表。</p><p>一般情況下，不可能知道哪些複製成功，以及哪些重複專案會被捨棄。 不過，當要求 JET_bitTTErrorOnDuplicateInsertion 選項時，具有要插入至臨時表之指定索引鍵的第一個記錄一律會成功。</p> | 
| <p>JET_bitTTUpdatable</p> | <p>要求臨時表有足夠的彈性，可讓之前插入的記錄之後變更。 如果這項功能不是必要的，則最好不要要求它。</p><p>如果未要求這項功能，則臨時表管理員可能會選擇管理臨時表的策略，而這會導致效能改進。</p> | 
| <p>JET_bitTTScrollable</p> | <p>要求臨時表具有足夠的彈性，可讓您以任意順序和使用 <a href="gg294117(v=exchg.10).md">JetMove</a>的方向來掃描記錄。</p><p>如果不需要這項功能，最好不要要求。 如果未要求這項功能，則臨時表管理員可能會選擇管理臨時表的策略，而這會導致效能改進。</p> | 
| <p>JET_bitTTSortNullsHigh</p> | <p>要求 <strong>Null</strong> 索引鍵資料行值的排序比非 Null 索引鍵資料行值更接近索引的結尾。</p> | 
| <p>JET_bitTTForceMaterialization</p> | <p>強制臨時表管理員放棄搜尋，以使用管理將會導致效能提高的臨時表的最佳策略。</p> | 
| <p>JET_bitTTErrorOnDuplicateInsertion</p> | <p>任何嘗試插入具有與先前所插入記錄相同索引鍵的記錄，都會立即失敗，並 JET_errKeyDuplicate。 如果未要求這個選項，則會立即偵測到重複的情況，並會失敗，或根據資料庫引擎根據所要求的功能來執行臨時表所選擇的策略，以無訊息方式移除。</p><p>如果這項功能不是必要的，則最好不要要求它。 如果未要求這項功能，則臨時表管理員可能會選擇管理臨時表的策略，而這會導致效能改進。</p> | 
| <p>JET_bitTTForwardOnly</p> | <p>只有當臨時表管理員可以使用針對中繼查詢結果優化的執行時，才會建立臨時表。 如果臨時表的任何特性會防止使用這項優化，則作業會失敗並 JET_errCannotMaterializeForwardOnlySort。</p><p>此選項的副作用是允許臨時表包含具有重複索引鍵的記錄。 如需詳細資訊，請參閱 JET_bitTTUnique。</p><p><strong>Windows Server 2003：</strong>此選項僅適用于 Windows Server 2003 和更新版本。</p> | 



**prgcolumnid**

輸出緩衝區，接收在建立臨時表期間所產生的資料行識別碼陣列。

此陣列中的資料行識別碼，將會完全對應至資料行定義的輸入陣列。 因此，這個緩衝區的大小必須對應到輸入陣列的大小。

**cbKeyMost**

代表指定資料列之索引鍵的大小上限。

您可以設定最大索引鍵大小來控制如何截斷金鑰。 金鑰截斷很重要，因為它可能會影響資料列視為相異的時間。

如果此參數設定為0或 JET_cbKeyMostMin (255) 則最大的索引鍵大小及其語義將維持與 Windows Server 2003 和舊版所支援的最大金鑰大小相同。 此參數也可以設定為較大的值，做為實例 (JET_paramDatabasePageSize) 之資料庫頁面大小的功能。 如需詳細資訊，請參閱 JET_paramKeyMost。

**cbVarSegMac**

將從任何可變長度資料行使用的最大資料量，以針對指定的資料列來建立索引鍵。

此參數可用來控制任何指定的索引鍵資料行所耗用的金鑰空間量。 這項限制是以位元組為單位。 如果此參數為零或與 *cbKeyMost* 參數相同，則沒有作用中的限制。

**tableid**

由於成功呼叫 [JetOpenTemporaryTable](./jetopentemporarytable-function.md)而建立之臨時表的資料表控制碼。

### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows Server 2008。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetOpenTemporaryTable](./jetopentemporarytable-function.md)  
[可擴充的儲存體引擎系統參數](./extensible-storage-engine-system-parameters.md)
