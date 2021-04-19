---
description: 深入瞭解： JetGetCurrentIndex 函數
title: JetGetCurrentIndex 函式
TOCTitle: JetGetCurrentIndex Function
ms:assetid: 9db3b875-0b95-4027-9742-c36d2d7e64cf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294041(v=EXCHG.10)
ms:contentKeyID: 32765642
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetCurrentIndexW
- JetGetCurrentIndex
- JetGetCurrentIndexA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d3337ddaefbea803a137ad8366d2e3df665bacd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001400"
---
# <a name="jetgetcurrentindex-function"></a>JetGetCurrentIndex 函式


_**適用于：** Windows |Windows Server_

## <a name="jetgetcurrentindex-function"></a>JetGetCurrentIndex 函式

**JetGetCurrentIndex** 函式會判斷指定之資料指標目前索引的名稱。 此名稱也用來在稍後使用 [JetSetCurrentIndex](./jetsetcurrentindex-function.md)重新選取該索引做為目前的索引。 它也可以用來使用 [JetGetTableIndexInfo](./jetgettableindexinfo-function.md)探索該索引的屬性。

```cpp
    JET_ERR JET_API JetGetCurrentIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_PSTR szIndexName,
      __in          unsigned long cchIndexName
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*tableid*

要用於此呼叫的資料指標。

*szIndexName*

輸出緩衝區，可接收資料指標目前索引的名稱。

*cchIndexName*

輸出緩衝區的大小上限（以字元為單位）。

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
<td><p>作業已順利完成，但輸出緩衝區太小，無法接收整個索引名稱。</p>
<p>輸出緩衝區已填滿適當的索引名稱。 如果輸出緩衝區的長度至少要有一個字元，則該輸出緩衝區中的字串會以 null 結束。</p>
<p><strong>注意  </strong>如果 cchIndexName 為零，則不會傳回此錯誤。 如需詳細資訊，請參閱「備註」一節。</p></td>
</tr>
</tbody>
</table>


成功時，會在輸出緩衝區中傳回指定資料指標目前索引的名稱。 如果傳回 JET_wrnBufferTruncated，輸出緩衝區將會包含所提供空間中的最多索引名稱。 如果輸出緩衝區的長度至少要有一個字元，則在該緩衝區中傳回的字串將會以 null 結束。 不會變更資料庫狀態。

失敗時，輸出緩衝區的狀態將會是未定義的。 不會變更資料庫狀態。

#### <a name="remarks"></a>備註

如果沒有目前的資料指標索引，則會傳回空字串。 當資料指標位於資料表的叢集索引，但未定義任何主要索引時，就會發生這種情況。 此索引稱為資料表的連續索引，且沒有任何定義。 在任何情況下，使用 [JetSetCurrentIndex](./jetsetcurrentindex-function.md) 將目前的索引設定為空字串，將會選取叢集索引，不論主要索引定義是否存在。

在此函式中，有一個重要的 bug 存在於所有版本中。 如果輸出緩衝區太小而無法接收整個索引名稱，而且輸出緩衝區的長度至少有一個字元，則不會傳回 JET_wrnBufferTruncated。 將會改為傳回 JET_errSuccess。 若要避免這個問題，輸出緩衝區的長度應該一律至少 JET_cbNameMost + 1 (65) 個字元。

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>實作為 <strong>JetGetCurrentIndexW</strong> (Unicode) 和 <strong>JetGetCurrentIndexA</strong> (ANSI) 。</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetSetCurrentIndex](./jetsetcurrentindex-function.md)
