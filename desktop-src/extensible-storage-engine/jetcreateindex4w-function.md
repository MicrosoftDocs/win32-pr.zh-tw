---
description: 深入瞭解： JetCreateIndex4W 函數
title: JetCreateIndex4W 函式
TOCTitle: JetCreateIndex4W Function
ms:assetid: 968745a2-66ce-4c7f-ab5b-43282adc5313
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835044(v=EXCHG.10)
ms:contentKeyID: 49894666
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCreateIndex4W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9a4c7671cbe361b6214552f4c611cd1706c0e48d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980573"
---
# <a name="jetcreateindex4w-function"></a>JetCreateIndex4W 函式


_**適用于：** Windows |Windows Server_

**JetCreateIndex4W** 函式會在可延伸儲存引擎中的資料上建立索引， (ESE) 資料庫，可用來快速找出特定資料。

**JetCreateIndex4W** 函式是在 Windows 8 作業系統中引進的。

``` c++
JET_ERR JET_API JetCreateIndex4W(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          JET_INDEXCREATE2* pindexcreate,
  __in          unsigned long cIndexCreate
);
```

### <a name="parameters"></a>參數

*sesid*

要用於 API 呼叫的資料庫會話內容。

*tableid*

將在其上建立索引的資料表。

*pindexcreate*

[JET_INDEXCREATE2](./jet-indexcreate2-structure.md)結構的陣列，其中每個結構會定義要建立的索引。

*cIndexCreate*

*Pindexcreate* 陣列中的元素數目。

### <a name="return-value"></a>傳回值

