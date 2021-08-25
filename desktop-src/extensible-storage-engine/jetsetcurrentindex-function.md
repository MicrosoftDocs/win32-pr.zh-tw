---
description: 深入瞭解： JetSetCurrentIndex 函數
title: JetSetCurrentIndex 函式
TOCTitle: JetSetCurrentIndex Function
ms:assetid: a2a15eab-b8bf-4a67-a63a-830ed1fdb3d9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294046(v=EXCHG.10)
ms:contentKeyID: 32765645
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex
- JetSetCurrentIndexA
- JetSetCurrentIndexW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0418665851bc1f4cf5d8e7df6b7c696d4458b869
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481244"
---
# <a name="jetsetcurrentindex-function"></a>JetSetCurrentIndex 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetsetcurrentindex-function"></a>JetSetCurrentIndex 函式

**JetSetCurrentIndex** 函數可以用來設定資料指標目前的索引。 資料指標的目前索引會定義資料表中的哪些記錄可以顯示在該資料指標，以及選取一組要用來公開這些記錄的索引項目目順序。

```cpp
    JET_ERR JET_API JetSetCurrentIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      const tchar* szIndexName
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

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errBadItagSequence</p> | <p>正在使用 JET_bitNoMove 選項來選取次要索引，且新索引定義中的第一個多重值索引鍵資料行沒有對應至指定序號的值。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p> | 
| <p>JET_errInvalidIndexId</p> | <p>索引識別碼的內容無效或已過期，需要重新整理。 在下列情況下， <strong>JetSetCurrentIndex</strong> 可能會發生：</p><ul><li><p>pindexid- &gt; cbStruct 不是預期的大小 (Windows Server 2003 和更新版本) 。</p></li><li><p>引擎已在提取索引識別碼之後關閉。</p></li><li><p>所有參考資料表的資料指標（包含對應至索引識別碼的索引）已關閉，且引擎已從架構快取中收回該索引的定義。</p></li><li><p>索引識別碼正在搭配在錯誤資料表上開啟的資料指標使用。</p></li><li><p>索引已卸載或尚未顯示在會話中。</p></li></ul> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p><p>只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errInvalidName</p> | <p>其中一個指定的物件名稱無效。 所有物件名稱都必須符合同一組規則。 這些規則如下：</p><ul><li><p>物件名稱必須由 ASCII 字元組成。</p></li><li><p>物件名稱的長度必須至少有一個字元。</p></li><li><p>物件名稱的長度不得超過 JET_cbNameMost (64) 個字元。</p></li><li><p>物件名稱不能以空格開頭。</p></li><li><p>物件名稱不能包含 ASCII 控制字元 (0x00 到 0x1F) 。</p></li><li><p>物件名稱不能包含驚嘆號 (！ ) 、句號 (. ) 、左括弧 ( [) 或右括弧 (] ) 字元。</p></li><li><p>一旦經過驗證之後，就只會將字串的部分寫入第一個空格 (如果有任何) 將用於物件名稱。 這實際上是指物件名稱不能包含空格。</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。 當<em>pindexid</em>不是 Null，且 pindexid cbStruct 不是預期的大小 (Windows XP 和舊版) <strong>時，就</strong>會發生這種情況 &gt; 。</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>正在使用 JET_bitNoMove 選項來選取次要索引，而新的索引中沒有索引項目對應至在舊索引上目前的資料指標位置與索引項目目相關聯的記錄。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errOutOfCursors</p> | <p>引擎已用盡用來開啟資料指標的資源集區。 可以在任何時間開啟的資料指標數目上限是使用 <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>來控制。 如需詳細資訊，請參閱 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 。 當選取次要索引，且引擎無法開啟內部資料指標來使用該索引時， <strong>JetSetCurrentIndex</strong> 就會發生這種情況。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>相同的會話無法同時用於一個以上的執行緒。</p><p>只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 



成功時，會將資料指標的目前索引設定為要求的索引。 根據所要求索引的索引定義，現在可以使用 [JetSeek](./jetseek-function.md) 來搜尋索引項目。 您也可以使用 [JetMove](./jetmove-function.md) ，以該索引定義所指定的順序來列舉索引項目。 資料指標的目前位置是設定為索引上的第一個索引項目目 (JET_bitMoveFirst) 或與舊索引 (JET_bitNoMove) 上目前的資料指標位置相關的特定索引項目。 不會變更資料庫狀態。

失敗時，目前的索引和目前的資料指標位置處於未定義狀態。 不會變更資料庫狀態。

#### <a name="remarks"></a>備註

如果索引識別碼提示已過時，則 API 只會失敗。 在此情況下，不會回復到索引的文字名稱。 此回復必須由 API 的呼叫端手動完成。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | | <p><strong>Unicode</strong></p> | <p>實作為 <strong>JetSetCurrentIndexW</strong> (Unicode) 和 <strong>JetSetCurrentIndexA</strong> (ANSI) 。</p> | 



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
[JetSeek](./jetseek-function.md)  
[JetSetCurrentIndex]()  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)
