---
description: 深入瞭解： JetMakeKey 函數
title: JetMakeKey 函式
TOCTitle: JetMakeKey Function
ms:assetid: 8c1cff2f-2f24-4990-a9d8-fb4f822e50b1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269329(v=EXCHG.10)
ms:contentKeyID: 32765619
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetMakeKey
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a642a103d67b023fdf42aa532cc328964c7734a4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482844"
---
# <a name="jetmakekey-function"></a>JetMakeKey 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetmakekey-function"></a>JetMakeKey 函式

**JetMakeKey** 函式會先建立搜尋索引鍵，然後在索引鍵資料行值上使用一些簡單的搜尋準則來尋找索引中的一組專案。 搜尋索引鍵也是資料指標的其中一個內建屬性，並由 [JetSeek](./jetseek-function.md) 和 [JetSetIndexRange](./jetsetindexrange-function.md) 作業用來尋找符合該資料指標目前索引之這些搜尋準則的索引項目。 完整的搜尋索引鍵會在一系列的 **JetMakeKey** 呼叫中建立，其中每個呼叫都是用來載入資料指標目前索引之下一個索引鍵資料行的資料行值。 您也可以載入先前使用 [JetRetrieveKey](./jetretrievekey-function.md)從資料指標抓取的搜尋索引鍵。

