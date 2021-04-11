---
description: 深入瞭解： JetPrereadIndexRanges 函數
title: JetPrereadIndexRanges 函式
TOCTitle: JetPrereadIndexRanges Function
ms:assetid: ab49abcc-eaeb-438f-8e6d-b08bc94d7bc3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835045(v=EXCHG.10)
ms:contentKeyID: 49894667
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetPrereadIndexRanges
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7cfdd8d25f7008f5fa854cbee32b54fa01942ce2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112048"
---
# <a name="jetprereadindexranges-function"></a>JetPrereadIndexRanges 函式


_**適用于：** Windows |Windows Server_

**JetPrereadIndexRanges** 函式會 prereads 索引以改善效能。

**JetPrereadIndexRanges** 函式是在 Windows 8 作業系統中引進的。

``` c++
JET_ERR JetPrereadIndexRanges(
  __in          const JET_SESID sesid,
  __in          const JET_TABLEID tableid,
  __in_ecount(cIndexRanges)  const JET_INDEX_RANGE* const rgIndexRanges,
  __in          const unsigned long cIndexRanges,
  __out_opt     unsigned long* const pcRangesPreread,
  __in_ecount(ccolumnidPreread)  const JET_COLUMNID* const rgcolumnidPreread,
  __in          const unsigned long ccolumnidPreread,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a>參數

*sesid*

要用於 API 呼叫的資料庫會話內容。

*tableid*

要針對其發出 prereads 的資料表。

*rgIndexRanges*

要 preread 的索引鍵範圍。

*cIndexRanges*

要 preread 的索引鍵範圍數目，取決於 *rgIndexRanges* 中的元素數目。

*pcRangesPreread*

實際 preread 的索引鍵範圍數目。

*rgcolumnidPreread*

要 preread 之 long 值資料行的資料行識別碼清單。 依預設，只會 preread 頁面記錄。 如果需要 preread 非 page long 值資料行，則必須透過此參數傳遞其資料行識別碼。

*ccolumnidPreread*

要 preread 之 long 值資料行的資料行識別碼數目，取決於 *rgcolumnidPreread* 中的元素數目。

*grbit*

一組位，指定下表所列的零或多個 preread 方向值。

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
<td><p>轉寄</p></td>
<td><p>向前 Preread。</p></td>
</tr>
<tr class="even">
<td><p>向後</p></td>
<td><p>向後 Preread。</p></td>
</tr>
<tr class="odd">
<td><p>FirstPageOnly</p></td>
<td><p>只 Preread 任何長資料行的第一頁。</p></td>
</tr>
<tr class="even">
<td><p>NormalizedKey</p></td>
<td><p>提供正規化的索引鍵/書簽，而不是資料行值。</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>傳回值

此函數會傳回 [JET_ERR](./jet-err.md) 資料類型，其中包含下表所列的其中一個傳回碼。 如需可能的可延伸儲存引擎 (ESE) 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。

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
</tbody>
</table>


#### <a name="remarks"></a>備註

如果具有指定索引鍵範圍的記錄不在緩衝區快取中，您應該啟動非同步讀取，以將記錄帶入資料庫緩衝區快取。

#### <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>用戶端</strong></p></td>
<td><p>需要 Windows 8。</p></td>
</tr>
<tr class="even">
<td><p><strong>伺服器</strong></p></td>
<td><p>需要 Windows Server 2012。</p></td>
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
