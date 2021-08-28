---
description: 深入瞭解： JetCreateIndex3 函數
title: JetCreateIndex3 函式
TOCTitle: JetCreateIndex3 Function
ms:assetid: bc9b940e-65c6-49d6-ad32-74434527d29f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294075(v=EXCHG.10)
ms:contentKeyID: 32765690
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndex3A
- JetCreateIndex3
- JetCreateIndex3W
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d0e50c0d2a2baab2b512a7525e5a852b335f99d4
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122981941"
---
# <a name="jetcreateindex3-function"></a>JetCreateIndex3 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetcreateindex3-function"></a>JetCreateIndex3 函式

**JetCreateIndex3** 函式會在 ESE 資料庫中建立資料的索引，可用來快速找出特定資料。

**Windows 7： JetCreateIndex3** 是在 Windows 7 作業系統中引進。

```cpp
    JET_ERR JET_API JetCreateIndex3(
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

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errCannotIndex</p> | <p>嘗試透過「正在進行」（update）或 SLV 資料行來編制索引， (請注意，SLV 資料行已被取代) 。</p> | 
| <p>JET_errColumnNotFound</p> | <p>嘗試在不存在的資料行上建立索引。 嘗試在不存在的資料行上有條件地編制索引，也會產生這個錯誤。</p> | 
| <p>JET_errDensityInvalid</p> | <p>如果<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>ulDensity</strong>成員設定為小於20或大於100的數位，則會傳回此錯誤。</p> | 
| <p>JET_errIndexDuplicate</p> | <p>嘗試定義兩個相同的索引。</p> | 
| <p>JET_errIndexHasPrimary</p> | <p>嘗試為數據表指定一個以上的主要索引。 資料表必須只有一個主要索引。 如果未指定任何主要索引，database engine 將會以透明方式建立一個索引。</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>指定了不正確索引定義。 以下是接收此錯誤的一些可能原因：</p><ul><li><p>主要索引是條件式 (<strong>grbit</strong>成員<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>已 JET_bitIndexPrimary 設定，而<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>的<strong>cConditionalColumn</strong>成員大於零) 。</p></li><li><p>WindowsWindows 的伺服器2003和更新版本。 嘗試建立具有元組限制的元組索引，但未在<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>中傳遞<strong>ptuplelimits</strong>成員的資訊 (亦即， <em>grbit</em>已 JET_bitIndexTupleLimits 設定，但<strong>ptuplelimits</strong>指標為 Null) 。</p></li><li><p>在<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>szKey</strong>成員中傳入不正確索引鍵定義。 如需有效定義的討論，請參閱 <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> 。</p></li><li><p>將<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>中的<strong>cbVarSegMac</strong>成員設定為大於主要索引的 JET_cbPrimaryKeyMost () 或大於次要索引 JET_cbSecondaryKeyMost 的 () 。</p></li><li><p>傳遞不正確使用者定義 Unicode 索引組合， (在<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>) 的<strong>grbit</strong>成員中設定 JET_bitIndexUnicode 位。 常見的原因可能是 <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> 結構的 pidxunicode 欄位為 Null，或 pidxunicode 結構中指定的 LCID 無效。</p></li><li><p>指定主要索引的多重值資料行。</p></li><li><p>正在嘗試編制太多條件式資料行的索引。 <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>cConditionalColumn</strong>成員不得大於 JET_ccolKeyMost。</p></li></ul> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>WindowsWindows 的 XP 和更新版本。 已指定 <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> 結構，但不支援其限制。 請參閱 <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> 結構的「備註」一節。</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly</p> | <p>WindowsWindows 的 XP 和更新版本。 元組索引不可以是唯一的 (<em>grbit</em> 不能同時有 JET_bitIndexTuples 和 JET_bitIndexUnique 設定) 。</p> | 
| <p>JET_errIndexTuplesOneColumnOnly</p> | <p>WindowsWindows 的 XP 和更新版本。 元組索引只能在單一資料行上 (也就是說， <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>grbit</strong>成員已 JET_bitIndexTuples 設定，而<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>szKey</strong>成員指定了一個以上的資料行) 。</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly</p> | <p>WindowsWindows 的 XP 和更新版本。 元組索引不可以是主要索引 (也就是說， <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>grbit</strong>成員不能同時有 JET_bitIndexPrimary 和 JET_bitIndexTuples 設定) 。</p> | 
| <p>JET_errIndexTuplesTextColumnsOnly</p> | <p>WindowsWindows 的 XP 和更新版本。 元組索引只能位於 text 或 Unicode 資料行上。 嘗試將其他資料行索引 (例如，二進位資料行) 將會導致 JET_errIndexTuplesTextColumnsOnly。</p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed</p> | <p>WindowsWindows 的 XP 和更新版本。 元組索引不允許設定<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>cbVarSegMac</strong>成員。</p> | 
| <p>JET_errInTransaction</p> | <p>嘗試在交易中建立沒有版本資訊的索引。</p> | 
| <p>JET_errInvalidgrbit</p> | <p>因為<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>grbit</strong>成員包含不一致的值，所以索引定義無效。 以下是一些可能的原因：</p><ul><li><p>主要索引具有指定的略過位 (JET_bitIndexPrimary 以 JET_bitIndexIgnoreNull、JET_bitIndexIgnoreAnyNull 或 JET_bitIndexIgnoreFirstNull) 之一傳遞。</p></li><li><p>空白索引不會忽略任何 NULL 欄位 (也就是說， <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>grbit</strong>成員已 JET_bitIndexEmpty 設定，但沒有 JET_bitIndexIgnoreAnyNull 設定) 。</p></li><li><p>傳入具有無效<strong>grbit</strong>成員的<a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>結構。 請參閱 <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>。</p></li></ul><p>當您一次建立多個索引時 (也就是說，如果 <em>cIndexCreate</em> 參數大於一個) ，則沒有任何索引可以包含下列任何位：</p><ul><li><p>JET_bitIndexPrimary</p></li><li><p>JET_bitIndexUnversioned</p></li><li><p>JET_bitIndexEmpty</p></li></ul> | 
| <p>JET_errInvalidLanguageId</p> | <p>不正確地區設定識別碼 (LCID) 是透過<a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a>結構中的<strong>lcid</strong>成員傳遞 (（ <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構中的<strong>pidxunicode</strong>成員包含指向的指標，或透過<a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構) 的<strong>lcid</strong>成員）。</p> | 
| <p>JET_errInvalidName</p> | <p>指定了不正確索引名稱。 如需詳細資訊，請參閱 <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> 。</p> | 
| <p>JET_errInvalidParameter</p> | <p>傳遞至 API 的參數無效。 以下是可能會傳回此錯誤的一些原因：</p><ul><li><p><a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>cbKey</strong>欄位設定為零。</p></li><li><p><a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>結構的<strong>cbStruct</strong>成員未設定為 sizeof ( <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ) 。</p></li></ul> | 
| <p>JET_errUnicodeTranslationFail</p> | <p>嘗試將 Unicode 資料行標準化時發生錯誤。 這可能是因為系統資源不足所造成。</p> | 
| <p>JET_errSpaceHintsInvalid</p> | <p>JET 空間提示結構的元素不正確或可採取動作。</p> | 



#### <a name="remarks"></a>備註

當指定的所有索引都成功完成時，就會 JET_errSuccess 傳回值。

**JetCreateIndex3** 會逐一查看 **pindexcreate** 中指定的索引，有時會在第一次失敗時中止。 即使 [JET_INDEXCREATE2](./jet-indexcreate2-structure.md)結構的 **err** 成員包含 JET_errSuccess，仍不會嘗試在第一個具有錯誤之索引之後的任何索引。

#### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 
| <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | 
| <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 
| <p><strong>Unicode</strong></p> | <p>實作為 <strong>JetCreateIndex3W</strong> (Unicode) 和 <strong>JetCreateIndex3A</strong> (ANSI) 。</p> | 



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
