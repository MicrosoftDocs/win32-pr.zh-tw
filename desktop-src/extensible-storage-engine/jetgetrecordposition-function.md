---
description: 深入瞭解： JetGetRecordPosition 函數
title: JetGetRecordPosition 函式
TOCTitle: JetGetRecordPosition Function
ms:assetid: 811d9e68-0594-4f70-b854-c3ec966b2705
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269316(v=EXCHG.10)
ms:contentKeyID: 32765606
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordPosition
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d4301b25ca111228b742ce7b35ab9ae28e170526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026844"
---
# <a name="jetgetrecordposition-function"></a>JetGetRecordPosition 函式


_**適用于：** Windows |Windows Server_

## <a name="jetgetrecordposition-function"></a>JetGetRecordPosition 函式

**JetGetRecordPosition** 函數會以 [JET_RECPOS](./jet-recpos-structure.md)結構的形式，傳回目前索引中目前記錄的小數位置。 此結構描述的是在目前記錄之前的索引項目目大約數量的小數位置，以及索引中專案的大約總數目。

```cpp
    JET_ERR JET_API JetGetRecordPosition(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECPOS* precpos,
      __in          unsigned long cbRecpos
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*tableid*

要用於此呼叫的資料指標。

*precpos*

用來取得目前索引中目前記錄位置的分數描述。

*cbRecpos*

配置於 *precpos* 的記憶體大小。

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
<td><p>JET_errNotInitialized</p></td>
<td><p>無法完成作業，因為與該會話相關聯的實例尚未初始化。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>無法完成作業，因為與該會話相關聯之實例上的所有活動都已停止，因此呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>因為與會話相關聯的實例發生嚴重錯誤，所以無法完成此操作。 必須撤銷所有資料的存取權，才能保護該資料的完整性。</p>
<p><strong>Windows 2000：</strong>  Windows 2000 作業系統將不會傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p><em>Precpos</em>配置的記憶體大小不是足夠的大小。</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>資料指標目前不在記錄中，而且無法傳回位置。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>相同的會話無法同時用於一個以上的執行緒。</p>
<p><strong>Windows 2000：</strong>  Windows 2000 作業系統將不會傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在關閉中。</p></td>
</tr>
</tbody>
</table>


成功時，會在 precpos-centriesLT 中傳回索引中目前記錄之前的大約索引項目目數 \> 。 precpos-centriesInRange 中傳回 1 \> 。 索引中的大約專案數會以 precpos- \> centriesTotal 傳回。

失敗時，不會對在 *precpos* 配置的記憶體進行任何變更。

#### <a name="remarks"></a>備註

當資料表上持續發生更新時，此作業會傳回不同的資料。 值的變更不一定會根據更新的知識來符合預期，因為這些值是根據索引的實體屬性來近似值。 交易式隔離不會套用至 **JetGetRecordPosition** 的位置，因為這些值相依于非交易隔離之索引的實體屬性。

[JET_RECPOS](./jet-recpos-structure.md) 不能用來描述資料表內的記錄，或將記錄重新放置到接近現有記錄的位置。 相反地，您應該先取出現有記錄的書簽，然後再用它來重新置放相同的記錄。

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

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_RECPOS](./jet-recpos-structure.md)  
[JET_SETINFO](./jet-setinfo-structure.md)  
[JetGotoPosition](./jetgotoposition-function.md)  
[JetStopService](./jetstopservice-function.md)
