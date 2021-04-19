---
description: 深入瞭解： JetCreateTableColumnIndex3 函數
title: JetCreateTableColumnIndex3 函式
TOCTitle: JetCreateTableColumnIndex3 Function
ms:assetid: c1a1b091-b4a6-4cdc-a0ea-af21c1462449
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294079(v=EXCHG.10)
ms:contentKeyID: 32765694
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableColumnIndex3
- JetCreateTableColumnIndex3W
- JetCreateTableColumnIndex3A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bf1d6aed3178f5593826097f8c5d6b01bd8c72d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988461"
---
# <a name="jetcreatetablecolumnindex3-function"></a>JetCreateTableColumnIndex3 函式


_**適用于：** Windows |Windows Server_

## <a name="jetcreatetablecolumnindex3-function"></a>JetCreateTableColumnIndex3 函式

**JetCreateTableColumnIndex3** 函式會在 ESE 資料庫中建立一個資料表，其中包含一組初始的索引，以及一組 [JET_TABLECREATE3](./jet-tablecreate3-structure.md)結構陣列的初始資料行。 [JET_TABLECREATE3](./jet-tablecreate3-structure.md)結構允許指定回呼函數。

**Windows 7：** **JetCreateTableColumnIndex3** 是在 windows 7 作業系統中引進。

```cpp
    JET_ERR JET_API JetCreateTableColumnIndex3(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in_out      JET_TABLECREATE3* ptablecreate
    );
```

### <a name="parameters"></a>參數

*sesid*

要用於 API 呼叫的資料庫會話內容。

*dbid*

用於 API 呼叫的資料庫識別碼。

*ptablecreate*

