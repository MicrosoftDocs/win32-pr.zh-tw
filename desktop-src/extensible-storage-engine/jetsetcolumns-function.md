---
description: 深入瞭解： JetSetColumns 函數
title: JetSetColumns 函式
TOCTitle: JetSetColumns Function
ms:assetid: a5b011dc-0da6-44bf-aaf5-352d8a57e5bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294050(v=EXCHG.10)
ms:contentKeyID: 32765649
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumns
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a62c3fee0b961268c11974e0a6064f091474d34
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984341"
---
# <a name="jetsetcolumns-function"></a>JetSetColumns 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetsetcolumns-function"></a>JetSetColumns 函式

**JetSetColumns** 函式與 [JetSetColumn](./jetsetcolumn-function.md)的行為類似，但是可讓應用程式在單一作業中設定多個資料行值。 [JET_SETCOLUMN](./jet-setcolumn-structure.md)結構的陣列用來描述要設定的資料行值集合，以及描述要設定之每個資料行值的輸入緩衝區。

```cpp
    JET_ERR JET_API JetSetColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_SETCOLUMN* psetcolumn,
      __in          unsigned long csetcolumn
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*tableid*

要用於此呼叫的資料指標。

*psetcolumn*

一或多個 [JET_SETCOLUMN](./jet-setcolumn-structure.md) 結構的陣列指標。 每個結構都包含要設定之資料行值的描述，以及要從哪裡取得要設定的資料行資料。

*csetcolumn*

*Psetcolumn* 所指定之陣列中的 [JET_SETCOLUMN](./jet-setcolumn-structure.md)結構數目。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errBadColumnId</p> | <p>提供的資料行識別碼超出資料行識別碼的合法限制。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p> | 
| <p>JET_errColumnIllegalNull</p> | <p>與 JET_errNullInvalid 相同。</p> | 
| <p>JET_errColumnNotFound</p> | <p>給定 <em>columnid</em> 所描述的資料行不存在於資料表中。</p> | 
| <p>JET_errColumnNotUpdatable</p> | <p>在插入複製刪除原始更新作業期間，嘗試更新長值的作業不合法。</p> | 
| <p>JET_errColumnTooBig</p> | <p>輸入緩衝區中提供的指定資料行值資料，超過固定長度資料行的自然大小限制，或是針對固定長度的文字或二進位資料行所設定的大小限制。 針對長資料行傳遞超過1024個位元組的資料，並設定 JET_bitSetIntrinsicLV 旗標時，也會傳回此錯誤。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>指定的資料行值資料大小不符合固定長度資料類型的自然內容。</p> | 
| <p>JET_errInvalidColumnType</p> | <p>在插入或更新作業期間，嘗試更新自動遞增資料行，或在取代作業期間更新版本資料行時，發生不合法的嘗試。</p> | 
| <p>JET_errInvalidgrbit</p> | <p>提供的選項未知，或已知位設定的不合法組合。</p> | 
| <p>JET_errInvalidParameter</p> | <p>給定的 psetinfo- &gt; cbStruct 不是 <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> 結構的有效大小。</p> | 
| <p>JET_errMultiValuedDuplicate</p> | <p>Set column 作業嘗試建立重複的值，並指定 JET_bitSetUniqueMultiValues 或 JET_bitSetUniqueNormalizedMultiValues。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errNotInTransaction</p> | <p>當呼叫會話不在交易中時，嘗試更新長的資料行值是不合法的。</p> | 
| <p>JET_errNullInvalid</p> | <p>嘗試將非 Null 資料行設定為 Null 是不合法的。</p> | 
| <p>JET_errRecordTooBig</p> | <p>無法將資料行值設定為輸入緩衝區中的值，因為它會導致記錄超過其頁面大小的相關大小限制。 <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>或<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>類型的資料行可以與剩餘的記錄資料分開儲存。 不過，其他資料行必須與記錄一起儲存，而且可能會導致超過記錄大小限制。 即使長的資料行在記錄內需要5個位元組的空間作為連結，但這也可能導致傳回 JET_errRecordTooBig。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>相同的會話無法同時用於一個以上的執行緒。 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 
| <p>JET_errUpdateNotPrepared</p> | <p>資料指標目前不在插入新記錄或更新現有記錄的過程中。</p> | 
| <p>JET_wrnColumnMaxTruncated</p> | <p>輸入緩衝區中的資料行值超過可變長度資料行所設定的最大長度，已被截斷。</p> | 



成功時，針對 psetcolumns 中所述的每個資料行，資料行值的所需部分會設定為從輸入緩衝區複製的資料。 如果資料行資料集超過為可變長度資料行指定的最大長度，可能已被截斷。

失敗時，資料指標位置會保持不變，而且複製緩衝區中不會更新任何資料行值資料。

#### <a name="remarks"></a>備註

如果任何個別的 set 資料行作業傳回錯誤，則整個 **JetSetColumns** 作業將會傳回錯誤。 一般情況下，警告會在 psetcolumns 中傳回 \> ，而不是在此函式的傳回碼中傳回。 但是，如果最後一個資料行集有警告，則會從 **JetSetColumns** 本身傳回此警告。

#### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 
| <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | 
| <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_COLTYP](./jet-coltyp.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_SETCOLUMN](./jet-setcolumn-structure.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)
