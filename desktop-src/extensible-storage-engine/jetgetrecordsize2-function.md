---
description: 深入瞭解： JetGetRecordSize2 函數
title: JetGetRecordSize2 函式
TOCTitle: JetGetRecordSize2 Function
ms:assetid: 803cfb4e-44f3-447a-b642-018e6f2f713f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269314(v=EXCHG.10)
ms:contentKeyID: 32765604
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordSize2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5c68eafaaa53b5b88e6b003bdbafce287035cbc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981699"
---
# <a name="jetgetrecordsize2-function"></a>JetGetRecordSize2 函式


_**適用于：** Windows |Windows Server_

## <a name="jetgetrecordsize2-function"></a>JetGetRecordSize2 函式

**JetGetRecordSize2** 函數會從所需的位置抓取記錄大小資訊。

**Windows 7： JetGetRecordSize2** 是在 windows 7 作業系統中引進。

```cpp
    JET_ERR JET_API JetGetRecordSize2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECSIZE2* precsize,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

識別將用於 API 呼叫的資料庫會話內容。

*tableid*

識別將用於 API 呼叫的資料表或資料指標。 資料指標必須放置在記錄上，或已備妥更新。

*precsize*

[JET_RECSIZE2](./jet-recsize2-structure.md)結構之輸出緩衝區的指標。

*grbit*

這是下列一或多個值。

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
<td><p>JET_bitRecordSizeInCopyBuffer</p></td>
<td><p>這會抓取已準備進行更新的複製緩衝區中記錄的大小。 否則， <em>tableid</em> 或資料指標必須放置在記錄上，而且將會使用該記錄。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRecordSizeRunningTotal</p></td>
<td><p>當指定這個位時，在填滿內容之前， <a href="gg269174(v=exchg.10).md">JET_RECSIZE2</a> 不會歸零，可有效地做為已造訪或已更新之多筆記錄的統計資料累積。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRecordSizeLocal</p></td>
<td><p>這會導致 API 忽略非內建函式的 Long 值。 例如，只會使用頁面上的本機記錄。</p></td>
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
<td><p>JET_errInvalidGrbit</p></td>
<td><p>其中一個要求的選項無效或未執行。 當指定了不合法的<em>grbit</em>時， <strong>JetGetRecordSize2</strong>函數會傳回這個錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p>
<p><strong>WINDOWS XP：  </strong>只有 Windows XP 作業系統和更新版本的 Windows 才會傳回 JET_errInstanceUnavailable。</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在關閉。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>同時針對多個執行緒使用相同的會話是不合法的。</p>
<p><strong>WINDOWS XP：  </strong>只有 Windows XP 和更新版的 Windows 才會傳回 JET_errInstanceUnavailable。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>如果資料指標的定位不正確，就可能發生這種情況。</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordDeleted</p></td>
<td><p>如果資料指標未放置於交易中，如果另一個執行緒從這個會話下刪除記錄，就會發生這種情況。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>如果傳遞的是 <strong>Null</strong><em>precsize</em> ，則可以傳回。</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>備註

[JET_RECSIZE2](./jet-recsize2-structure.md)的 **cbOverhead** 欄位中累積的金鑰大小會受到 JET_bitRecordSizeInCopyBuffer 的影響。 如果指定了此位，則在 **cbOverhead** 欄位中累積的索引鍵大小會是完整的金鑰大小。 如果未使用此位，累積的金鑰大小將不會包含任何因金鑰首碼壓縮而儲存的大小。

#### <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>用戶端</strong></p></td>
<td><p>需要 Windows Vista。</p></td>
</tr>
<tr class="even">
<td><p><strong>伺服器</strong></p></td>
<td><p>需要 Windows Server 2008。</p></td>
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
[JET_RECSIZE](./jet-recsize-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)
