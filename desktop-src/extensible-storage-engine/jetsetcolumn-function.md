---
description: 深入瞭解： JetSetColumn 函數
title: JetSetColumn 函式
TOCTitle: JetSetColumn Function
ms:assetid: f8877519-86d5-4e59-95a8-1927c70cd6b4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294137(v=EXCHG.10)
ms:contentKeyID: 32765751
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumn
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d37762166f079c7810a5ea28f2affe460d3bc08f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478274"
---
# <a name="jetsetcolumn-function"></a>JetSetColumn 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetsetcolumn-function"></a>JetSetColumn 函式

**JetSetColumn** 函式會修改修改過的記錄中要插入的單一資料行值，或更新目前的記錄。 它可以覆寫現有的值、將新的值加入至多重值資料行中的值序列、從多重值資料行中的值序列移除值，或更新完整或部分的完整值、 [JET_coltypLongText](./jet-coltyp.md) 或 [JET_coltypLongBinary](./jet-coltyp.md)類型的資料行。

```cpp
    JET_ERR JET_API JetSetColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __in_opt      const void* pvData,
      __in          unsigned long cbData,
      __in          JET_GRBIT grbit,
      __in_opt      JET_SETINFO* psetinfo
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*tableid*

要用於此呼叫的資料指標。

*columnid*

要抓取之資料行的 [JET_COLUMNID](./jet-columnid.md) 。 或者，您可以指定 *columnid* 值 0 (零) 。 當 *columnid* 0 (零) 時，所有標記的資料行、稀疏和多重值資料行都會被視為單一資料行。 這有助於抓取記錄中所有的稀疏資料行。

*pvData*

輸入緩衝區，其中包含要用於資料行值的資料。

*cbData*

輸入緩衝區的大小（以位元組為單位）。

*grbit*

位群組，其中包含要用於此呼叫的選項，其中包含零或多個下列各項：


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitSetAppendLV</p> | <p>這個選項是用來將資料附加至類型 <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> 或 <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>的資料行。 您可以藉由判斷現有 long 值的大小，並在<em>psetinfo</em>中指定<em>ibLongValue</em> ，來達成相同的行為。 不過，使用此 <em>grbit</em> 比較簡單，因為不需要知道現有資料行值的大小。</p> | 
| <p>JET_bitSetOverwriteLV</p> | <p>這個選項是用來將現有的 long 值取代為新提供的資料。 使用這個選項時，就好像現有的 long 值已設定為 0 (零) 長度，然後再設定新的資料。</p> | 
| <p>JET_bitSetRevertToDefaultValue</p> | <p>此選項僅適用于已標記、稀疏或多重值的資料行。 它會在後續的取出資料行作業中，讓資料行傳回預設資料行值。 移除所有現有的資料行值。</p> | 
| <p>JET_bitSetSeparateLV</p> | <p>此選項用來強制將長值（類型 <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> 或 <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>的資料行）與記錄資料的其餘部分分開儲存。 這種情況通常會在長值的大小防止與剩餘的記錄資料一起儲存時發生。 不過，這個選項可以用來強制儲存較長的值。 請注意，在大小較小的四個位元組之間，不能被強制分開。 在這種情況下，會忽略選項。</p> | 
| <p>JET_bitSetSizeLV</p> | <p>此選項可用來將輸入緩衝區轉譯為整數位節數，以設定為指定 <em>columnid</em> 所描述的完整值長度（如果有提供的話），psetinfo-itagSequence 中的序號 &gt; 。 如果指定的大小大於現有的資料行值，資料行會以0到0進行擴充。 如果大小小於現有的資料行值，則會截斷此值。</p> | 
| <p>JET_bitSetUniqueMultiValues</p> | <p>此選項用來強制多重值資料行中的所有值都是相異的。 此選項會將來源資料行資料（沒有任何轉換）與其他現有的資料行值進行比較，如果找到重複的資料，就會傳回錯誤。 如果指定此選項，則也不能指定 JET_bitSetAppendLV、JET_bitSetOverwriteLV 和 JET_bitSetSizeLV。</p> | 
| <p>JET_bitSetUniqueNormalizedMultiValues</p> | <p>此選項用來強制多重值資料行中的所有值都是相異的。 這個選項會比較資料行資料的索引鍵正規化轉換，以及其他類似轉換的現有資料行值，如果找到重複的資料行，就會傳回錯誤。 如果指定此選項，則也不能指定 JET_bitSetAppendLV、JET_bitSetOverwriteLV 和 JET_bitSetSizeLV。</p> | 
| <p>JET_bitSetZeroLength</p> | <p>此選項可用來將值設定為零長度。 一般來說，資料行值會藉由將 0 (零) 的 cbMax 傳遞至 <strong>Null</strong> 。 不過，對於某些類型，例如 <a href="gg269213(v=exchg.10).md">JET_coltypText</a>，資料行值可以是 0 (零) 長度，而不是 <strong>null</strong>，而且此選項可用來區分 <strong>null</strong> 和 0 (零) 長度。</p><p><strong>注意</strong>  一般情況下，如果資料行是固定長度的資料行，則會忽略這個位並將資料行設定為 <strong>Null</strong>。 但是，如果資料行是固定長度的標記資料行，資料行長度就會設定為0。 當固定長度的標記資料行設定為0時，嘗試使用 <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> 或 <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a> 來取出資料行將會成功，但在 <em>cbActual</em> 參數中傳回的實際長度為0。</p> | 
| <p>JET_bitSetIntrinsicLV</p> | <p>此選項是用來將完整的長數值儲存在記錄中。</p> | 
| <p>JET_bitSetCompressed</p> | <p>此選項可用來在儲存資料時嘗試資料壓縮。</p><p><strong>Windows 7：</strong> JET_bitSetCompressed 會在 Windows 7 中引進。</p> | 
| <p>JET_bitSetUncompressed</p> | <p>儲存資料時，使用這個選項不會嘗試壓縮。</p><p><strong>Windows 7：</strong> JET_bitSetUnCompressed 會在 Windows 7 中引進。</p> | 



*psetinfo*

可使用 [JET_SETINFO](./jet-setinfo-structure.md) 結構為此函式設定之選擇性輸入參數的指標。

如果將 *psetinfo* 指定為 **Null** ，則函式的行為會如同 *ItagSequence* 為1，而 *ibLongValue* 為 0 (零) 。 這會導致資料行集設定多重值資料行的第一個值，並設定從位移0開始的長資料 (零) 。

您可以為此參數設定下列選項：


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>ibLongValue</p> | <p>要在其中開始設定資料的長資料行值的二進位位移。</p> | 
| <p>itagSequence</p> | <p>要設定之所需多重值資料行值的序號。 如果 <em>itagSequence</em> 設定為 0 (零) ，則提供的值應該附加到多值值序列的結尾。 如果提供的序號大於最後一個現有的多重值，則會再次將指定的值附加至值序列的結尾。 如果序號對應至現有的值，則該值會取代為指定的值。</p> | 



### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errBadColumnId</p> | <p>提供的資料行識別碼超出資料行識別碼的合法限制。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p> | 
| <p>JET_errColumnNotFound</p> | <p>給定 <em>columnid</em> 所描述的資料行不存在於資料表中。</p> | 
| <p>JET_errColumnNotUpdatable</p> | <p>在插入複製刪除原始更新作業期間，嘗試更新長值的作業不合法。</p> | 
| <p>JET_errColumnTooBig</p> | <p>輸入緩衝區中提供的指定資料行值資料，超過固定長度資料行的自然大小限制，或是針對固定長度的文字或二進位資料行所設定的大小限制。 針對長資料行傳遞超過1024個位元組的資料，並設定 JET_bitSetIntrinsicLV 旗標時，也會傳回此錯誤。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p><p><strong>Windows XP：</strong> 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>指定的資料行值資料大小不符合固定長度資料類型的自然內容。</p> | 
| <p>JET_errInvalidColumnType</p> | <p>在插入或更新作業期間，嘗試更新自動遞增資料行，或在取代作業期間更新版本資料行時，發生不合法的嘗試。</p> | 
| <p>JET_errInvalidgrbit</p> | <p>提供的選項未知，或已知位設定的不合法組合。</p> | 
| <p>JET_errInvalidParameter</p> | <p>給定的 psetinfo- &gt; cbStruct 不是 <a href="gg294090(v=exchg.10).md">JET_SETINFO</a> 結構的有效大小。</p> | 
| <p>JET_errMultiValuedDuplicate</p> | <p>Set column 作業嘗試建立重複的值，並指定 JET_bitSetUniqueMultiValues 或 JET_bitSetUniqueNormalizedMultiValues。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errNotInTransaction</p> | <p>當呼叫會話不在交易中時，嘗試更新長的資料行值是不合法的。</p> | 
| <p>JET_errNullInvalid</p> | <p>嘗試將非<strong>null</strong> 資料行設定為 <strong>null</strong>是不合法的。</p> | 
| <p>JET_errColumnIllegalNull</p> | <p>與 JET_errNullInvalid 相同。</p> | 
| <p>JET_errRecordTooBig</p> | <p>無法將資料行值設定為輸入緩衝區中的值，因為它會導致記錄超過其頁面大小的相關大小限制。 <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>或<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a>類型的資料行可以與剩餘的記錄資料分開儲存。 不過，其他資料行必須與記錄一起儲存，而且可能會導致超過記錄大小限制。 即使長的資料行在記錄內需要5個位元組的空間作為連結，但這也可能導致傳回 JET_errRecordTooBig。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>相同的會話無法同時用於一個以上的執行緒。</p><p><strong>Windows XP：</strong> 只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 
| <p>JET_errUpdateNotPrepared</p> | <p>資料指標目前不在插入新記錄或更新現有記錄的過程中。</p> | 
| <p>JET_errVersionStoreOutOfMemory</p> | <p>當版本存放區的設定大小不足以保存所有未處理的更新時，就會發生此錯誤。</p> | 
| <p>JET_wrnColumnMaxTruncated</p> | <p>輸入緩衝區中的資料行值超過可變長度資料行所設定的最大長度，已被截斷。</p> | 



成功時，指定資料行之資料行值的所需部分會設定為從輸入緩衝區複製的資料。 如果資料集超過為可變長度資料行指定的最大長度，可能已被截斷。

失敗時，資料指標位置會保持不變，而且複製緩衝區中不會更新任何資料行值資料。

#### <a name="remarks"></a>備註

設定 long 值、 [JET_coltypLongText](./jet-coltyp.md)或[JET_coltypLongBinary](./jet-coltyp.md)類型之資料行[JET_coltypLongBinary](./jet-coltyp.md)的值，只有在呼叫會話在交易中時才會完成。 如果呼叫會話不在交易中，則修改儲存的較長值可能會完全認可，即使稍後取消更新作業也是一樣。 如果呼叫端會話是在交易中，則可以藉由取消更新並回復會話交易，來完全回復更新的影響。

由於 **JetSetColumn** 作業的結果，不會執行索引更新。 相反地，只有在所有資料行修改都已完成並呼叫 [JetUpdate](./jetupdate-function.md) 之後，才會更新索引。 當索引牽涉到多個要修改的資料行時，這會允許最有效率的索引更新。

記錄的大小限制為根據資料庫頁面大小。 記錄中大於五個位元組的任何 long 值將會與記錄分開儲存，因為記錄中的資料會因為 **JetSetColumn** 作業而超過其限制。 只有在所有可分離的記錄資料行資料都與記錄分開儲存，而且記錄仍超過記錄大小限制之後，才會傳回錯誤 JET_errRecordTooBig。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_SETINFO](./jet-setinfo-structure.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumns](./jetsetcolumns-function.md)