[JET_TABLECREATE3](./jet-tablecreate3-structure.md)結構的指標，此結構會定義要建立的資料表。 如需詳細資訊，請參閱 [JET_TABLECREATE3](./jet-tablecreate3-structure.md) 。

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
<td><p>JET_errCallbackNotResolved</p></td>
<td><p>無法解析回呼函數。 可能找不到 DLL，或可能找不到 DLL 中的函數。 啟用足夠記錄之後，事件記錄檔將會提供更多詳細資料。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errCannotIndex</p></td>
<td><p>嘗試透過「正在進行」（update）或 SLV 資料行來編制索引， (請注意，SLV 資料行已被取代) 。</p></td>
</tr>
<tr class="even">
<td><p>JET_errCannotNestDDL</p></td>
<td><p>如果 ptablecreate- &gt; grbit 指定 JET_bitTableCreateTemplateTable，但 ptablecreate- &gt; szTemplateTableName 設定為 Null。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnDuplicate</p></td>
<td><p>資料行已經存在。</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnNotFound</p></td>
<td><p>嘗試在不存在的資料行上建立索引。 嘗試在不存在的資料行上有條件地編制索引，也會產生這個錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnRedundant</p></td>
<td><p>嘗試加入重複的資料行。 應該不會有一個以上的自動遞增資料行，而且每個資料表不能有一個以上的版本資料行。</p></td>
</tr>
<tr class="even">
<td><p>JET_errDensityInvalid</p></td>
<td><p>如果<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>ulDensity</strong>成員設定為小於20或超過100的數位，則會傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDDLNotInheritable</p></td>
<td><p>表示在<a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a>結構的<strong>szTemplateTableName</strong>成員中命名的資料表未標示為樣板資料表 (也就是說，該資料表沒有 JET_bitTableCreateTemplateTable 設定) 。</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexDuplicate</p></td>
<td><p>嘗試定義兩個相同的索引。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexHasPrimary</p></td>
<td><p>嘗試為數據表指定一個以上的主要索引。 資料表必須只有一個主要索引。 如果未指定任何主要索引，database engine 將會以透明方式建立一個索引。</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexInvalidDef</p></td>
<td><p>指定了不正確索引定義。 以下是接收此錯誤的一些可能原因：</p>
<ul>
<li><p>主要索引是條件式 (也就是， <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>grbit</strong>成員已 JET_bitIndexPrimary 設定，而<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>cConditionalColumn</strong>成員大於零) 。</p></li>
<li><p>Windows Server 2003 和更新版本的 Windows。 嘗試建立具有元組限制的元組索引，但未在<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構中傳遞<strong>ptuplelimits</strong>成員 (也就是說，JET_INDEXCREATE2 結構的<strong>grbit</strong>成員已 JET_bitIndexTupleLimits 設定，但<strong>ptuplelimits</strong>指標為 Null) 。</p></li>
<li><p>在<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>szKey</strong>成員中傳入不正確索引鍵定義。 如需有效定義的討論，請參閱 <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> 。</p></li>
<li><p>將<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>中的<strong>cbVarSegMac</strong>成員設定為大於主要索引的 JET_cbPrimaryKeyMost () 或大於次要索引 JET_cbSecondaryKeyMost 的 () 。</p></li>
<li><p>傳遞不正確使用者定義 Unicode 索引組合， (<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>) 的<strong>grbit</strong>成員中設定 JET_bitIndexUnicode 位的成員。 某些常見的原因包括<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>PIDXUNICODE</strong>成員為 Null，或<strong>PIDXUNICODE</strong>結構中指定的 LCID 無效。</p></li>
<li><p>指定主要索引的多重值資料行。</p></li>
<li><p>正在嘗試編制太多條件式資料行的索引。 <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>cConditionalColumn</strong>成員不得大於 JET_ccolKeyMost。</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>Windows XP 和更新版本的 Windows。 已指定 <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> 結構，但不支援其限制。 請參閱 <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> 結構的「備註」一節。</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesNonUniqueOnly</p></td>
<td><p>Windows XP 和更新版本的 Windows。 元組索引不可以是唯一的 (也就是說， <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<em>grbit</em>成員不能同時有 JET_bitIndexPrimary 和 JET_bitIndexUnique 設定) 。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesOneColumnOnly</p></td>
<td><p>Windows XP 和更新版本的 Windows。 元組索引只能在單一資料行上 (也就是，如果<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>grbit</strong>成員已設定 JET_bitIndexTuples，且<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>szKey</strong>成員指定了一個以上的資料行) 。</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesSecondaryIndexOnly</p></td>
<td><p>Windows XP 和更新版本的 Windows。 元組索引不可以是主要索引 (也就是說， <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>grbit</strong>成員不能同時有 JET_bitIndexPrimary 和 JET_bitIndexTuples 設定) 。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesTextColumnsOnly</p></td>
<td><p>Windows XP 和更新版本的 Windows。 元組索引只能位於 text 或 Unicode 資料行上。 嘗試將其他資料行的索引 (例如二進位資料行) 會導致 JET_errIndexTuplesTextColumnsOnly。</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesVarSegMacNotAllowed</p></td>
<td><p>Windows XP 和更新版本的 Windows。 元組索引不允許設定<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>cbVarSegMac</strong>成員。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction</p></td>
<td><p>嘗試在交易中建立沒有版本資訊的索引。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCodePage</p></td>
<td><p><a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a>結構的<strong>cp</strong>成員未設定為有效的字碼頁。 Text 資料行的唯一有效值是英文 (1252) 和 Unicode (1200) 。 0值表示預設值將使用 (英文、1252) 。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidColumnType</p></td>
<td><p><a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a>結構的<strong>coltyp</strong>成員未設定為有效的資料行類型。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidCreateIndex</p></td>
<td><p>以下是可能發生此錯誤的一些原因：</p>
<ul>
<li><p><a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>結構的<strong>rgindexcreate</strong>成員已設定為 Null。</p></li>
<li><p><a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>結構的<strong>rgcolumncreate</strong>成員已設定為 Null。</p></li>
<li><p><a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>cbStruct</strong>成員未設定為有效的值。</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>在<a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a>中指定了不正確<strong>grbit</strong>成員組合。</p>
<p>因為 <strong>grbit</strong> 成員包含不一致的值，所以索引定義無效。 以下是一些可能的原因：</p>
<ul>
<li><p>主要索引具有指定的略過位 (也就是，JET_bitIndexPrimary 是以 JET_bitIndexIgnoreNull、JET_bitIndexIgnoreAnyNull 或 JET_bitIndexIgnoreFirstNull) 傳遞。</p></li>
<li><p>空白索引不會忽略任何 Null 成員 (也就是說， <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>grbit</strong>成員已 JET_bitIndexEmpty 設定，但沒有 JET_bitIndexIgnoreAnyNull 設定) 。</p></li>
<li><p>傳入具有無效<strong>grbit</strong>成員的<a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>結構。</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>在 (中傳遞不正確地區設定識別碼 (LCID) ，方法是透過<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構中的<strong>pidxunicode</strong>成員所指向的<a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a>結構的<strong>lcid</strong>成員，或透過<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構) 的<strong>lcid</strong>欄位來傳遞。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>指定的參數無效。 以下是一些可能的原因：</p>
<ul>
<li><p><a href="gg269264(v=exchg.10).md">JET_TABLECREATE3</a>結構的<strong>RGCOLUMNCREATE</strong>成員為 Null。</p></li>
<li><p><a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>結構的<strong>rgcolumncreate</strong>成員中指定的其中一個<a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a>結構的<strong>cbStruct</strong>成員未設定為 sizeof ( JET_COLUMNCREATE ) 。</p></li>
<li><p><a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>cbKey</strong>成員設定為零。</p></li>
<li><p><a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>cbStruct</strong>成員未設定為 sizeof ( JET_INDEXCREATE2 ) 。</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errRecordTooBig</p></td>
<td><p>記錄太大。 所有固定資料行之<a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a>結構的<strong>cbMax</strong>成員總和不得超過某個值。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTableDuplicate</p></td>
<td><p>資料表已經存在。</p></td>
</tr>
<tr class="even">
<td><p>JET_errTooManyColumns</p></td>
<td><p>嘗試將過多的資料行新增至資料表。 資料表不能超過 JET_ccolFixedMost 固定資料行，不能超過 JET_ccolVarMost 的可變長度資料行，且不能超過 JET_ccolTaggedMost 標記的資料行。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errUnicodeTranslationFail</p></td>
<td><p>嘗試將 Unicode 資料行正規化時發生錯誤。 這可能是因為系統資源不足所造成。</p></td>
</tr>
<tr class="even">
<td><p>JET_errSpaceHintsInvalid</p></td>
<td><p>JET 空間提示結構的元素不正確或可採取動作。</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>備註