```cpp
    JET_ERR JET_API JetMakeKey(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      const void* pvData,
      __in          unsigned long cbData,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*tableid*

要用於此呼叫的資料指標。

*pvData*

輸入緩衝區，其中包含要為其建立搜尋索引鍵之資料指標目前索引鍵資料行的資料行資料。

輸入緩衝區中資料行資料的資料類型必須完全符合目前索引鍵資料行之資料行定義的資料類型和其他屬性。 在資料行資料上不會執行任何類型強制型轉。

如果在 *grbit* 參數中指定 JET_bitNormalizedKey，輸入緩衝區必須包含先前已建立的搜尋索引鍵。 這類金鑰是使用 [JetRetrieveKey](./jetretrievekey-function.md)呼叫所取得。

*cbData*

輸入緩衝區中提供之資料行資料的大小（以位元組為單位）。

如果在 *grbit* 參數中指定 JET_bitNormalizedKey，這就是輸入緩衝區中提供的搜尋索引鍵大小。

如果資料行資料的大小為零，則會忽略輸入緩衝區的內容。 如果在 *grbit* 參數中指定了 JET_bitKeyDataZeroLength，而且目前的資料指標索引鍵資料行是可變長度資料行，則輸入資料行的資料會假設為零長度的值。 否則，輸入資料行資料會假設為 Null 值。

*grbit*

指定零或多個下列選項的位群組。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitFullColumnEndLimit</p> | <p>搜尋索引鍵的建立方式，是在目前的索引鍵資料行之後的任何索引鍵資料行都會被視為萬用字元。 這表示，您可以使用已建立的搜尋索引鍵來比對具有下列專案的索引項目：</p><ul><li><p>為此索引鍵資料行和所有先前的索引鍵資料行提供的確切資料行值。</p></li><li><p>後續索引鍵資料行所需的任何資料行值。</p></li></ul><p>建立萬用字元搜尋索引鍵以用來尋找最接近索引結尾的索引項目時，應使用這個選項。 索引的結尾是移至該索引中的最後一筆記錄時，所找到的索引項目。 索引的結尾與索引的高端不同，它可能會根據索引中索引鍵資料行的排序次序而變更。</p><p>此選項僅適用于 Windows XP 及更新版本。</p> | 
| <p>JETbitFullColumnStartLimit</p> | <p>應將搜尋索引鍵的結構化，以便在目前的索引鍵資料行之後的任何索引鍵資料行都應視為萬用字元。 這表示，您可以使用已建立的搜尋索引鍵來比對具有下列專案的索引項目：</p><ul><li><p>為此索引鍵資料行和所有先前的索引鍵資料行提供的確切資料行值。</p></li><li><p>後續索引鍵資料行所需的任何資料行值。</p></li></ul><p>建立萬用字元搜尋索引鍵以用來尋找最接近索引開頭的索引項目時，應使用這個選項。 索引的開頭是移至該索引中的第一筆記錄時，所找到的索引項目。 索引的開頭與索引的下限不同，它可能會根據索引中索引鍵資料行的排序次序而變更。</p><p>此選項僅適用于 Windows XP 及更新版本。</p> | 
| <p>JET_bitKeyDataZeroLength</p> | <p>如果輸入緩衝區的大小為零，且目前的索引鍵資料行是可變長度資料行，則此選項表示輸入緩衝區包含零長度的值。 否則，輸入緩衝區大小為零會指出 Null 值。</p> | 
| <p>JET_bitNewKey</p> | <p>應建立新的搜尋索引鍵。 任何先前現有的搜尋金鑰都會被捨棄。</p> | 
| <p>JET_bitNormalizedKey</p> | <p>指定此選項時，會忽略所有其他選項，任何先前現有的搜尋金鑰都會被捨棄，而輸入緩衝區的內容會載入為新的搜尋索引鍵。</p> | 
| <p>JET_bitPartialColumnEndLimit</p> | <p>應建立搜尋索引鍵，讓目前的索引鍵資料行被視為首碼萬用字元，且在目前索引鍵資料行之後的任何索引鍵資料行都應視為萬用字元。 這表示，您可以使用已建立的搜尋索引鍵來比對具有下列專案的索引項目：</p><ul><li><p>為此索引鍵資料行和所有先前的索引鍵資料行提供的確切資料行值。</p></li><li><p>後續索引鍵資料行所需的任何資料行值。</p></li></ul><p>建立萬用字元搜尋索引鍵以用來尋找最接近索引結尾的索引項目時，應使用這個選項。 索引的結尾是移至該索引中的最後一筆記錄時，所找到的索引項目。 索引的結尾與索引的高端不同，它可能會根據索引中索引鍵資料行的排序次序而變更。</p><p>當目前的索引鍵資料行不是文字資料行或變數二進位資料行時，就無法使用這個選項。 如果嘗試這麼做，則作業將會失敗，並出現 JET_errInvalidgrbit。</p><p>此選項僅適用于 Windows XP 及更新版本。</p> | 
| <p>JET_bitPartialColumnStartLimit</p> | <p>此選項表示應建立搜尋索引鍵，讓目前的索引鍵資料行被視為首碼萬用字元，且在目前索引鍵資料行之後的任何索引鍵資料行都應視為萬用字元。 這表示，您可以使用已建立的搜尋索引鍵來比對具有下列專案的索引項目：</p><ul><li><p>為此索引鍵資料行和所有先前的索引鍵資料行提供的確切資料行值。</p></li><li><p>後續索引鍵資料行所需的任何資料行值。</p></li></ul><p>建立萬用字元搜尋索引鍵以用來尋找最接近索引開頭的索引項目時，應使用這個選項。 索引的開頭是移至該索引中的第一筆記錄時，所找到的索引項目。 索引的開頭與索引的下限不同，它可能會根據索引中索引鍵資料行的排序次序而變更。</p><p>當目前的索引鍵資料行不是文字資料行或變數二進位資料行時，就無法使用這個選項。 如果嘗試這麼做，則作業將會失敗，並出現 JET_errInvalidgrbit。</p><p>此選項僅適用于 Windows XP 及更新版本。</p> | 
| <p>JET_bitStrLimit</p> | <p>此選項表示應建立搜尋索引鍵，以便將目前索引鍵資料行後面的任何索引鍵資料行視為萬用字元。 這表示，您可以使用已建立的搜尋索引鍵來比對具有下列專案的索引項目：</p><ul><li><p>為此索引鍵資料行和所有先前的索引鍵資料行提供的確切資料行值。</p></li><li><p>後續索引鍵資料行所需的任何資料行值。</p></li></ul><p>建立萬用字元搜尋索引鍵以用來尋找最接近索引結尾的索引項目時，應使用這個選項。 索引的結尾是移至該索引中的最後一筆記錄時，所找到的索引項目。 索引的結尾與索引的高端不同，它可能會根據索引中索引鍵資料行的排序次序而變更。</p><p>當這個選項與 JET_bitSubStrLimit 一起指定，且目前的索引鍵資料行是文字資料行時，將會忽略此選項。 此行為是為了允許在建立搜尋索引鍵時，推斷目前索引鍵資料行的類型。</p><p>如果您想要針對索引的開頭建立類似的搜尋索引鍵，則應該對不是萬用字元的最後一個索引鍵資料行進行類似的 <strong>JetMakeKey</strong> 呼叫，但不指定萬用字元選項。 搜尋金鑰接著會處於適當的狀態，以用於這類搜尋。 這類似于使用 JET_bitFullColumnStartLimit，不同之處在于搜尋索引鍵未完全完成，因為它是在使用萬用字元選項之後。</p><p>針對 Windows XP 和更新版本，此選項已被取代，以解決這種不容易的語義。 應該盡可能使用 JET_bitFullColumnStartLimit 和 JET_bitFullColumnEndLimit。</p> | 
| <p>JET_bitSubStrLimit</p> | <p>此選項表示應建立搜尋索引鍵，讓目前的索引鍵資料行被視為首碼萬用字元，且在目前索引鍵資料行之後的任何索引鍵資料行都應視為萬用字元。 這表示，您可以使用已建立的搜尋索引鍵來比對具有下列專案的索引項目：</p><ul><li><p>針對所有先前的索引鍵資料行提供的確切資料行值。</p></li><li><p>指定的資料行資料，做為目前索引鍵資料行之資料行值的前置詞。</p></li><li><p>後續索引鍵資料行的任何資料行值。</p></li></ul><p>建立萬用字元搜尋索引鍵以用來尋找最接近索引結尾的索引項目時，應使用這個選項。 索引的結尾是移至該索引中的最後一筆記錄時，所找到的索引項目。 索引的結尾與索引的高端不同，它可能會根據索引中索引鍵資料行的排序次序而變更。</p><p>當這個選項與 JET_bitStrLimit 一起指定，且目前的索引鍵資料行是文字資料行時，就會優先使用此選項。 當目前的索引鍵資料行不是文字資料行時，就會忽略這個選項。 此行為是為了允許在建立搜尋索引鍵時，推斷目前索引鍵資料行的類型。</p><p>如果您想要針對索引的開頭建立類似的搜尋索引鍵，則應該針對要做為前置詞萬用字元的索引鍵資料行進行類似的 <strong>JetMakeKey</strong> 呼叫，但未指定萬用字元選項。 搜尋金鑰接著會處於適當的狀態，以用於這類搜尋。 這類似于使用 JET_bitPartialColumnStartLimit，不同之處在于搜尋索引鍵未完全完成，因為它是在使用萬用字元選項之後。</p><p>針對 Windows XP 和更新版本，此選項已被取代，以解決這種不容易的語義。 如果可能的話，應該改用 JET_bitPartialColumnStartLimit 和 JET_bitPartialColumnEndLimit。</p> | 



### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p> | 
| <p>JET_errIndexTuplesKeyTooSmall</p> | <p>提供的資料行資料太小，無法為目前的索引建立有效的索引鍵，因為該索引是元組索引，且最小的元組大小大於所提供的資料行資料。 如需元組索引的詳細資訊，請參閱 <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> 。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>提供的資料行資料不符合資料行定義所需的大小。 如果資料行的資料類型本質上是特定大小，就會發生這種情況。 如果資料行的資料類型本質上不是特定大小，但是資料行的定義宣告為固定長度，也會發生這種情況。 其中一個例外狀況是，如果為固定長度的文字資料行提供太少資料，將不會發生此錯誤，因為任何遺漏的資料都會自動填補空格。 第二個例外狀況是，如果為固定長度的二進位資料行提供太少資料，將不會發生此錯誤，因為遺漏的資料將會自動填補零。</p> | 
| <p>JET_errInvalidgrbit</p> | <p>其中一個要求的選項無效、以不合法的方式使用，或未執行。 在下列情況下， <strong>JetMakeKey</strong> 可能會發生：</p><ul><li><p>指定 JET_bitPartialColumnStartLimit 或 JET_bitPartialColumnEndLimit，而且對應的索引鍵資料行不是文字資料行，而且不是可變長度的二進位資料行。 這種情況只會發生在 Windows XP 和更新版本上。</p></li><li><p>嘗試同時使用下列一個以上的選項： JET_bitPartialColumnStartLimit、JET_bitPartialColumnEndLimit、JET_bitFullColumnStartLimit 和 JET_bitFullColumnEndLimit。 這種情況只會發生在 Windows XP 和更新版本上。</p></li><li><p>使用下列其中一個選項時，會嘗試使用 JET_bitStrLimit 或 JET_bitSubStrLimit： JET_bitPartialColumnStartLimit、JET_bitPartialColumnEndLimit、JET_bitFullColumnStartLimit 和 JET_bitFullColumnEndLimit。 這種情況只會發生在 Windows XP 和更新版本上。</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。</p><p>當指定 JET_bitNormalizedKey，且輸入緩衝區中提供的值太大而無法成為有效的搜尋索引鍵時， <strong>JetMakeKey</strong> 就會發生這種情況。</p> | 
| <p>JET_errKeyIsMade</p> | <p>提供給 <strong>JetMakeKey</strong> 的資料行資料遭到拒絕，因為目前索引中的所有索引鍵資料行都已提供資料行資料。 這可能會以三種方式發生。 第一種方式是針對目前索引中的每個索引鍵資料行提供資料行資料。 第二種方式是，是否已為至少一個索引鍵資料行提供資料行資料，且已為最後一次呼叫選擇萬用字元選項。 第三種方式是使用 JET_bitNormalizedKey （涵蓋所有索引鍵資料行）來提供先前所建立的搜尋索引鍵。</p> | 
| <p>JET_errKeyNotMade</p> | <p>沒有目前的資料指標搜尋索引鍵。 如果未指定 JET_bitNewKey，且尚未使用<strong>JetMakeKey</strong>的先前呼叫來為此資料指標建立搜尋索引鍵<strong>，則會</strong>發生這種情況。 搜尋索引鍵將會由先前呼叫 <a href="gg294117(v=exchg.10).md">JetMove</a>以外的資料指標上的任何導覽 API 來刪除。</p> | 
| <p>JET_errNoCurrentIndex</p> | <p>沒有目前的資料指標索引。 如果資料指標位於資料表的叢集索引、未定義主要索引，且未指定 JET_bitNormalizedKey，就會發生這種<strong>情況。</strong> 如果資料指標位於沒有任何索引鍵資料行的索引上，除非提供了先前建立的搜尋索引鍵，否則無法建立搜尋索引鍵。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>相同的會話無法同時用於一個以上的執行緒。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 



成功時，如果未指定 JET_bitNormalizedKey 和 JET_bitNewKey，則會在目前索引中，針對一個以上的索引鍵資料行，以搜尋準則建立搜尋索引鍵。 如果未指定 JET_bitNormalizedKey，且指定了 JET_bitNewKey，則會捨棄任何先前現有的搜尋索引鍵，並且會由目前索引中第一個索引鍵資料行的搜尋準則來建立新的搜尋金鑰。 如果指定 JET_bitNormalizedKey，則會捨棄任何先前現有的搜尋金鑰，並從輸入緩衝區載入新的搜尋金鑰。 在任何情況下，都不會變更資料庫狀態。

失敗時，如果指定了 JET_bitNormalizedKey 或 JET_bitNewKey，則不會定義搜尋索引鍵的狀態。 如果未指定 JET_bitNormalizedKey 或 JET_bitNewKey，將不會對搜尋索引鍵的狀態進行任何變更。 在任何情況下，都不會變更資料庫狀態。

#### <a name="remarks"></a>備註

金鑰應該視為不透明的資料區塊。 不應嘗試利用此資料的內部結構。 但是，下列已知所有 ESENT 金鑰：

  - 您可以使用 [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) 來相互比較索引鍵，以在來源索引項目目的資料表中建立原始索引的相對順序。

  - 將索引項目的索引鍵與不同索引的索引鍵進行比較是無意義的。

  - 金鑰一律小於或等於 JET_cbKeyMost (255) 個位元組，Windows Vista 之前的長度。 在 Windows Vista 和更新版本中，金鑰可以更大。 索引鍵的大小上限等於 JET_paramKeyMost 目前的值。

如果使用萬用字元選項，搜尋索引鍵的時間可能會較長一位元組。 在這種情況下，搜尋索引鍵最多可 JET_cbLimitKeyMost (256) 位元組用於 Windows vista 之前的版本，以及 JET_paramKeyMost vista 和更新版本的 Windows + 1 位元組。

此最大金鑰大小的 ramification 很重要。 只要索引項目的資料行值大到足以為該索引產生索引鍵，而該索引大於此大小上限時，就會以無訊息方式截斷該索引鍵的大小上限。 這會導致兩個效果：

  - 如果是唯一索引中的專案，則會導致其他唯一的專案宣告為重複專案。

  - 對於所有索引中的專案，索引鍵截斷會導致索引項目不符合指定搜尋索引鍵的搜尋準則，以宣告為相符專案。

應用程式必須預期此截斷，並避免它或補償其效果。 在 Windows Vista 中，已加入新的索引旗標 JET_bitIndexDisallowTruncation，讓應用程式更容易防止金鑰截斷。 如需此索引編制選項的詳細資訊，請參閱 [JET_INDEXCREATE](./jet-indexcreate-structure.md) 結構。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetRetrieveKey](./jetretrievekey-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
