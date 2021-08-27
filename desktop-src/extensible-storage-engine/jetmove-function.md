---
description: 深入瞭解： JetMove 函數
title: JetMove 函式
TOCTitle: JetMove Function
ms:assetid: ded3cd21-8586-4d90-9efc-61213132d201
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294117(v=EXCHG.10)
ms:contentKeyID: 32765731
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetMove
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a0d00578f4f66af0b0cef76cef7193d0174e253a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983391"
---
# <a name="jetmove-function"></a>JetMove 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetmove-function"></a>JetMove 函式

**JetMove** 函式會將游標放在索引的開頭或結尾，然後將該索引中的專案向前或向後移動。 您也可以在目前索引上，以指定的索引項目數目向前或向後移動游標。 另一種方法是使用 [JetSetIndexRange](./jetsetindexrange-function.md)在資料指標上設定索引範圍，藉此限制可使用 **JetMove** 列舉的索引項目。

```cpp
    JET_ERR JET_API JetMove(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          long cRow,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*tableid*

要用於此呼叫的資料指標。

*烏鴉*

任意位移，表示所需的資料指標在目前索引上的移動。

除了標準位移之外，也可以使用下列其中一個選項來設定此參數。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_MoveFirst</p> | <p>將游標移至索引 (中的第一個索引項目目（如果有的話) ）。</p><p><strong>注意</strong>   -2147483648 的常值會用來表示這個選項。 請勿使用此值做為一般位移或可能導致非預期的行為。</p> | 
| <p>JET_MoveLast</p> | <p>將游標移至索引 (中的最後一個索引項目目（如果有的話）) 。</p><p><strong>注意</strong>   2147483647的常值會用來表示這個選項。 請勿使用此值做為一般位移或可能導致非預期的行為。</p> | 
| <p>JET_MoveNext</p> | <p>將游標移至索引 (中的下一個索引項目（如果有的話) ）。 此值完全等於 + 1 的一般位移。</p> | 
| <p>JET_MovePrevious</p> | <p>將游標移至索引 (中的前一個索引項目目（如果有的話) ）。</p><p>此值完全等於-1 的一般位移，或 0 (零) 。</p><p>游標會保持在目前的邏輯位置，並且會測試對應至該邏輯位置的索引項目目是否存在。</p> | 



*grbit*

指定零或多個下列選項的位群組。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitMoveKeyNE</p> | <p>向前或向後移動游標，以略過索引中所遇到的索引鍵值數目。 這會將具有重複索引鍵值的索引項目轉換成單一索引項目的效果。 通常，位移會將游標移至指定的索引項目數目，而不論其索引鍵值為何。</p> | 



### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。 若為 <strong>JetMove</strong>，這表示在要求的位置或在目前索引的位移上找到索引項目。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p><p><strong>Windows XP：</strong> 此傳回值會在 Windows XP 中引進。</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>資料指標目前不在索引項目上。 若為 <strong>JetMove</strong>，這表示在要求的位置或在目前索引的位移處找不到索引項目。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errRecordDeleted</p> | <p>資料指標目前以邏輯方式放置於對應至已刪除之記錄的索引項目目。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>作業無法完成，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>相同的會話無法同時用於一個以上的執行緒。</p><p><strong>Windows XP：</strong> 此傳回值會在 Windows XP 中引進。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉中。</p> | 



如果此函式成功，游標將定位於符合所要求位置或位移的索引項目。 如果已備妥記錄以進行更新，就會取消該更新。 如果索引範圍有效，且已指定 JET_MoveFirst 或 JET_MoveLast，將會取消該索引範圍。 不會變更資料庫狀態。

如果此函式失敗，除非傳回 JET_errNoCurrentRecord，否則資料指標的位置會保持不變。 在此情況下，游標將放置於符合所要求位置或位移的索引項目目。 資料指標可以相對於該位置移動，但仍不在有效的索引項目上。 如果已備妥記錄以進行更新，就會取消該更新。 如果索引範圍有效，且已指定 JET_MoveFirst 或 JET_MoveLast，將會取消該索引範圍。 不會變更資料庫狀態。

#### <a name="remarks"></a>備註

您可以使用 **JetMove**，在第一個和最後一個之後，將資料指標移至兩個特殊位置。 如果資料指標是在資料表中的第一個索引項目目上，而 **JetMove** 是以 JET_MovePrevious 呼叫，則呼叫會失敗併發生 JET_errNoCurrentRecord，而且資料指標會在邏輯上定位於索引中的第一個專案之前。 即使在索引中的第一個專案之前插入另一個索引項目，仍會維護此邏輯位置。 在最後一次相對於索引結尾之後，就會發生類似的情況。 當您設定要使用 **JetMove** 逐一查看的索引項目範圍時，在第一個和最後一個之前，最有用的是使用反覆運算器模型，該模型預期會在使用該專案之前，一律移至下一個 (或先前的) 元素。

可以透過在資料指標上設定索引範圍來限制 **JetMove** 可造訪的索引項目集合。 這對列舉一組索引項目的應用程式很有用，這些專案符合可透過針對該索引所建立的一對搜尋索引鍵來表示的簡單準則。 如需詳細資訊，請參閱 [JetSetIndexRange](./jetsetindexrange-function.md)。

在 Windows Server 2003 SP1 之前的版本中，在某些特定情況下發生 **JetMove** 問題，這會影響 [JetSetIndexRange](./jetsetindexrange-function.md)函數所設定之索引範圍的正確強制執行。 如果資料指標目前是在第一個索引項目之前，而且索引範圍設定的上限小於第一個索引項目，則下一次呼叫 **JetMove** 時，將會錯誤地移至該索引項目目，而不會如預期般與 JET_errNoCurrentRecord 失敗。 從索引結尾開始，類似的情況會發生相同的錯誤。 這種情況可能會發生在設定索引範圍的應用程式中，並使用預期會在第一個索引項目目（其為要列舉之專案集的成員）之前啟動的反覆運算器導覽，而不是從該集合的第一個索引項目目開始。 這種情況也會發生在類似的情況下，從索引的結尾開始。 因應措施是讓應用程式以手動方式確認取得的索引項目位於索引範圍內，方法是使用 JetRetrieveKey) 來比較目前索引 (項的索引鍵，以使用[](./jetretrievekey-function.md) ，其索引鍵代表目前索引範圍的結尾 (使用 JET_bitRetrieveCopy) 來[JetRetrieveKey](./jetretrievekey-function.md)抓取。

將計算位移傳遞給 **JetMove** 時，請務必小心。 如果計算的位移小於或等於 JET_MoveFirst，則該位移必須分割成多個片段，每個片段會分別傳遞至 **JetMove** ，但在單一交易內，以取得所需的效果。 大於或等於 JET_MoveNext 的位移也是如此。 應用程式不太可能在現實世界中進行這項工作，但在這種情況下，最好是根據 JET_MoveFirst 的不同語義和 JET_MoveLast 的一般位移來進行防禦。

使用非常大的位移呼叫 **JetMove** 時（例如，當魚尾紋參數設定為1000時）， **JetMove** 會將所有1000索引項目移至最後一個位置。 目前，ESE API 不會提供有效的方式，透過位移直接移至指定的索引項目，而不會跨越每個索引項目目。

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
[JetRetrieveKey](./jetretrievekey-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
