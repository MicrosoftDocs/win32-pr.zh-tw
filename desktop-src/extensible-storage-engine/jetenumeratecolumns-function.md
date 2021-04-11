---
description: 深入瞭解： JetEnumerateColumns 函數
title: JetEnumerateColumns 函式
TOCTitle: JetEnumerateColumns Function
ms:assetid: 8413d056-cdb1-420e-9dd3-7280ad510165
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269321(v=EXCHG.10)
ms:contentKeyID: 32765611
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEnumerateColumns
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b913fb970232ca6f0fc21eb846df85e1db684f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193797"
---
# <a name="jetenumeratecolumns-function"></a>JetEnumerateColumns 函式


_**適用于：** Windows |Windows Server_

## <a name="jetenumeratecolumns-function"></a>JetEnumerateColumns 函式

**JetEnumerateColumns** 函式會從資料指標的目前記錄或該資料指標的複製緩衝區，有效率地取出一組資料行和其值。 您可以使用資料行識別碼、 *itagSequence* 數位和其他特性的清單來限制抓取的資料行和值。 此資料行抓取 API 是唯一的，因為它會將資訊傳回給動態配置的記憶體，而這些記憶體是使用使用者提供的 [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) 相容回呼所取得。 這項新的彈性可讓您有效率地抓取具有特定特性 (的資料行資料，例如呼叫端未知) 大小和多重性。 如此一來，就不需要使用 [JetRetrieveColumn](./jetretrievecolumn-function.md) 的探索模式來判斷這些特性，以便設定 [JetRetrieveColumn](./jetretrievecolumn-function.md) 的最後一個呼叫，以成功取得所需的資料。

**Windows xp： JetEnumerateColumns** 是在 windows xp 中引進的。

