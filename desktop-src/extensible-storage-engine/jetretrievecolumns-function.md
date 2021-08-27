---
description: 深入瞭解： JetRetrieveColumns 函數
title: JetRetrieveColumns 函式
TOCTitle: JetRetrieveColumns Function
ms:assetid: f7158fe8-ba4b-420c-9d45-185791a5759b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294135(v=EXCHG.10)
ms:contentKeyID: 32765749
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveColumns
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad6e1d39797c9a9ff965644ceea7858cb4af1a56
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472494"
---
# <a name="jetretrievecolumns-function"></a>JetRetrieveColumns 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetretrievecolumns-function"></a>JetRetrieveColumns 函式

**JetRetrieveColumns** 函數會從單一作業中的目前記錄抓取多個資料行值。 [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)結構的陣列用來描述要抓取的資料行值集合，以及描述要抓取之每個資料行值的輸出緩衝區。

```cpp
    JET_ERR JET_API JetRetrieveColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_RETRIEVECOLUMN* pretrievecolumn,
      __in          unsigned long cretrievecolumn
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*tableid*

要用於此呼叫的資料指標。

*pretrievecolumn*

一或多個 [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) 結構的陣列指標。 每個結構都包含要取得的資料行值的描述，以及要在哪裡儲存傳回的資料。

*cretrievecolumn*

*Pretrievecolumn* 所指定之陣列中的 [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)結構數目。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errBadItagSequence</p> | <p>傳遞了不正確多重值資料行序號值給 pretinfo- &gt; itagSequence。 多重值資料行值序號的有效值為1或更大。 值為 0 (零) 對此函數有效，但對 <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a>無效。</p> | 
| <p>JET_errBadColumnId</p> | <p>提供的資料行識別碼超出資料行識別碼的合法限制。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p> | 
| <p>JET_errColumnNotFound</p> | <p>給定 <em>columnid</em> 所描述的資料行不存在於資料表中。</p> | 
| <p>JET_errIndexTuplesCannotRetrieveFromIndex</p> | <p>無法從索引中取出索引為子字串的資料行，因為只有資料行的一小部分通常會出現在每個索引項目目中。</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>在某些情況下，為抓取資料行提供的緩衝區必須夠大，才能傳回任何數量的資料行值。 例如，將可更新的可更新資料行調整為在呼叫會話的交易內容中保持一致，而且這項調整需要呼叫端所提供的緩衝區。 如果提供的緩衝區空間不足，則會傳回 JET_errInvalidBufferSize，且不會傳回任何資料行資料。</p> | 
| <p>JET_errInvalidgrbit</p> | <p>提供的選項未知，或已知位設定的不合法組合。</p> | 
| <p>JET_errInvalidParameter</p> | <p>指定的一個或多個參數不正確。 如果 retinfo 的大小小於 <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>的大小，就會發生這種情況。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p><p><strong>Windows XP：</strong> 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>資料指標未放置在記錄上。 此情況具有許多不同的原因。 例如，如果資料指標目前位於目前索引的最後一筆記錄之後，就會發生這種情況。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>相同的會話無法同時用於一個以上的執行緒。</p><p><strong>Windows XP：</strong> 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 
| <p>JET_wrnBufferTruncated</p> | <p>無法取出整個資料行值，因為指定的緩衝區小於資料行的大小。</p> | 



成功時，會在提供的緩衝區中傳回資料行資料和資料行大小， [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) 結構的陣列中所述。 如果 *itagSequence* 設定為 0 (零) 表示需要多值欄位的實例數目而非資料行資料，則會在 *itagSequence* 欄位本身傳回多值資料行的實例數目。 每個 [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md) 結構都有一個錯誤欄位，其中包含所抓取資料行的警告。 如果資料行是 **Null** 值，則錯誤碼會設定為 JET_wrnColumnNull。

失敗時，資料指標位置會保持不變，且不會將任何資料複製到提供的緩衝區。

#### <a name="remarks"></a>備註

**JetRetrieveColumns** 支援 [JetRetrieveColumn](./jetretrievecolumn-function.md) 不支援的其中一項功能。 這是捕獲多值資料行實例數目的能力。 這項功能的目的是讓應用程式取出資料行的所有值。 這可以藉由先判斷資料行具有的值數目來完成。 接下來，您可以使用為每個值配置的一個 [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)結構，再次呼叫 **JetRetrieveColumns** 來判斷資料行資料的長度，藉以判斷其長度。 這可以藉由傳遞 *cbMax* 為 0 () 零的 **Null**_pvData_ 指標來完成，並在 *cbActual* 中抓取資料行長度。 第三個和最後一個呼叫可以使用配置的記憶體做為資料行值資料。

如果任何資料行由於長度不足的緩衝區而遭到截斷，則 API 會傳回 JET_wrnBufferTruncated。 不過，其他錯誤 JET_wrnColumnNull 只會在 [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)的 [錯誤] 欄位中傳回。 這是因為應用程式通常會想要確保所有的資料都已從 **JetRetrieveColumns** 中取出並傳回此錯誤，以促進這項理解。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumns](./jetsetcolumns-function.md)
