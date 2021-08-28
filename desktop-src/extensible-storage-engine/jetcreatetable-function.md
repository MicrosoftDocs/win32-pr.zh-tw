---
description: 深入瞭解： JetCreateTable 函數
title: JetCreateTable 函式
TOCTitle: JetCreateTable Function
ms:assetid: 28455b8b-0000-4bd5-a3ca-e1ef0446ee07
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269210(v=EXCHG.10)
ms:contentKeyID: 32765513
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateTableW
- JetCreateTable
- JetCreateTableA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6e06e4c2d0cfa55ff85279b634449fd313eb7570
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985021"
---
# <a name="jetcreatetable-function"></a>JetCreateTable 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetcreatetable-function"></a>JetCreateTable 函式

**JetCreateTable** 函數會在 ESE 資料庫中建立空的資料表。

```cpp
    JET_ERR JET_API JetCreateTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName,
      __in          unsigned long lPages,
      __in          unsigned long lDensity,
      __out         JET_TABLEID* ptableid
    );
```

### <a name="parameters"></a>參數

*sesid*

要使用的資料庫會話內容。

*dbid*

要使用的資料庫識別碼。

*szTableName*

要建立之索引的名稱。

名稱必須根據下列規則來格式化：

  - 小於 JET_cbNameMost，不包括終止的 Null。

  - 由下列一組字元組成：0到9、A 到 Z、a 到 z，以及 "" 以外的所有其他標點符號 \!  (驚嘆號) 、"、" (逗號) 、" \[ " (左括弧) 和 " \] " (右括弧) —也就是 ASCII 字元0x20、0x22 至0x2d、0x2f 至0x5a、0x5c、0x5d 到0x7f。

  - 不是以空格開頭。

  - 至少要有一個非空白字元。

*lPages*

要配置給資料表的初始資料庫頁面數目。 如果有多個資料列插入此資料表中，指定大於1的數位可以減少片段。

*lDensity*

資料表密度（以百分比為單位）。 此數位必須是0或20到100的範圍。 傳遞0表示應該使用預設值。 預設值為80。

*ptableid*

