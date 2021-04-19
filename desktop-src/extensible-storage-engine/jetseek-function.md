---
description: 深入瞭解： JetSeek 函數
title: JetSeek 函式
TOCTitle: JetSeek Function
ms:assetid: d3d5bfae-dd27-47ab-96c4-6bc9a01a501b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294103(v=EXCHG.10)
ms:contentKeyID: 32765718
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSeek
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c386ae3af5353b95d9d1d3c67df4d680c52bff68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988420"
---
# <a name="jetseek-function"></a>JetSeek 函式


_**適用于：** Windows |Windows Server_

## <a name="jetseek-function"></a>JetSeek 函式

**JetSeek** 函式會有效率地將資料指標放在索引項目目，以符合該資料指標中的搜尋索引鍵所指定的搜尋條件，以及指定的不相等。 搜尋金鑰必須先前已使用 [JetMakeKey](./jetmakekey-function.md)來建立。

```cpp
    JET_ERR JET_API JetSeek(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*tableid*

要用於此呼叫的資料指標。

*grbit*

位群組，其中包含要用於此呼叫的選項。 *Grbit* 必須為非零值，而且必須包含下表所列的一或多個值。

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
<td><p>JET_bitCheckUniqueness</p></td>
<td><p>如果低廉價格判斷出只有一個符合搜尋索引鍵的索引項目，就會傳回特殊的錯誤碼（JET_wrnUniqueKey）。</p>
<p>除非也指定了 JET_bitSeekEQ，否則會忽略這個選項。</p>
<p>此選項僅適用于 Windows Server 2003 和更新版本。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSeekEQ</p></td>
<td><p>資料指標將定位於最接近索引開頭的索引項目目，此索引項目目完全符合搜尋索引鍵。 索引的開頭是移至該索引中的第一筆記錄時，所找到的索引項目。 索引的開頭與索引的下限不同，它可能會根據索引中索引鍵資料行的排序次序而變更。</p>
<p>將此選項與使用 <a href="gg269329(v=exchg.10).md">JetMakeKey</a> 所建立的搜尋索引鍵搭配使用萬用字元選項沒有意義。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSeekGE</p></td>
<td><p>資料指標將定位於最接近索引開頭的索引項目目，此索引項目目大於或等於符合搜尋條件的索引項目目。 索引的開頭是移至該索引中的第一筆記錄時，所找到的索引項目。 索引的開頭與索引的下限不同，它可能會根據索引中索引鍵資料行的排序次序而變更。</p>
<p>將此選項與使用 <a href="gg269329(v=exchg.10).md">JetMakeKey</a> 所建立的搜尋索引鍵搭配使用，並使用萬用字元選項來尋找最接近索引結尾的索引項目，並沒有任何意義。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSeekGT</p></td>
<td><p>資料指標將放置在索引項目目的開頭最接近索引的開頭，而該索引項目大於符合搜尋準則的索引項目目。 索引的開頭是移至該索引中的第一筆記錄時，所找到的索引項目。 索引的開頭與索引的下限不同，它可能會根據索引中索引鍵資料行的排序次序而變更。</p>
<p>搭配使用 <a href="gg269329(v=exchg.10).md">JetMakeKey</a> 所建立的搜尋索引鍵，並不適合用來尋找最接近索引開頭的索引項目的萬用字元選項，這是使用此選項的意義。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSeekLE</p></td>
<td><p>資料指標將定位於最接近索引結尾的索引項目目，這個專案小於或等於符合搜尋準則的索引項目目。 索引的結尾是移至該索引中的最後一筆記錄時，所找到的索引項目。 索引的結尾與索引的高端不同，它可能會根據索引中索引鍵資料行的排序次序而變更。</p>
<p>搭配使用 <a href="gg269329(v=exchg.10).md">JetMakeKey</a> 所建立的搜尋索引鍵，並不適合用來尋找最接近索引開頭的索引項目的萬用字元選項，這是使用此選項的意義。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitSeekLT</p></td>
<td><p>資料指標將放置在最接近索引結尾的索引項目目，此索引項目目小於符合搜尋條件的索引項目。 索引的結尾是移至該索引中的最後一筆記錄時，所找到的索引項目。 索引的結尾與索引的高端不同，它可能會根據索引中索引鍵資料行的排序次序而變更。</p>
<p>將此選項與使用 <a href="gg269329(v=exchg.10).md">JetMakeKey</a> 所建立的搜尋索引鍵搭配使用，並使用萬用字元選項來尋找最接近索引結尾的索引項目，並沒有任何意義。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitSetIndexRange</p></td>
<td><p>將會針對完全符合搜尋索引鍵的所有索引鍵，自動設定索引範圍。 產生的索引範圍等同于使用 JET_bitRangeInclusive 和 JET_bitRangeUpperLimit 選項呼叫 <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> 所建立的索引範圍。 如需詳細資訊，請參閱 <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a> 。</p>
<p>這是一種方便的方法，可讓您探索符合相同搜尋條件的所有索引項目。</p>
<p>除非也指定了 JET_bitSeekEQ，否則會忽略這個選項。</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>傳回值

此函數可讓您傳回此 API 中所定義的任何 [JET_ERRs](./jet-err.md) 。 如需有關 Jet 錯誤的詳細資訊，請參閱 [可擴充儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。

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
<td><p>作業已成功完成。</p>
<p>針對 <strong>JetSeek</strong>，這表示找到完全符合搜尋準則的索引項目。</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p>
<p>只有 Windows XP 和更新版本才會傳回此錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errKeyNotMade</p></td>
<td><p>沒有目前的資料指標搜尋索引鍵。 <strong>JetSeek</strong> 要求資料指標必須有有效的搜尋索引鍵，因為它會針對用來尋找索引項目的搜尋條件使用該索引鍵。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordNotFound</p></td>
<td><p>找不到符合搜尋準則的索引項目。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnSeekNotEqual</p></td>
<td><p>找到符合搜尋準則的索引項目。 但是，該索引項目不完全相符。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>相同的會話無法同時用於一個以上的執行緒。</p>
<p>只有 Windows XP 和更新版本才會傳回此錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在關閉。</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnUniqueKey</p></td>
<td><p>找不到完全符合搜尋準則的一個索引項目。 只有在指定 JET_bitSeekCheckUniqueness 時，才會傳回此錯誤，而且很便宜地判斷相符的索引項目目是完全符合搜尋準則的唯一索引專案。</p>
<p>只有 Windows Server 2003 和更新版本才會傳回此錯誤。</p></td>
</tr>
</tbody>
</table>


成功時，游標將定位於符合搜尋準則的索引項目。 如果已準備好要進行更新的記錄，則會取消該更新。 如果索引範圍有效，就會取消該索引範圍。 如果已針對資料指標建立搜尋索引鍵，則會刪除該搜尋索引鍵。 不會變更資料庫狀態。 當多個索引項目具有相同的值時，一律會選取最接近索引開頭的專案。

失敗時，除非傳回 JET_errRecordNotFound，否則資料指標的位置會保持不變。 在這種情況下，游標將放置於符合該資料指標中搜尋索引鍵所指定之搜尋準則的索引項目目，以及指定的不相等。 資料指標可以相對於該位置移動，但仍不在有效的索引項目上。 如果已準備好要進行更新的記錄，則會取消該更新。 如果索引範圍有效，就會取消該索引範圍。 如果已針對資料指標建立搜尋索引鍵，則會刪除該搜尋索引鍵。 不會變更資料庫狀態。

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
[JetSetIndexRange](./jetsetindexrange-function.md)  
[JetStopService](./jetstopservice-function.md)
