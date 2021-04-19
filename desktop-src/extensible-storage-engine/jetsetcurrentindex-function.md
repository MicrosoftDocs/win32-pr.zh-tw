---
description: 深入瞭解： JetSetCurrentIndex 函數
title: JetSetCurrentIndex 函式
TOCTitle: JetSetCurrentIndex Function
ms:assetid: a2a15eab-b8bf-4a67-a63a-830ed1fdb3d9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294046(v=EXCHG.10)
ms:contentKeyID: 32765645
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex
- JetSetCurrentIndexA
- JetSetCurrentIndexW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7698a12f470fadd5c43dc2afe23f95f8e51bdf66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971184"
---
# <a name="jetsetcurrentindex-function"></a>JetSetCurrentIndex 函式


_**適用于：** Windows |Windows Server_

## <a name="jetsetcurrentindex-function"></a>JetSetCurrentIndex 函式

**JetSetCurrentIndex** 函數可以用來設定資料指標目前的索引。 資料指標的目前索引會定義資料表中的哪些記錄可以顯示在該資料指標，以及選取一組要用來公開這些記錄的索引項目目順序。

```cpp
    JET_ERR JET_API JetSetCurrentIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      const tchar* szIndexName
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*tableid*

要用於此呼叫的資料指標。

*szIndexName*

要為數據指標選取的索引名稱。

如果此參數為 Null 或空字串，則會選取叢集索引。 如果定義了資料表的主要索引，則會選取該索引，因為它與叢集索引相同。 如果未定義資料表的主要索引，則會選取連續索引。 順序索引沒有索引定義。 如需詳細資訊，請參閱 [JetCreateIndex](./jetcreateindex-function.md) 。

如果 *pindexid* 不是 Null，則會忽略索引名稱，並且會依索引識別碼來選取索引。

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
<td><p>JET_errBadItagSequence</p></td>
<td><p>正在使用 JET_bitNoMove 選項來選取次要索引，且新索引定義中的第一個多重值索引鍵資料行沒有對應至指定序號的值。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidIndexId</p></td>
<td><p>索引識別碼的內容無效或已過期，需要重新整理。 在下列情況下， <strong>JetSetCurrentIndex</strong> 可能會發生：</p>
<ul>
<li><p>pindexid- &gt; cbStruct 不是 (Windows Server 2003 和更新版本) 的預期大小。</p></li>
<li><p>引擎已在提取索引識別碼之後關閉。</p></li>
<li><p>所有參考資料表的資料指標（包含對應至索引識別碼的索引）已關閉，且引擎已從架構快取中收回該索引的定義。</p></li>
<li><p>索引識別碼正在搭配在錯誤資料表上開啟的資料指標使用。</p></li>
<li><p>索引已卸載或尚未顯示在會話中。</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p>
<p>只有 Windows XP 和更新版本才會傳回此錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>其中一個指定的物件名稱無效。 所有物件名稱都必須符合同一組規則。 這些規則如下：</p>
<ul>
<li><p>物件名稱必須由 ASCII 字元組成。</p></li>
<li><p>物件名稱的長度必須至少有一個字元。</p></li>
<li><p>物件名稱的長度不得超過 JET_cbNameMost (64) 個字元。</p></li>
<li><p>物件名稱不能以空格開頭。</p></li>
<li><p>物件名稱不能包含 ASCII 控制字元 (0x00 到 0x1F) 。</p></li>
<li><p>物件名稱不能包含驚嘆號 (！ ) 、句號 (. ) 、左括弧 ( [) 或右括弧 (] ) 字元。</p></li>
<li><p>一旦經過驗證之後，就只會將字串的部分寫入第一個空格 (如果有任何) 將用於物件名稱。 這實際上是指物件名稱不能包含空格。</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。 當<em>pindexid</em>不是 Null，且 pindexid cbStruct 的大小不是 (Windows XP 和舊版) 的預期大小<strong>時，就</strong>可能會發生這種情況 &gt; 。</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>正在使用 JET_bitNoMove 選項來選取次要索引，而新的索引中沒有索引項目對應至在舊索引上目前的資料指標位置與索引項目目相關聯的記錄。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfCursors</p></td>
<td><p>引擎已用盡用來開啟資料指標的資源集區。 可以在任何時間開啟的資料指標數目上限是使用 <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>來控制。 如需詳細資訊，請參閱 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 。 當選取次要索引，且引擎無法開啟內部資料指標來使用該索引時， <strong>JetSetCurrentIndex</strong> 就會發生這種情況。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>相同的會話無法同時用於一個以上的執行緒。</p>
<p>只有 Windows XP 和更新版本才會傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在關閉。</p></td>
</tr>
</tbody>
</table>


成功時，會將資料指標的目前索引設定為要求的索引。 根據所要求索引的索引定義，現在可以使用 [JetSeek](./jetseek-function.md) 來搜尋索引項目。 您也可以使用 [JetMove](./jetmove-function.md) ，以該索引定義所指定的順序來列舉索引項目。 資料指標的目前位置是設定為索引上的第一個索引項目目 (JET_bitMoveFirst) 或與舊索引 (JET_bitNoMove) 上目前的資料指標位置相關的特定索引項目。 不會變更資料庫狀態。

失敗時，目前的索引和目前的資料指標位置處於未定義狀態。 不會變更資料庫狀態。

#### <a name="remarks"></a>備註

如果索引識別碼提示已過時，則 API 只會失敗。 在此情況下，不會回復到索引的文字名稱。 此回復必須由 API 的呼叫端手動完成。

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
<td><p>實作為 <strong>JetSetCurrentIndexW</strong> (Unicode) 和 <strong>JetSetCurrentIndexA</strong> (ANSI) 。</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXID](./jet-indexid-structure.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetGetCurrentIndex](./jetgetcurrentindex-function.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetMove](./jetmove-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetCurrentIndex]()  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)