名稱 **JetCreateTableColumnIndex3** 來自物件的建立順序：它會先建立資料表、資料行，最後再建立索引。 **JetCreateTableColumnIndex3** 會建立一份資料表，其中包含一組初始的資料行和索引。 您可以使用 [JetAddColumn](./jetaddcolumn-function.md)、 [JetDeleteColumn](./jetdeletecolumn-function.md)、 [JetDeleteColumn2](./jetdeletecolumn2-function.md)、 [JetCreateIndex](./jetcreateindex-function.md)、 [JetCreateIndex2](./jetcreateindex2-function.md)、 [JetCreateIndex3](./jetcreateindex3-function.md)和 [JetDeleteIndex](./jetdeleteindex-function.md)，動態地新增和移除其他資料行和索引。

如同 [JetOpenTable](./jetopentable-function.md)，當應用程式使用傳回的 *tableid* 完成時，通常應該會以 [JetCloseTable](./jetclosetable-function.md)來關閉它。

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>實作為 <strong>JetCreateTableColumnIndex3W</strong> (Unicode) 和 <strong>JetCreateTableColumnIndex3A</strong> (ANSI) 。</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>另請參閱

[JET_CBTYP](./jet-cbtyp.md)  
[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_INDEXCREATE2](./jet-indexcreate2-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JET_TABLECREATE3](./jet-tablecreate3-structure.md)  
[JET_TUPLELIMITS](./jet-tuplelimits-structure.md)  
[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)  
[JetCreateIndex3](./jetcreateindex3-function.md)  
[JetCreateTable](./jetcreatetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetDeleteColumn](./jetdeletecolumn-function.md)  
[JetDeleteColumn2](./jetdeletecolumn2-function.md)
