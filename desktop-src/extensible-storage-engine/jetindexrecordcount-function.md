---
description: 深入瞭解： JetIndexRecordCount 函數
title: JetIndexRecordCount 函式
TOCTitle: JetIndexRecordCount Function
ms:assetid: 62d39738-cd91-4cfb-9483-f4a2dd845d9a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269267(v=EXCHG.10)
ms:contentKeyID: 32765569
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIndexRecordCount
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3324ad2fe68d106c7f4d2dcdcd1c3dd6ddefd608
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510917"
---
# <a name="jetindexrecordcount-function"></a>JetIndexRecordCount 函式


_**適用于：** Windows |Windows Server_

## <a name="jetindexrecordcount-function"></a>JetIndexRecordCount 函式

**JetIndexRecordCount** 函式會計算目前索引中的專案數，從目前的位置向前算起。 目前的位置會包含在計數中。 如果目前索引超過多重值資料行，而且資料行的實例具有多個值，則計數可以大於資料表中的記錄總數。 如果資料表是空的，則會傳回計數的0。

```cpp
    JET_ERR JET_API JetIndexRecordCount(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         unsigned long* pcrec,
      __in          unsigned long crecMax
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*tableid*

要用於此呼叫的資料指標。

*pcrec*

要接收計數之不帶正負號的完整值指標。

*crecMax*

要計算的記錄數目上限。 *CrecMax* 值為0表示計數是無限制的。

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
<td><p>無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p>
<p><strong>WINDOWS XP：</strong>  這個傳回值是在 Windows XP 中引進的。</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>資料指標目前不在記錄上，且資料表不是空的。</p>
<p><strong>WINDOWS XP、Windows Server 2003、windows 2000 Server 及 windows 2000 Professional：</strong>  如果資料指標位於空的索引或索引範圍上， <strong>JetIndexRecordCount</strong> 會錯誤地傳回 JET_errNoCurrentRecord。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>作業無法完成，因為與會話相關聯的實例正在進行還原作業。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>相同的會話無法同時用於一個以上的執行緒。</p>
<p><strong>WINDOWS XP：</strong>  這個傳回值是在 Windows XP 中引進的。</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在關閉中。</p></td>
</tr>
</tbody>
</table>


如果此函式成功，則包含目前位置和最高 *crecMax* (索引項目的確切數目（如果不是 0) ）會以 *pcrec* 所指向的不帶正負號的長整數格式傳回。

如果此函式失敗，則不會對在 *precpos* 配置的記憶體進行任何變更。

#### <a name="remarks"></a>備註

如果資料表不是空的，則資料指標應放置於開始計數的記錄上。 計數將會包含此記錄，並在 *crecMax* 中向前算到指定的限制。 如果 *crecMax* 為0，則作業會繼續計算到索引結尾。

索引範圍可以用來為計數建立人工索引的結尾限制。 如此一來，就可以精確地計算索引的子範圍。 資料指標應該定位至範圍中的第一個資料列。 應該建立範圍索引鍵的結尾，然後 [JetSetIndexRange](./jetsetindexrange-function.md) 應該用來設定以上的範圍（包括或僅限）。 最後，應呼叫 **JetIndexRecordCount** 來精確計算範圍。

**JetIndexRecordCount** 會遵守交易語義，並傳回在其目前交易狀態下，此特定會話精確的計數。

**JetIndexRecordCount** 會存取索引分葉頁面，以便精確地計算專案。 因此，它可以執行大量 i/o，而且可能很慢。 *CrecMax* 限制應該用來防止過度負載。 如果範圍很大，則可能使用 [JetGetRecordPosition](./jetgetrecordposition-function.md)以近似值的方式計算範圍。

**WINDOWS XP、Windows Server 2003、windows 2000 Server 及 windows 2000 Professional：**  如果資料指標位於空的索引或索引範圍上， **JetIndexRecordCount** 會錯誤地傳回 JET_errNoCurrentRecord 而不是傳回零的記錄計數。 在此情況下，應用程式應該查看索引或索引範圍是否為空白。

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
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetRecordPosition](./jetgetrecordposition-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)  
[JetStopService](./jetstopservice-function.md)
