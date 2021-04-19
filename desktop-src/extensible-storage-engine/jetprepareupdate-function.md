---
description: 深入瞭解： JetPrepareUpdate 函數
title: JetPrepareUpdate 函式
TOCTitle: JetPrepareUpdate Function
ms:assetid: 90cbaa83-47f2-4a65-b561-3bdecb7fd95a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269339(v=EXCHG.10)
ms:contentKeyID: 32765628
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetPrepareUpdate
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16362463194d945d7b451f784bc0942bda2d03e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997990"
---
# <a name="jetprepareupdate-function"></a>JetPrepareUpdate 函式


_**適用于：** Windows |Windows Server_

## <a name="jetprepareupdate-function"></a>JetPrepareUpdate 函式

**JetPrepareUpdate** 函式是執行更新的第一個作業，目的是要插入新的記錄，或以新的值取代現有的記錄。 更新的完成方式是呼叫 **JetPrepareUpdate**，然後呼叫 [JetSetColumn](./jetsetcolumn-function.md) 或 [JetSetColumns](./jetsetcolumns-function.md) 零次或多次，最後呼叫 [JetUpdate](./jetupdate-function.md) 來完成作業。 **JetPrepareUpdate** 和 [JetUpdate](./jetupdate-function.md) 會設定更新作業的界限，而且只有在索引中輸入記錄的最終更新狀態時很重要。 這會更有效率，但在資料必須透過超過 set 資料行作業的有效狀態必須符合的情況下，也是必要的。

有幾個不同的選項可用於插入或取代記錄，並且會在下面更詳細地說明。

```cpp
    JET_ERR JET_API JetPrepareUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          unsigned long prep
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*tableid*

要用於此呼叫的資料指標。

*準備*

可以用來準備更新的選項，包括下列各項。

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
<td><p>JET_prepCancel</p></td>
<td><p>此旗標會使 <strong>JetPrepareUpdate</strong> 取消此資料指標的更新。</p></td>
</tr>
<tr class="even">
<td><p>JET_prepInsert</p></td>
<td><p>此旗標會讓資料指標準備插入新的記錄。 所有資料都會初始化為記錄的預設狀態。 如果資料表具有自動遞增資料行，就會將新的值指派給此記錄，而不論更新最終成功、失敗或已取消。</p></td>
</tr>
<tr class="odd">
<td><p>JET_prepInsertCopy</p></td>
<td><p>此旗標會讓資料指標準備插入現有記錄的複本。 如果使用此選項，則必須要有目前的記錄。 新記錄的初始狀態會從目前記錄複製。 幾乎會複製儲存在登出的 Long 值。</p></td>
</tr>
<tr class="even">
<td><p>JET_prepInsertCopyDeleteOriginal</p></td>
<td><p>此旗標會讓資料指標準備插入相同的記錄，以及刪除或原始記錄。 當主要金鑰已變更時，就會使用它。</p></td>
</tr>
<tr class="odd">
<td><p>JET_prepReplace</p></td>
<td><p>此旗標會讓資料指標準備取代目前的記錄。 如果資料表有版本資料行，則 [版本] 欄會設定為其序列中的下一個值。 如果此更新未完成，則記錄中的版本值不會受到影響。 記錄上會執行更新鎖定，以防止其他會話在此會話完成之前更新此記錄。</p></td>
</tr>
<tr class="even">
<td><p>JET_prepReplaceNoLock</p></td>
<td><p>此旗標類似于 JET_prepReplace，但不會採取任何鎖定來防止其他會話更新此記錄。 相反地，此會話可能會在呼叫 <a href="gg269288(v=exchg.10).md">JetUpdate</a> 來完成更新時收到 JET_errWriteConflict。</p></td>
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
<td><p>JET_errAlreadyPrepared</p></td>
<td><p>已使用有效的準備旗標呼叫<strong>JetPrepareUpdate</strong> ，但未 JET_prepCancel，且資料指標已處於備妥狀態。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。 只有 Windows XP 和更新版本才會傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>指定的準備旗標不是有效的旗標。</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInTransaction</p></td>
<td><p>呼叫<strong>JetPrepareUpdate</strong>來取代具有 SLV 資料行的記錄。 SLV 資料行。 請注意，SLV 資料行是不適合一般使用的功能。 這項功能是用來支援 Microsoft Exchange 基礎結構，而且不適合在您的應用程式中使用。</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRollbackError</p></td>
<td><p>使用 JET_prepCancel 呼叫<strong>JetPrepareUpdate</strong> ，但無法復原 JET_coltypLongBinary 類型 JET_coltypLongText 和/或資料行的資料行所做的所有變更。</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>此旗標不能同時與多個執行緒中的相同會話一起使用。 只有 Windows XP 和更新版本才會傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在關閉。</p></td>
</tr>
<tr class="even">
<td><p>JET_errUpdateNotPrepared</p></td>
<td><p>使用 JET_prepCancel 呼叫<strong>JetPrepareUpdate</strong> ，但資料指標不是處於已備妥的狀態。</p></td>
</tr>
</tbody>
</table>


成功時，資料指標會針對所需的更新目的變更為備妥狀態，或者，如果是 JET_prepCancel，則會將資料指標還原為未備妥狀態，並捨棄任何變更。

失敗時，資料指標狀態會保持不變。 如果 JET_errRollbackError 失敗，則資料指標狀態會變更為未就緒狀態，但並非所有變更都已還原。

#### <a name="remarks"></a>備註

當記錄共用 JET_coltypLongText 和/或 JET_coltypLongBinary 類型的資料時，插入記錄的副本是很重要的優化。 這項資料會在很大的情況下儲存在記錄中，而且可能會有多筆記錄共用相同的資料實體標記法。 在此情況下，資料可以從任一記錄進行更新，但這麼做會導致資料突然增加，讓每一筆記錄都有自己的複本。 您無法藉由另一筆記錄的修改來變更某筆記錄中的資料。 此外，也無法透過更新另一筆記錄來封鎖某一筆記錄的更新。 這是 ESE 的集中功能，也稱為記錄層級鎖定。

失敗的[JetUpdate](./jetupdate-function.md)作業會將資料指標保持在「更新準備」狀態。 這是為了允許更正某些錯誤，例如錯誤的資料行值，而不需要重新建立更新狀態。 這表示在所有情況下，如果資料指標放棄更新，它就必須使用 JET_prepCancel 明確地呼叫 **JetPrepareUpdate** 。

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
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)  
[JetUpdate](./jetupdate-function.md)