此函數會傳回 [JET_ERR](./jet-err.md) 資料類型，其中包含下表所列的其中一個傳回碼。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸 [儲存引擎錯誤](./extensible-storage-engine-errors.md) 和 [錯誤處理參數](./error-handling-parameters.md)。

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
<td><p>JET_errCannotIndex</p></td>
<td><p>嘗試透過「正在進行」（update）或 SLV 資料行來編制索引， (請注意，SLV 資料行已被取代) 。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound</p></td>
<td><p>嘗試在不存在的資料行上建立索引。 針對不存在的資料行嘗試有條件的索引，也會產生這個錯誤。</p></td>
</tr>
<tr class="even">
<td><p>JET_errDensityInvalid</p></td>
<td><p>如果<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>ulDensity</strong>成員設定為小於20或大於100的數位，則會傳回此錯誤。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexDuplicate</p></td>
<td><p>嘗試定義兩個相同的索引。</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexHasPrimary</p></td>
<td><p>嘗試為數據表指定一個以上的主要索引。 資料表必須只有一個主要索引。 如果未指定任何主要索引，database engine 將會以透明方式建立一個索引。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexInvalidDef</p></td>
<td><p>指定了不正確索引定義。 以下是此錯誤的一些可能原因：</p>
<ul>
<li><p>主要索引是條件式 (<strong>grbit</strong>成員<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>已<strong>JET_bitIndexPrimary</strong>設定，而<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>的<strong>cConditionalColumn</strong>成員大於零) 。</p></li>
<li><p>適用于從 Windows Server 2003 開始的 Windows 版本。 嘗試建立具有元組限制的元組索引，但未在<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>中傳遞<strong>ptuplelimits</strong>成員的資訊 (亦即， <em>grbit</em>已<strong>JET_bitIndexTupleLimits</strong>設定，但<strong>ptuplelimits</strong>指標為 null) 。</p></li>
<li><p>在<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>szKey</strong>成員中傳入不正確索引鍵定義。 如需有效定義的詳細資訊，請參閱 <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>。</p></li>
<li><p>將<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>中的<strong>cbVarSegMac</strong>成員設定為大於主要索引的<strong>JET_cbPrimaryKeyMost</strong> () 或大於次要索引 JET_cbSecondaryKeyMost 的<strong> (</strong>) 。</p></li>
<li><p>傳遞不正確使用者定義 Unicode 索引組合， (在<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>) 的<strong>grbit</strong>成員中設定<strong>JET_bitIndexUnicode</strong>位。 常見的原因可能是 <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> 結構的 pidxunicode 欄位為 null，或 pidxunicode 結構中指定的 LCID 無效。</p></li>
<li><p>指定主要索引的多重值資料行。</p></li>
<li><p>正在嘗試編制太多條件式資料行的索引。 <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>cConditionalColumn</strong>成員不得大於<strong>JET_ccolKeyMost</strong>。</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>適用于 windows XP 開頭的 Windows 版本。 已指定 <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> 結構，但不支援其限制。 如需詳細資訊，請參閱 <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> 結構的「備註」一節。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesNonUniqueOnly</p></td>
<td><p>適用于 windows XP 開頭的 Windows 版本。 元組索引不可以是唯一的 (<em>grbit</em> 不能同時有 <strong>JET_bitIndexTuples</strong> 和 <strong>JET_bitIndexUnique</strong> 設定) 。</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesOneColumnOnly</p></td>
<td><p>適用于 windows XP 開頭的 Windows 版本。 元組索引只能在單一資料行上 (也就是說， <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>grbit</strong>成員已<strong>JET_bitIndexTuples</strong>設定，而<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>szKey</strong>成員指定了一個以上的資料行) 。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesSecondaryIndexOnly</p></td>
<td><p>適用于 windows XP 開頭的 Windows 版本。 元組索引不可以是主要索引 (也就是說， <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>grbit</strong>成員不能同時有<strong>JET_bitIndexPrimary</strong>和<strong>JET_bitIndexTuples</strong>設定) 。</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesTextColumnsOnly</p></td>
<td><p>適用于 windows XP 開頭的 Windows 版本。 元組索引只能位於 text 或 Unicode 資料行上。 嘗試將其他資料行索引 (例如，二進位資料行) 將會導致 <strong>JET_errIndexTuplesTextColumnsOnly</strong>。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errIndexTuplesVarSegMacNotAllowed</p></td>
<td><p>適用于 windows XP 開頭的 Windows 版本。 元組索引不允許設定<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>cbVarSegMac</strong>成員。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInTransaction</p></td>
<td><p>嘗試在交易中建立沒有版本資訊的索引。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>因為<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>grbit</strong>成員包含不一致的值，所以索引定義無效。 以下是一些可能的原因：</p>
<ul>
<li><p>主要索引具有指定的略過位 (JET_bitIndexPrimary 以 <strong>JET_bitIndexIgnoreNull</strong>、 <strong>JET_bitIndexIgnoreAnyNull</strong>或 <strong>JET_bitIndexIgnoreFirstNull</strong>) 之一傳遞。</p></li>
<li><p>空白索引不會忽略任何 null 欄位 (也就是說， <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>grbit</strong>成員已<strong>JET_bitIndexEmpty</strong>設定，但沒有<strong>JET_bitIndexIgnoreAnyNull</strong>設定) 。</p></li>
<li><p>傳入具有無效<strong>grbit</strong>成員的<a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>結構。 請參閱 <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>。</p></li>
</ul>
<p>當您一次建立多個索引時 (也就是說，如果 <em>cIndexCreate</em> 參數大於一個) ，則沒有任何索引可以包含下列任何位：</p>
<ul>
<li><p><strong>JET_bitIndexPrimary</strong></p></li>
<li><p><strong>JET_bitIndexUnversioned</strong></p></li>
<li><p><strong>JET_bitIndexEmpty</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidLanguageId</p></td>
<td><p>不正確地區設定識別碼 (LCID) 是透過<a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a>結構中的<strong>lcid</strong>成員傳遞 (（ <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構中的<strong>pidxunicode</strong>成員包含指向的指標，或透過<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構) 的<strong>lcid</strong>成員）。</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidName</p></td>
<td><p>指定了不正確索引名稱。 如需詳細資訊，請參閱 <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> 。</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidParameter</p></td>
<td><p>傳遞至 API 的參數無效。 以下是可能會傳回此錯誤的一些原因：</p>
<ul>
<li><p><a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>cbKey</strong>欄位設定為零。</p></li>
<li><p><a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>cbStruct</strong>成員未設定為 sizeof (JET_INDEXCREATE2) 。</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errUnicodeTranslationFail</p></td>
<td><p>嘗試將 Unicode 資料行標準化時發生錯誤。 這可能是因為系統資源不足所造成。</p></td>
</tr>
<tr class="even">
<td><p>JET_errSpaceHintsInvalid</p></td>
<td><p>JET 空間提示結構的元素不正確或可採取動作。</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>備註

**JetCreateIndex4W** 函式會逐一查看 *pindexcreate* 參數中指定的索引，有時會在第一次失敗時中止。 即使 [JET_INDEXCREATE2](./jet-indexcreate2-structure.md)結構的 **err** 成員包含 JET_errSuccess，仍不會嘗試在第一個具有錯誤之索引之後的任何索引。

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

[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE2](./jet-indexcreate2-structure.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)  
[JET_SPACEHINTS](./jet-spacehints-structure.md)