成功時，會在此欄位中傳回資料表識別碼。 如果 API 未傳回 JET_errSuccess，此值為未定義。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errCallbackNotResolved</p> | <p>無法解析回呼函數。 可能找不到 DLL，或可能找不到 DLL 中的函數。 啟用足夠記錄之後，事件記錄檔將會提供更多詳細資料。</p> | 
| <p>JET_errCannotIndex</p> | <p>嘗試透過「正在進行」（update）或 SLV 資料行來編制索引， (請注意，SLV 資料行已被取代) 。</p> | 
| <p>JET_errCannotNestDDL</p> | <p>如果 ptablecreate- &gt; grbit 指定 JET_bitTableCreateTemplateTable，但 ptablecreate- &gt; szTemplateTableName 設定為 Null。</p> | 
| <p>JET_errColumnDuplicate</p> | <p>資料行已經存在。</p> | 
| <p>JET_errColumnNotFound</p> | <p>嘗試在不存在的資料行上建立索引。 嘗試在不存在的資料行上有條件地編制索引，也會產生這個錯誤。</p> | 
| <p>JET_errColumnRedundant</p> | <p>嘗試加入重複的資料行。 應該不會有一個以上的自動遞增資料行，而且每個資料表不能有一個以上的版本資料行。</p> | 
| <p>JET_errDensityInvalid</p> | <p>在<a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a>或<a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>結構的<em>ulDensity</em>成員中傳遞了不正確密度。</p> | 
| <p>JET_errDDLNotInheritable</p> | <p>表示<a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a>結構的<strong>szTemplateTableName</strong>成員中所命名的資料表不是標示為樣板資料表 (也就是說，該資料表沒有 JET_bitTableCreateTemplateTable 設定) 。</p> | 
| <p>JET_errIndexDuplicate</p> | <p>嘗試定義兩個相同的索引。</p> | 
| <p>JET_errIndexHasPrimary</p> | <p>嘗試為數據表指定一個以上的主要索引。 資料表必須只有一個主要索引。 如果未指定任何主要索引，database engine 將會以透明方式建立一個索引。</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>指定了不正確索引定義。 收到此錯誤的部分可能原因包括：</p><ul><li><p>主要索引是條件式 (也就是， <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>grbit</strong>成員已 JET_bitIndexPrimary 設定，而<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>cConditionalColumn</strong>成員大於零) 。</p></li><li><p>Windows伺服器2003和更新版本。 嘗試建立具有元組限制的元組索引，但未在<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構中傳遞<strong>ptuplelimits</strong>成員 (也就是說， <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>grbit</strong>成員已 JET_bitIndexTupleLimits 設定，但<strong>ptuplelimits</strong>指標為 Null) 。</p></li><li><p>在<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>szKey</strong>成員中傳入不正確索引鍵定義。 如需有效定義的討論，請參閱 <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> 。</p></li><li><p>將<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>中的<strong>cbVarSegMac</strong>成員設定為大於主要索引的 JET_cbPrimaryKeyMost () 或大於次要索引 JET_cbSecondaryKeyMost 的 () 。</p></li><li><p>傳遞不正確使用者定義 Unicode 索引組合， (在<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>) 的<strong>grbit</strong>成員中設定 JET_bitIndexUnicode 位。 某些常見的原因包括<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>PIDXUNICODE</strong>成員為 Null，或<strong>PIDXUNICODE</strong>結構中指定的 LCID 無效。</p></li><li><p>指定主要索引的多重值資料行。</p></li><li><p>正在嘗試編制太多條件式資料行的索引。 <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>cConditionalColumn</strong>成員不得大於 JET_ccolKeyMost。</p></li></ul> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>WindowsXP 和更新版本。 已指定 <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> 結構，但不支援其限制。 請參閱 <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> 結構的「備註」一節。</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly</p> | <p>WindowsXP 和更新版本。 元組索引不可以是唯一的 (也就是說， <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<em>grbit</em>成員不能同時有 JET_bitIndexPrimary 和 JET_bitIndexUnique 設定) 。</p> | 
| <p>JET_errIndexTuplesOneColumnOnly</p> | <p>WindowsXP 和更新版本。 元組索引只能在單一資料行上 (也就是，如果<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>grbit</strong>成員已設定 JET_bitIndexTuples，且<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>szKey</strong>成員指定了一個以上的資料行) 。</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly</p> | <p>WindowsXP 和更新版本。 元組索引不可以是主要索引 (也就是說， <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>grbit</strong>成員不能同時有 JET_bitIndexPrimary 和 JET_bitIndexTuples 設定) 。</p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed</p> | <p>WindowsXP 和更新版本。 元組索引不允許設定<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>cbVarSegMac</strong>成員。</p> | 
| <p>JET_errIndexTuplesTextColumnsOnly</p> | <p>WindowsXP 和更新版本。 元組索引只能位於 text 或 Unicode 資料行上。 嘗試將其他資料行的索引 (例如二進位資料行) 會導致 JET_errIndexTuplesTextColumnsOnly。</p> | 
| <p>JET_errInTransaction</p> | <p>嘗試在交易中建立沒有版本資訊的索引。</p> | 
| <p>JET_errInvalidCodePage</p> | <p><a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a>結構的<strong>cp</strong>成員未設定為有效的字碼頁。 Text 資料行的唯一有效值是英文 (1252) 和 Unicode (1200) 。 0值表示預設值將使用 (英文、1252) 。</p> | 
| <p>JET_errInvalidColumnType</p> | <p><a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a>結構的<strong>coltyp</strong>成員未設定為有效的資料行類型。</p> | 
| <p>JET_errInvalidCreateIndex</p> | <p>可能會發生此錯誤的部分原因：</p><ul><li><p><a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>結構的<strong>rgindexcreate</strong>成員已設定為 Null。</p></li><li><p><a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>結構的<strong>rgcolumncreate</strong>成員已設定為 Null。</p></li><li><p><a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>cbStruct</strong>成員未設定為有效的值。</p></li></ul> | 
| <p>JET_errInvalidgrbit</p> | <p><a href="gg294146(v=exchg.10).md">JET_TABLECREATE</a>或<a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>中指定了不正確<strong>grbit</strong>成員組合。</p><p>因為 <strong>grbit</strong> 成員包含不一致的值，所以索引定義無效。 可能的原因如下：</p><ul><li><p>主要索引具有指定的略過位 (也就是，JET_bitIndexPrimary 是以 JET_bitIndexIgnoreNull、JET_bitIndexIgnoreAnyNull 或 JET_bitIndexIgnoreFirstNull) 傳遞。</p></li><li><p>空白索引不會忽略任何 Null 成員 (也就是說， <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>grbit</strong>成員已 JET_bitIndexEmpty 設定，但沒有 JET_bitIndexIgnoreAnyNull 設定) 。</p></li><li><p>傳入具有無效<strong>grbit</strong>成員的<a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>結構。</p></li></ul> | 
| <p>JET_errInvalidLanguageId</p> | <p>在 (中傳遞不正確地區設定識別碼 (LCID) ，方法是透過<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構中的<strong>pidxunicode</strong>成員所指向的<a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a>結構的<strong>lcid</strong>成員，或透過<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構) 的<strong>lcid</strong>欄位來傳遞。</p> | 
| <p>JET_errInvalidParameter</p> | <p>指定的參數無效。 可能的原因如下：</p><ul><li><p><a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>結構的<strong>RGCOLUMNCREATE</strong>成員為 Null。</p></li><li><p><a href="gg269203(v=exchg.10).md">JET_TABLECREATE2</a>結構的<strong>rgcolumncreate</strong>成員中指定的其中一個<a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a>結構的<strong>cbStruct</strong>成員未設定為 sizeof ( JET_COLUMNCREATE ) 。</p></li><li><p><a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>cbKey</strong>成員設定為零。</p></li><li><p><a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>結構的<strong>cbStruct</strong>成員未設定為 sizeof ( JET_INDEXCREATE ) 。</p></li></ul> | 
| <p>JET_errRecordTooBig</p> | <p>記錄太大。 所有固定資料行之<a href="gg269252(v=exchg.10).md">JET_COLUMNCREATE</a>結構的<strong>cbMax</strong>成員總和不得超過某個值。</p> | 
| <p>JET_errTableDuplicate</p> | <p>資料表已經存在。</p> | 
| <p>JET_errTooManyColumns</p> | <p>嘗試將過多的資料行新增至資料表。 資料表不能超過 JET_ccolFixedMost 固定資料行，不能超過 JET_ccolVarMost 的可變長度資料行，且不能超過 JET_ccolTaggedMost 標記的資料行。</p> | 
| <p>JET_errUnicodeTranslationFail</p> | <p>嘗試將 Unicode 資料行正規化時發生錯誤。 這可能是因為系統資源不足所造成。</p> | 



