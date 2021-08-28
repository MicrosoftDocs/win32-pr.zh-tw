---
description: 深入瞭解： JetSetIndexRange 函數
title: JetSetIndexRange 函式
TOCTitle: JetSetIndexRange Function
ms:assetid: dac99576-707d-4713-9825-ddad1980723e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294112(v=EXCHG.10)
ms:contentKeyID: 32765726
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetIndexRange
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 330adc9b4d18a7bfa66ced0c9cb5776f31162be5
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988451"
---
# <a name="jetsetindexrange-function"></a>JetSetIndexRange 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetsetindexrange-function"></a>JetSetIndexRange 函式

**JetSetIndexRange** 函式會暫時限制索引項目的索引項目目集合，而資料指標可使用 [JetMove](./jetmove-function.md) ，從目前的索引項目目開始，然後結束于符合該資料指標中搜尋索引鍵所指定的搜尋條件，以及指定的系結準則中的索引項目目。 搜尋金鑰必須先前已使用 [JetMakeKey](./jetmakekey-function.md)來建立。

```cpp
    JET_ERR JET_API JetSetIndexRange(
      __in          JET_SESID sesid,
    __in          JET_TABLEID tableidSrc,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*tableidSrc*

要用於此呼叫的資料指標。

*grbit*

位群組，其中包含要用於此呼叫的選項，其中包含零或多個下列各項：


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitRangeInclusive</p> | <p>此選項的存在或不存在，表示索引範圍的界限準則。 如果有的話，這個選項會指出索引範圍的限制是內含的。 如果不存在，此選項表示索引範圍的限制為獨佔。 當索引範圍的限制為包含時，與搜尋準則完全相符的任何索引項目都會包含在範圍內。</p> | 
| <p>JET_bitRangeInstantDuration</p> | <p>此選項會要求在建立索引範圍時立即予以移除。 作業的所有其他層面都會保持不變。 這適合用來測試符合搜尋準則的索引項目是否存在。</p> | 
| <p>JET_bitRangeRemove</p> | <p>此選項會要求取消資料指標上的現有索引範圍。 一旦取消索引範圍後，就可以使用 <a href="gg294117(v=exchg.10).md">JetMove</a>移至索引範圍結尾以外的範圍。 如果索引範圍尚未生效， <strong>JetSetIndexRange</strong> 將會失敗，並 JET_errInvalidOperation。</p><p>指定此選項時，會忽略所有其他選項。</p> | 
| <p>JET_bitRangeUpperLimit</p> | <p>如果使用此選項，則資料指標中的搜尋索引鍵代表索引項目的搜尋準則，最接近索引的結尾會符合索引範圍。 索引範圍將會建立在目前的資料指標位置與此索引項目之間，以便找到所有相符專案，方法是使用 <a href="gg294117(v=exchg.10).md">JetMove</a> 搭配 JET_MoveNext 或正位移向前移動索引。</p><p>搭配使用 <a href="gg269329(v=exchg.10).md">JetMakeKey</a> 所建立的搜尋索引鍵，並不適合用來尋找最接近索引開頭的索引項目的萬用字元選項，這是使用此選項的意義。</p><p>如果省略這個選項，則資料指標中的搜尋索引鍵代表索引項目的搜尋準則，最接近索引的開頭會符合索引範圍。 索引範圍將會建立在目前的資料指標位置與此索引項目之間，以便找到所有相符專案，方法是使用 <a href="gg294117(v=exchg.10).md">JetMove</a> 搭配 JET_MovePrevious 或負位移，在索引上向前移動。</p><p>使用透過 <a href="gg269329(v=exchg.10).md">JetMakeKey</a> 所建立的搜尋索引鍵，並使用萬用字元選項來尋找最接近索引結尾的索引項目，以省略此選項的意義。</p> | 



### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p><p>若為 <strong>JetSetIndexRange</strong>，這表示現有的索引範圍已取消，或索引範圍內至少有一個索引項目目。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p><p>只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errInvalidOperation</p> | <p>當指定 JET_bitRangeRemove 且沒有任何索引範圍生效時， <strong>JetSetIndexRange</strong> 會傳回這個錯誤。</p> | 
| <p>JET_errKeyNotMade</p> | <p>沒有目前的資料指標搜尋索引鍵。 <strong>JetSetIndexRange</strong> 要求資料指標必須有有效的搜尋索引鍵，因為它會針對用來尋找索引項目的搜尋條件使用該索引鍵。</p> | 
| <p>JET_errNoCurrentIndex</p> | <p>沒有目前的資料指標索引。 如果資料指標位於資料表的叢集索引，但尚未定義主要索引，就會發生這種<strong>情況。</strong> 不支援設定這類索引的索引範圍。</p> | 
| <p>JET_errNoCurrentRecord</p> | <p><strong>JetSetIndexRange</strong>會傳回此錯誤，表示索引範圍內沒有任何索引項目。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>相同的會話無法同時用於一個以上的執行緒。</p><p>只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 



成功時，如果指定 JET_bitRangeRemove，則會取消目前作用中的索引範圍。 如果未指定 JET_bitRangeRemove，且指定了 JET_bitRangeInstantDuration，則沒有任何索引範圍生效。 如果未指定 JET_bitRangeRemove 或 JET_bitRangeInstantDuration，則新的索引範圍會生效。 此索引範圍會暫時限制索引項目的索引項目集合，資料指標可以使用 [JetMove](./jetmove-function.md) 從目前的索引項目目開始，然後結束于符合搜尋準則的索引項目。 資料指標的位置會保持不變。 如果已針對資料指標建立搜尋索引鍵，則會刪除該搜尋索引鍵。 不會變更資料庫狀態。

失敗時，如果未傳回 JET_errNoCurrentRecord，則沒有任何索引範圍生效。 如果傳回 JET_errNoCurrentRecord，則新的索引範圍會生效。 此索引範圍會暫時限制索引項目的索引項目集合，資料指標可以使用 [JetMove](./jetmove-function.md) 從目前的索引項目目開始，然後結束于符合搜尋準則的索引項目。 資料指標的位置會保持不變。 如果傳回 JET_errNoCurrentRecord，且已針對資料指標建立搜尋索引鍵，則會刪除該搜尋索引鍵。 不會變更資料庫狀態。

#### <a name="remarks"></a>備註

索引範圍是暫時性的，而且如果在資料指標上執行 [JetMove](./jetmove-function.md) 以外的任何導覽，則會自動取消。

索引範圍只能以一個方向運作。 如果已建立上限，則在到達索引範圍的結尾時，只會使用 [JetMove](./jetmove-function.md) 搭配 JET_MoveNext 或正數位移來轉送動作。 在此情況下，您仍然可以使用 [JetMove](./jetmove-function.md) 搭配 JET_MovePrevious 或負位移來保留索引範圍。 較低的限制會發生類似的情況。

#### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 
| <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | 
| <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetMakeKey](./jetmakekey-function.md)  
[JetMove](./jetmove-function.md)  
[JetSetIndexRange]()  
[JetStopService](./jetstopservice-function.md)
