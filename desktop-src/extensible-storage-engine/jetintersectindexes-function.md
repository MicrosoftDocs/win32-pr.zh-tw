---
description: 深入瞭解： JetIntersectIndexes 函數
title: JetIntersectIndexes 函式
TOCTitle: JetIntersectIndexes Function
ms:assetid: 6e111d10-6882-46ac-a70b-7896662d3b5d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269289(v=EXCHG.10)
ms:contentKeyID: 32765581
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIntersectIndexes
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4bdffa6f21a65ae7f438f87ea0d8d2adf4aed6a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970131"
---
# <a name="jetintersectindexes-function"></a>JetIntersectIndexes 函式


_**適用于：** Windows |Windows Server_

## <a name="jetintersectindexes-function"></a>JetIntersectIndexes 函式

**JetIntersectIndexes** 函式會計算相同資料表上不同次要索引的多個索引項目目集合之間的交集。 這項作業適用于在資料表中尋找符合可使用索引範圍表示之兩個或多個準則的一組記錄。

```cpp
    JET_ERR JET_API JetIntersectIndexes(
      __in          JET_SESID sesid,
      __in          JET_INDEXRANGE* rgindexrange,
      __in          unsigned long cindexrange,
      __in_out      JET_RECORDLIST* precordlist,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*rgindexrange*

[JET_IndexRange](./jet-indexrange-structure.md)結構陣列的指標。 每個結構都包含已設定的 [JET_TABLEID](./jet-tableid.md) ，以保存其中一個要交集的索引範圍。 如需詳細資訊，請參閱 [JET_IndexRange](./jet-indexrange-structure.md)。

*cindexrange*

包含在 *rgindexrange* 參數中的陣列中 [JET_IndexRange](./jet-indexrange-structure.md)結構的數目。

*precordlist*

[JET_RECORDLIST](./jet-recordlist-structure.md)結構的指標。 此結構將會填入足夠的資訊，以使用 **JetIntersectIndexes** 的結果來進行臨時表的往返。

接收 [JET_RECORDLIST](./jet-recordlist-structure.md) 結構的輸出緩衝區。 結構包含交集之結果集的描述。

*grbit*

保留供未來使用。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需 ESE 錯誤的詳細資訊，請參閱 [可擴充儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。

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
<td><p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p>
<p><strong>WINDOWS XP：</strong>  這個傳回值是在 Windows XP 中引進的。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>其中一個要求的選項無效、使用不正確或未執行。</p>
<p><strong>JetIntersectIndexes</strong>會在下列情況傳回此錯誤：</p>
<p>由<em>rgindexrange</em>陣列中的任何元素所指向<a href="gg269335(v=exchg.10).md">JET_IndexRange</a>結構中所包含的<em>grbit</em> ，不等於 JET_bitRecordInIndex。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>提供的其中一個參數包含未預期的值，或與另一個參數的值結合時不一致的值。</p>
<p><strong>JetIntersectIndexes</strong>會傳回此錯誤，原因如下：</p>
<ul>
<li><p><em>Precordlist</em>參數為 Null。</p></li>
<li><p>在<em>precordlist</em>參數中指定之<a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a>結構的<strong>cbStruct</strong>成員不等於<a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a>結構的大小。</p></li>
<li><p><em>Cindexrange</em>參數為零。</p></li>
<li><p><em>Cindexrange</em>參數大於64。</p></li>
<li><p><em>Rgindexrange</em>參數所指定之陣列中任何元素的<strong>cbStruct</strong>成員，都不等於<a href="gg269335(v=exchg.10).md">JET_IndexRange</a>結構的大小。</p></li>
<li><p><em>Rgindexrange</em>陣列中的元素包含來自不同資料表的<a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s。</p></li>
<li><p><em>Rgindexrange</em>陣列中的元素包含不在次要索引上的<a href="gg269182(v=exchg.10).md">JET_TABLEID</a> 。</p></li>
<li><p><em>Rgindexrange</em>陣列中的一或多個元素包含位於相同次要索引的<a href="gg269182(v=exchg.10).md">JET_TABLEID</a>s。</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSesid</p></td>
<td><p>會話控制碼無效或參考已關閉的會話。</p>
<p>在所有情況下，都不會傳回此錯誤。 控制碼只會根據最大努力進行驗證。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfCursors</p></td>
<td><p>因為引擎無法配置開啟新資料指標所需的資源，所以操作失敗。 您可以使用<em>paramid</em>參數中指定的<em>JET_paramMaxCursors</em>呼叫<a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>來設定資料指標資源。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory</p></td>
<td><p>作業失敗，因為無法配置足夠的記憶體來完成。</p>
<p>如果主機進程的位址空間變得太分散， <strong>JetIntersectIndexes</strong>可能會傳回 JET_errOutOfMemory。 無論要儲存的資料量為何，臨時表管理員一律會為每個建立的臨時表配置1MB 的位址空間區塊。 <strong>JetIntersectIndexes</strong>會為<em>rgindexrange</em>參數中指定的每個<a href="gg269335(v=exchg.10).md">JET_IndexRange</a>建立一個臨時表，並為<a href="gg269287(v=exchg.10).md">JET_RECORDLIST</a>的輸出建立一個臨時表。</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>同時從一個以上的執行緒使用相同的會話是不合法的。</p>
<p><strong>WINDOWS XP：</strong>  這個傳回值是在 Windows XP 中引進的。</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在關閉。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyOpenIndexes</p></td>
<td><p>因為引擎無法配置快取資料表索引所需的資源，所以操作失敗。 您可以使用<a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>搭配<em>paramid</em>參數中指定的<em>JET_paramMaxOpenTables</em> ，來設定可以快取其架構的索引數目。</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyOpenTables</p></td>
<td><p>作業失敗，因為引擎無法配置快取資料表架構所需的資源。 您可以使用<a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>搭配<em>paramid</em>參數中指定的<em>JET_paramMaxOpenTables</em> ，來設定可以快取其架構的資料表數目。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManySorts</p></td>
<td><p>因為引擎無法配置建立臨時表所需的資源，所以操作失敗。 臨時表資源是使用 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 與 <em>paramid</em> 參數中指定的 JET_paramMaxTemporaryTables 來設定。</p></td>
</tr>
</tbody>
</table>


成功時，會傳回新的臨時表，其中包含符合每個輸入索引範圍描述所代表準則的記錄的書簽。

失敗時，將不會建立包含結果的臨時表。 暫存資料庫的狀態可能會變更。 資料庫引擎所使用之任何一般資料庫的狀態將保持不變。 提供給此函式之 [JET_TABLEID](./jet-tableid.md)的目前位置可能會變更。

#### <a name="remarks"></a>備註

**JetIntersectIndexes** 可以用來以多個準則有效率地篩選資料表中的記錄，如果這些準則是以該資料表的次要索引來表示。 例如，假設您有一個非常大的資料表包含人員。 資料表可以有資料行做為其使用者識別碼、名字、姓氏等等。 假設每個資料行都是分開編制索引，而且資料表的主要索引是超過使用者識別碼。如果您想要尋找名字開頭為且其姓氏開頭為 G 的每個人，請執行下列步驟：

1.  開啟資料表上的新資料指標，並將該資料指標設定為使用「名字」資料行的索引。 然後為其 "first name" 以 ' A ' 開頭的所有人設定索引範圍，然後建立包含此資料指標的 [JET_IndexRange](./jet-indexrange-structure.md) 結構。

2.  針對「姓氏」以 ' G ' 開頭的所有使用者，在「姓氏」索引上重複步驟1。

3.  將這些準則傳遞給 **JetIntersectIndexes** ，以將結果計算到臨時表中。

4.  遍歷臨時表，並取得以書簽傳遞準則的每個記錄。

包含結果集的臨時表是一個簡單的資料表，其中包含每筆記錄的書簽，而這些記錄會通過所有用來計算交集的條件。 結果集的排序次序與主要索引相同，而且不包含重複的專案。 應用程式可以藉由列舉臨時表中的資料列、使用 [JetRetrieveColumn](./jetretrievecolumn-function.md)來取得每個結果的書簽，然後流覽資料庫中的記錄，藉由在位於主要索引的資料指標上使用該書簽來呼叫 [JetGotoBookmark](./jetgotobookmark-function.md) ，以列舉交集的結果。

**JetIntersectIndexes** 所傳回的臨時表只能以正向方向掃描。 當掃描完成時，也應該透過 [JetCloseTable](./jetclosetable-function.md) 來關閉它。 如需臨時表和其運作方式的詳細資訊，請參閱 [JetOpenTemporaryTable](./jetopentemporarytable-function.md)。

**JetIntersectIndexes** 通常是根據多個索引準則來篩選記錄的有效率且方便的方式。 不過，您應該遵循一些重要的秘訣，以充分發揮這項功能的實用性。 如果您知道其中一個條件的限制是，所產生的索引範圍有極少的記錄，則只需要在應用層級上流覽索引範圍並篩選記錄，可能會比較好。 此外，如果您知道您的準則比交集的其他準則還低，那麼您可能會考慮從交集中卸載那些限制較少的準則。 最後，如果您知道其中一個準則不會有任何限制，使產生的索引範圍幾乎與主要索引一樣大，則不太可能與該索引範圍有交集的優點 (將) 結果集的大小減少。 在所有情況下，您應該以最少的輸入索引項目目來選取準則，並在輸出上產生最特定的書簽集合，以取得最大效能。

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
[JET_IndexRange](./jet-indexrange-structure.md)  
[JET_RECORDLIST](./jet-recordlist-structure.md)  
[JetGotoBookmark](./jetgotobookmark-function.md)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
