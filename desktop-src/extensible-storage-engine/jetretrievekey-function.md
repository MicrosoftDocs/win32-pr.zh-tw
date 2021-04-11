---
description: 深入瞭解： JetRetrieveKey 函數
title: JetRetrieveKey 函式
TOCTitle: JetRetrieveKey Function
ms:assetid: a96d0a7c-f1db-48bc-807d-4e6357aec726
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294051(v=EXCHG.10)
ms:contentKeyID: 32765650
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveKey
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8e560d28447b7e5d3798949f47dcadf259e49d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027431"
---
# <a name="jetretrievekey-function"></a>JetRetrieveKey 函式


_**適用于：** Windows |Windows Server_

## <a name="jetretrievekey-function"></a>JetRetrieveKey 函式

**JetRetrieveKey** 函式會在資料指標的目前位置，抓取索引項目的索引鍵。 這類金鑰是由呼叫 [JetMakeKey](./jetmakekey-function.md)所構成。 然後，您可以使用抓取的金鑰，藉由呼叫 [JetSeek](./jetseek-function.md)，有效率地將該資料指標傳回相同的索引項目。

```cpp
    JET_ERR JET_API JetRetrieveKey(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvData,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*tableid*

要用於此呼叫的資料指標。

*pvData*

將接收金鑰的輸出緩衝區。

*cbMax*

輸出緩衝區的大小上限（以位元組為單位）。

*pcbActual*

接收金鑰的實際大小（以位元組為單位）。

如果這個參數為 Null，則不會傳回實際的索引鍵大小。

如果輸出緩衝區太小，則仍會傳回實際的金鑰大小。 這表示這個數位會大於輸出緩衝區的大小。

*grbit*

位群組，其中包含要用於此呼叫的選項，包括下列零或多個。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>值</p></th>
<th><p>意義</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitRetrieveCopy</p></td>
<td><p>當指定時，引擎會傳回資料指標的搜尋索引鍵。 搜尋索引鍵是使用一或多個先前的 <a href="gg269329(v=exchg.10).md">JetMakeKey</a> 呼叫來建立的，目的是要使用 <a href="gg294103(v=exchg.10).md">JetSeek</a> 來搜尋該金鑰，或使用 <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a>設定索引範圍。</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>傳回碼</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>作業已成功完成。</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。 只有 Windows XP 和更新版本才會傳回此錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyNotMade</p></td>
<td><p>沒有目前的資料指標搜尋索引鍵。 如果指定 JET_bitRetrieveCopy，且尚未使用先前的<a href="gg269329(v=exchg.10).md">JetMakeKey</a>呼叫來為此資料指標建立搜尋索引鍵<strong>，則會</strong>發生這種情況。 搜尋索引鍵將會由先前呼叫 <a href="gg294117(v=exchg.10).md">JetMove</a>以外的資料指標上的任何導覽 API 來刪除。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>資料指標未放置在記錄上。 此情況具有許多不同的原因。 例如，如果資料指標目前位於目前索引的最後一筆記錄之後，就會發生這種情況。</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>相同的會話無法同時用於一個以上的執行緒。 只有 Windows XP 和更新版本才會傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在關閉。</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnBufferTruncated</p></td>
<td><p>作業已順利完成，但輸出緩衝區太小，無法接收整個金鑰。 輸出緩衝區已填滿最適合的索引鍵數量。 如果要求，也會傳回實際的金鑰大小。</p>
<p><strong>注意</strong>   如果指定 JET_bitRetrieveCopy，將不會傳回此錯誤。 如需詳細資訊，請參閱「備註」一節。</p></td>
</tr>
</tbody>
</table>


成功時，會在輸出緩衝區中傳回索引項目在資料指標目前位置的索引鍵索引鍵。 如果傳回 JET_wrnBufferTruncated，輸出緩衝區將會包含所提供空間中最多的索引鍵，而且金鑰的實際大小將會正確。 不會變更資料庫狀態。

失敗時，輸出緩衝區的狀態和金鑰的實際大小將會是未定義的。 不會變更資料庫狀態。

#### <a name="remarks"></a>備註

金鑰通常應該視為不透明的資料區塊。 不應嘗試利用此資料的內部結構。 不過，您可以知道所有 ESENT 機碼的下列屬性：

  - 您可以使用 [memcmp](https://msdn.microsoft.com/library/aa246467\(vs.60\).aspx) 函式，將索引鍵與其他索引鍵進行比較，以在來源索引項目資料表的原始索引中建立其相對順序。

  - 將索引項目的索引鍵與不同索引的索引鍵進行比較是無意義的。

  - 在 Windows Vista 之前，索引鍵一律小於或等於 JET_cbKeyMost (255) 位元組。 在 Windows Vista 和更新版本中，金鑰可以更大。 索引鍵的大小上限等於 JET_paramKeyMost 目前的值。

除了上述的 ESENT 按鍵屬性之外，請務必注意，搜尋索引鍵與索引項目的索引鍵不同。 具體而言，搜尋索引鍵的長度可能會超過一般的按鍵。 當您在建立搜尋索引鍵時使用萬用字元選項時，就會發生這個額外的長度。 如需詳細資訊，請參閱 [JetMakeKey](./jetmakekey-function.md) 。

此 API 存在所有版本中的重要 bug。 如果使用 JET_bitRetrieveCopy 來要求搜尋索引鍵，而且輸出緩衝區太小而無法接收整個金鑰，則不會傳回 JET_wrnBufferTruncated。 將會改為傳回 JET_errSuccess。 請務必確認使用 *pcbActual* 所傳回之金鑰的實際大小，是否小於或等於輸出緩衝區的大小。 如果實際大小大於輸出緩衝區的大小，則 **JetRetrieveKey** 的呼叫端應該會回應，如同改為傳回 JET_wrnBufferTruncated。

#### <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>用戶端</strong></p></td>
<td><p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p></td>
</tr>
<tr class="even">
<td><p><strong>伺服器</strong></p></td>
<td><p>需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</p></td>
</tr>
<tr class="odd">
<td><p><strong>標頭</strong></p></td>
<td><p>宣告于 Esent. h 中。</p></td>
</tr>
<tr class="even">
<td><p><strong>程式庫</strong></p></td>
<td><p>使用 ESENT。</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>需要 ESENT.dll。</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetMakeKey](./jetmakekey-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