```cpp
    JET_ERR JET_API JetEnumerateColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          unsigned long cEnumColumnId,
      __in_opt      JET_ENUMCOLUMNID* rgEnumColumnId,
      __out         unsigned long* pcEnumColumn,
      __out         JET_ENUMCOLUMN** prgEnumColumn,
      __in          JET_PFNREALLOC pfnRealloc,
      __in          void* pvReallocContext,
      __in          unsigned long cbDataMost,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*tableid*

要用於此呼叫的資料指標。

*cEnumColumnId*

資料行識別碼的陣列，每個都有一個選擇性的 *itagSequence* 數位陣列來列舉。

如果 *cEnumColumnId* 為 0 (零) 則會忽略 *rgEnumColumnId* 並列舉所有資料行值，並將其傳回給呼叫端。 如果資料行識別碼陣列的元素參考到 0 (零的資料行識別碼) 則會略過該資料行的列舉，並且會產生輸出中的對應位置，並將資料行狀態設為 JET_wrnColumnSkipped。

如果 *ctagSequence* 為 0 (零) 用於資料行識別碼陣列的指定元素，則會忽略 *rgtagSequence* ，並且會列舉該資料行識別碼的所有資料行值，並將其傳回給呼叫端。 如果 *itagSequence* 數位陣列的元素參考 *itagSequence* 數位 0 () 零，則會略過該 *itagSequence* 數位的列舉，並且會產生輸出中的對應位置，並將資料行值狀態設為 JET_wrnColumnSkipped。

*rgEnumColumnId*

請參閱 *cEnumColumnId*。

*pcEnumColumn*

在透過提供的 *itagSequence* 相容回呼所配置的記憶體中，傳回資料行的列舉陣列和其值。

如果在輸入上要求資料行識別碼的陣列，則輸出陣列的順序和大小會反映輸入陣列的順序和大小。 同樣地，如果在輸入時要求特定資料行識別碼的 *itagSequence* 數位陣列，則該資料行之資料行值的輸出陣列順序和大小將會反映輸入陣列的順序和大小。

輸出參數會設定為 0 (零) ，而且除了 JET_errBadColumnId 和 JET_errColumnNotFound 以外的任何錯誤都是 **Null** 。 傳回這些錯誤時，除了受影響的資料行識別碼之外，輸出資料是有效且完整的。 每個受影響資料行識別碼的狀態碼會設定為其中一個錯誤，因此呼叫者可以判斷哪些資料行識別碼不正確，並可能採取矯正措施。

*prgEnumColumn*

請參閱 *pcEnumColumn*。

*pfnRealloc*

識別與 [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) 相容的回呼，以及選用的內容指標，用來為數據行的輸出陣列和其值配置記憶體。

*pvReallocCoNtext*

請參閱 *pfnRealloc*。

*cbDataMost*

設定要從長文字或長二進位資料行傳回的資料量上限。

您可以使用這個參數來防止列舉非常大的資料行值。 一般來說，這類列舉可能會使 API 呼叫失敗，並 JET_errOutOfMemory。 如果以這種方式截斷大型資料行值，則資料行值的狀態將會是 JET_wrnColumnTruncated。

*grbit*

指定零或多個下列選項的位群組。

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
<td><p>JET_bitEnumerateCompressOutput</p></td>
<td><p>列舉資料行值時，我們將會以壓縮格式傳回所有資料行，而這些資料行只會傳回一個非 Null 資料行值。 這類資料行的狀態將會設定為 JET_wrnColumnSingleValue，且資料行值和包含資料行值的記憶體大小將直接在 <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> 結構中傳回。 不保證會以這種方式壓縮所有合格的資料行。 如需詳細資訊，請參閱 <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> 。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitEnumerateCopy</p></td>
<td><p>此選項表示應該列舉記錄的已修改資料行值，而不是原始資料行值。 如果資料行值尚未修改，則會列舉原始資料行值。 如此一來，插入或更新記錄時，可能會列舉尚未插入或更新的資料行值。</p>
<p>與 <a href="gg269198(v=exchg.10).md">JetRetrieveColumn</a> 或 <a href="gg294135(v=exchg.10).md">JetRetrieveColumns</a>搭配使用時，此選項等同于 JET_bitRetrieveCopy。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitEnumerateIgnoreDefault</p></td>
<td><p>如果指定的資料行不存在於記錄中，則不會傳回任何資料行值。 一般來說，在此案例中會傳回資料行的預設值（如果有的話）。 如果資料行設定為與預設值不同的值，則會傳回不同的值 (也就是說，如果具有預設值的資料行明確設定為 <strong>null</strong> ，則會傳回 <strong>null</strong> 做為該資料行的值) 。 請注意，即使已要求此選項，仍然可以看到剛好等於預設值的資料行值。 移除符合其預設值的資料行值不會進行任何工作。</p>
<p>請務必注意，當使用 JET_bitEnumeratePresenceOnly 或 JET_bitEnumerateTaggedOnly 時，此選項會影響 <strong>JetEnumerateColumns</strong> 的輸出。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitEnumerateIgnoreUserDefinedDefault</p></td>
<td><p>如果指定的資料行不存在於記錄中，而且它具有使用者定義的預設值，則不會傳回任何資料行值。 此選項可防止在列舉該資料行的值時，計算資料行之使用者定義預設值的回呼。</p>
<p><strong>Windows Server 2003 及更早版本：  </strong>若為 Windows Server 2003 及更早版本，此作業將會失敗，並 JET_errCallbackFailed。</p>
<p><strong>Windows Server 2003 SP1：  </strong>此可能值僅適用于 Windows Server 2003 SP1 和更新版本的作業系統。 如果指定了此可能的值，且資料表包含具有使用者定義之預設值的資料行，則作業會失敗並出現 JET_errCallbackFailed。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitEnumeratePresenceOnly</p></td>
<td><p>如果要求的資料行或資料行值有非 Null 的值，則不會傳回相關聯的資料。 相反地，該資料行或資料行值的關聯狀態將會設定為 JET_wrnColumnPresent。 如果資料行或資料行值為 <strong>Null</strong> ，則會如往常般傳回 JET_wrnColumnNull。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitEnumerateTaggedOnly</p></td>
<td><p>列舉記錄中的所有資料行值時 (例如，當 <em>cEnumColumnId</em> 為零) 時，只會傳回已標記的資料行值。 列舉資料行識別碼的特定陣列時，不允許使用這個選項。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitEnumerateInRecordOnly</p></td>
<td><p><strong>Windows 7：  </strong>JET_bitEnumerateInRecordOnly 是在 Windows 7 中引進的。</p></td>
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
<td><p>JET_errBadColumnId</p></td>
<td><p>提供的資料行識別碼超出資料行識別碼的合法限制。 如果要求了特定的資料行識別碼、其中一個資料行識別碼無效，且第一個不正確資料行識別碼因為其資料行狀態碼的錯誤而失敗，則 <strong>JetEnumerateColumns</strong> 會傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>給定資料行識別碼所描述的資料行不存在於資料表中。 如果要求了特定的資料行識別碼、其中一個資料行識別碼無效，且第一個不正確資料行識別碼因為其資料行狀態碼的錯誤而失敗，則 <strong>JetEnumerateColumns</strong> 會傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p>
<p><strong>WINDOWS XP：  </strong>只有 Windows XP 和更新版本才會傳回此錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>其中一個要求的選項無效或未執行。 <strong>JetEnumerateColumns</strong>會在下列情況傳回此錯誤：</p>
<ul>
<li><p>已指定 JET_bitEnumerateLocal。</p></li>
<li><p>指定了不合法的 <em>grbit</em> 。</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。 <strong>JetEnumerateColumns</strong>會在下列情況傳回此錯誤：</p>
<ul>
<li><p><em>pcEnumColumn</em> 為 <strong>Null</strong>。</p></li>
<li><p><em>prgEnumColumn</em> 為 <strong>Null</strong>。</p></li>
<li><p><em>pfnRealloc</em> 為 <strong>Null</strong>。</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>資料指標未放置在記錄上。 此情況具有許多不同的原因。 例如，如果資料指標目前位於目前索引的最後一筆記錄之後，就會發生這種情況。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordDeleted</p></td>
<td><p>游標位於已刪除的記錄上。 此情況具有許多不同的原因。 最常見的原因是會話不在交易中、資料指標位於記錄上、刪除記錄，然後資料指標嘗試參考該記錄。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>相同的會話無法同時用於一個以上的執行緒。</p>
<p><strong>WINDOWS XP：  </strong>只有 Windows XP 和更新版本才會傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>無法完成作業，因為與會話相關聯的實例正在關閉。</p></td>
</tr>
</tbody>
</table>


成功時，會在輸出緩衝區中傳回所要求的資料。 呼叫端必須負責釋放由此回呼配置並在輸出緩衝區中傳回的任何記憶體。 您應該透過提供的 [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) 相容回呼來釋放該記憶體。 不會變更資料庫狀態。

失敗時，將不會傳回任何要求的資料。 在呼叫期間配置的任何記憶體都會使用提供的 [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) 相容回呼自動釋放。 不會變更資料庫狀態。

#### <a name="remarks"></a>備註

如果您要列舉記錄中的所有資料行值，但未指定 JET_bitEnumerateIgnoreDefaults，則您無法假設您永遠不會看到狀態碼為 JET_wrnColumnNull 的資料行或資料行值。 如果資料行有預設值，而且明確設定為 **Null** ，或者資料行是非稀疏資料行 (例如，固定或變數資料行) ，您就可以看到此狀態碼。

*CbDataMost* 參數不適用於所有資料行值。 此參數只會截斷長文字和長二進位資料行值，而這些值很大，因此與記錄分開儲存。

如果 **JetEnumerateColumns** 在其輸出參數中傳回資料，則呼叫端會負責釋放陣列中的記憶體，以及內嵌在該陣列中的指標所參考的任何記憶體。

#### <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>用戶端</strong></p></td>
<td><p>需要 Windows Vista 或 Windows XP。</p></td>
</tr>
<tr class="even">
<td><p><strong>伺服器</strong></p></td>
<td><p>需要 Windows Server 2008 或 Windows Server 2003。</p></td>
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
[JET_ENUMCOLUMNID](./jet-enumcolumnid-structure.md)  
[JET_ENUMCOLUMN](./jet-enumcolumn-structure.md)  
[JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)  
[JET_PFNREALLOC](./jet-pfnrealloc-callback-function.md)  
[realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019)  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)
