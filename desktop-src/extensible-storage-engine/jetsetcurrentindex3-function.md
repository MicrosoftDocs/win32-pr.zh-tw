---
description: 深入瞭解： JetSetCurrentIndex3 函數
title: JetSetCurrentIndex3 函式
TOCTitle: JetSetCurrentIndex3 Function
ms:assetid: 50050bd3-4b74-4be7-985c-754ced8aded1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269244(v=EXCHG.10)
ms:contentKeyID: 32765546
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex3A
- JetSetCurrentIndex3W
- JetSetCurrentIndex3
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 36aadb42cdf942c802a65f92b5c450535575793b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986651"
---
# <a name="jetsetcurrentindex3-function"></a>JetSetCurrentIndex3 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetsetcurrentindex3-function"></a>JetSetCurrentIndex3 函式

**JetSetCurrentIndex3** 函數是用來設定資料指標的目前索引。 資料指標的目前索引會定義資料表中的哪些記錄可以顯示在該資料指標，以及選取一組要用來公開這些記錄的索引項目目順序。

```cpp
    JET_ERR JET_API JetSetCurrentIndex3(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      JET_PCSTR szIndexName,
      __in          JET_GRBIT grbit,
      __in          unsigned long itagSequence
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*tableid*

要用於此呼叫的資料指標。

*szIndexName*

要為數據指標選取的索引名稱。

如果此參數為 Null 或空字串，則會選取叢集索引。 如果定義了資料表的主要索引，則會選取該索引，因為它與叢集索引相同。 如果未定義資料表的主要索引，則會選取連續索引。 順序索引沒有索引定義。 如需詳細資訊，請參閱 [JetCreateIndex](./jetcreateindex-function.md) 。

如果 *pindexid* 不是 Null，則會忽略索引名稱，並且會依索引識別碼來選取索引。

*grbit*

位群組，其中包含要用於此呼叫的選項，包括下列零或多個。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitMoveFirst</p> | <p>此選項表示資料指標應放置在指定之索引的第一個專案。 如果選取叢集索引 (主要索引或連續索引) ，而且目前的索引是次要索引，則會假設 JET_bitMoveFirst。 如果正在選取目前的索引，則會忽略此選項，且不會變更資料指標的位置。</p> | 
| <p>JET_bitNoMove</p> | <p>此選項表示資料指標應放置在新索引的索引項目上，此索引會對應到與舊索引上之資料指標目前位置的索引項目目相關聯的記錄。</p><p>如果新索引的定義至少包含一個多重值索引鍵資料行，則目的地索引項目不明確。 在此情況下，會使用指定的 <em>itagSequence</em> 來選取最重要的多重值索引鍵資料行用來放置資料指標的多重值。 即使在多個多重值索引鍵資料行的情況下，只需要傳遞單一 <em>itagSequence</em> ，因為引擎只會展開最重要多重值索引鍵資料行的所有值。 如需詳細資訊，請參閱 <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> 。</p><p>如果指定 JET_bitMoveFirst，則會忽略此選項。</p><p>如果正在選取目前的索引，則會忽略此選項，且不會變更資料指標的位置。 如果這個參數不存在，則會假設其值為 JET_bitMoveFirst。</p> | 



*itagSequence*

多值資料行值的序號，此值會用來將資料指標放置在新的索引上。

此參數只會搭配 JET_bitNoMove 使用。 如需詳細資訊，請參閱此選項的描述。

當這個參數不存在或設為零時，其值會假設為1。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errBadItagSequence</p> | <p>正在使用 JET_bitNoMove 選項來選取次要索引，且新索引定義中的第一個多重值索引鍵資料行沒有對應至指定序號的值。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p><p>只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errInvalidIndexId</p> | <p>索引識別碼的內容無效或已過期，需要重新整理。 在下列情況下， <strong>JetSetCurrentIndex3</strong> 可能會發生：</p><ul><li><p>pindexid- &gt; cbStruct 不是預期的大小 (Windows Server 2003 和更新版本) 。</p></li><li><p>引擎已在提取索引識別碼之後關閉。</p></li><li><p>所有參考資料表的資料指標（包含對應至索引識別碼的索引）已關閉，且引擎已從架構快取中收回該索引的定義。</p></li><li><p>索引識別碼正在搭配在錯誤資料表上開啟的資料指標使用。</p></li><li><p>索引已卸載或尚未顯示在會話中。</p></li></ul> | 
| <p>JET_errInvalidName</p> | <p>其中一個指定的物件名稱無效。 所有物件名稱都必須符合同一組規則。 這些規則如下：</p><ul><li><p>物件名稱必須由 ASCII 字元組成。</p></li><li><p>物件名稱的長度必須至少有一個字元。</p></li><li><p>物件名稱的長度不得超過 JET_cbNameMost (64) 個字元。</p></li><li><p>物件名稱不能以空格開頭。</p></li><li><p>物件名稱不能包含 ASCII 控制字元 (0x00 到 0x1F) 。</p></li><li><p>物件名稱不能包含驚嘆號 (！ ) 、句號 (. ) 、左括弧 ( [) 或右括弧 (] ) 字元。</p></li><li><p>一旦經過驗證之後，就只會將字串的部分寫入第一個空格 (如果有任何) 將用於物件名稱。 這實際上是指物件名稱不能包含空格。</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。 當<em>pindexid</em>不是 Null，且 pindexid cbStruct 不是預期的大小 (Windows XP 和舊版) <strong>時，就</strong>會發生這種情況 &gt; 。</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>正在使用 JET_bitNoMove 選項來選取次要索引，而新的索引中沒有索引項目對應至在舊索引上目前的資料指標位置與索引項目目相關聯的記錄。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errOutOfCursors</p> | <p>引擎已用盡用來開啟資料指標的資源集區。 可以在任何時間開啟的資料指標數目上限是使用 <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>來控制。 如需詳細資訊，請參閱 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 。 當選取次要索引，且引擎無法開啟內部資料指標來使用該索引時， <strong>JetSetCurrentIndex3</strong> 就會發生這種情況。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>相同的會話無法同時用於一個以上的執行緒。</p><p>只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 



成功時，會將資料指標的目前索引設定為要求的索引。 根據所要求索引的索引定義，現在可以使用 [JetSeek](./jetseek-function.md) 來搜尋索引項目。 您也可以使用 [JetMove](./jetmove-function.md) ，以該索引定義所指定的順序來列舉索引項目。 資料指標的目前位置是設定為索引上的第一個索引項目目 (JET_bitMoveFirst) 或與舊索引 (JET_bitNoMove) 上目前的資料指標位置相關的特定索引項目。 不會變更資料庫狀態。

失敗時，目前的索引和目前的資料指標位置處於未定義狀態。 不會變更資料庫狀態。

#### <a name="remarks"></a>備註

如果索引識別碼提示已過時，則 API 只會失敗。 在此情況下，不會回復到索引的文字名稱。 此回復必須由 API 的呼叫端手動完成。

#### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 
| <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | 
| <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 
| <p><strong>Unicode</strong></p> | <p>實作為 <strong>JetSetCurrentIndex3W</strong> (Unicode) 和 <strong>JetSetCurrentIndex3A</strong> (ANSI) 。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXID](./jet-indexid-structure.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetGetCurrentIndex](./jetgetcurrentindex-function.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetMove](./jetmove-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetSeek](./jetseek-function.md)