#### <a name="remarks"></a>備註

**JetCreateTable** 會建立不包含任何資料行的資料表。 若要加入資料行，請參閱 [JetAddColumn](./jetaddcolumn-function.md)。

在內部， **JetCreateTable** 會呼叫 [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)，並使用下列內容填入 [JET_TABLECREATE2](./jet-tablecreate2-structure.md) 結構：

  - JET_TABLECREATE2. cbStruct = sizeof ( JET_TABLECREATE2 ) 

  - JET_TABLECREATE2. szTableName = szTableName

  - JET_TABLECREATE2. ulPages = lPage

  - JET_TABLECREATE2. ulDensity = lDensity

  - JET_TABLECREATE2. tableid = JET_tableidNil

內部 [JET_TABLECREATE2](./jet-tablecreate2-structure.md) 結構的所有其他欄位都設定為零或 Null。 在輸出時， *ptableid* 會設定為 JET_TABLECREATE2. tableid。

如需詳細資訊，請參閱 [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) 。

如同 [JetOpenTable](./jetopentable-function.md)，當應用程式使用從 [JET_TABLECREATE2](./jet-tablecreate2-structure.md)結構傳回的 **tableid** 成員完成時，通常應該會以 [JetCloseTable](./jetclosetable-function.md)來關閉。

#### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 
| <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | 
| <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 
| <p><strong>Unicode</strong></p> | <p>實作為 <strong>JetCreateTableW</strong> (Unicode) 和 <strong>JetCreateTableA</strong> (ANSI) 。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
