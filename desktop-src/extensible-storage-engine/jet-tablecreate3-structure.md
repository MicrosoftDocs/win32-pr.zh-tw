---
description: 深入瞭解： JET_TABLECREATE3 結構
title: JET_TABLECREATE3 結構
TOCTitle: JET_TABLECREATE3 Structure
ms:assetid: 61909569-e704-494b-a56d-b64d1a2ee157
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269264(v=EXCHG.10)
ms:contentKeyID: 32765566
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 587649b592f2b0d213a481c3bfbecc723240e486
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991680"
---
# <a name="jet_tablecreate3-structure"></a>JET_TABLECREATE3 結構


_**適用于：** Windows |Windows Server_

**JET_TABLECREATE3** 結構包含建立資料表時所需的資訊，此資料表會填入可延伸儲存引擎中的資料行和索引， (ESE) 資料庫，並指定回呼函數。 [JetCreateTableColumnIndex3](./jetcreatetablecolumnindex3-function.md)函數會使用 **JET_TABLECREATE3** 結構。

在 Windows 7 作業系統中引進了 **JET_TABLECREATE3** 結構。

``` cpp
typedef struct tagJET_TABLECREATE3 {
  unsigned long cbStruct;
  tchar* szTableName;
  tchar* szTemplateTableName;
  unsigned long ulPages;
  unsigned long ulDensity;
  JET_COLUMNCREATE* rgcolumncreate;
  unsigned long cColumns;
    JET_INDEXCREATE2* rgindexcreate;
  unsigned long cIndexes;
  tchar* szCallback;
  JET_CBTYP cbtyp;
  JET_GRBIT grbit;
  JET_TABLEID tableid;
  un  JET_GRBIT grbit;
  JET_SPACEHINTS* pSeqSpacehints;
  JET_SPACEHINTS* pLVSpacehints;
  unsigned long cbSeparateLV;
  JET_TABLEID tableid;
  unsigned long cCreated;
} JET_TABLECREATE3;>
```

### <a name="members"></a>成員

**cbStruct**

此結構的大小，以位元組為單位， (未來的擴充) 。 它必須設定為 sizeof ( JET_TABLECREATE3 ) （以位元組為單位）。

**szTableName**

要建立之資料表的名稱。

此名稱必須符合下列條件：

  - 它必須有小於 JET_cbNameMost 的值，不包括終止的 null。

  - 它必須包含下列字元組：0到9、A 到 Z、a 到 z，以及除了驚嘆號以外的所有其他標點符號 (\!) 、逗點 (、) 、左括弧 (\[) 和右括弧 () \] ; 也就是說，ASCII 字元0x20、0x22 至0x2d、0x2f 至0x5a、0x5c 和0x5d 至0x7f。

  - 不得以空格開頭。

  - 它必須包含至少一個非空白字元。

**szTemplateTableName**

要從中繼承基底資料定義語言 (DDL) 的現有資料表名稱。 使用範本資料表可讓您輕鬆地建立具有相同資料行和索引的多個資料表。

**ulPages**

要配置給資料表的初始資料庫頁面數目。 如果有多個資料列插入此資料表中，指定大於1的數位可以減少片段。

**ulDensity**

資料表密度（以百分比為單位）。 此數位必須是0或20到100的範圍。 傳遞0表示應該使用預設值。 預設值是 80。

**rgcolumncreate**

[JET_COLUMNCREATE](./jet-columncreate-structure.md)結構的陣列，其中每一個都對應到要在新資料表中建立的資料行。

**cColumns**

*Rgcolumncreate* 參數中 [JET_COLUMNCREATE](./jet-columncreate-structure.md)元素的數目。

**rgindexcreate**

[JET_INDEXCREATE2](./jet-indexcreate2-structure.md)結構的陣列，其中每一個都對應至要在新資料表中建立的索引。

**cIndexes**

*Rgindexcreate* 參數中 [JET_INDEXCREATE2](./jet-indexcreate2-structure.md)元素的數目。

**szCallback**

在特定事件期間呼叫的函式。 **cbtyp** 會判斷呼叫回呼函式的時間。

**SzCallback** 的格式必須是 "module \! function"，例如 "Alpha \! Beta" 指的是名為 "Alpha" 的模組中的搶鮮版（Beta）函數。

函數的原型必須符合 [JET_CALLBACK](./jet-callback-callback-function.md) 回呼函數。

**cbtyp**

描述 **szCallback** 所指定之回呼函式的類型。 如需詳細資訊，請參閱 [JET_CBTYP](./jet-cbtyp.md)。

此位位由下表所列的一或多個位值所組成。

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
<td><p>JET_cbtypFinalize</p></td>
<td><p>當可以完成的資料行已消失時，就會呼叫回呼函數。</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypBeforeInsert</p></td>
<td><p>回呼函式會在插入記錄之前呼叫。</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypAfterInsert</p></td>
<td><p>在資料庫引擎完成插入記錄之後，將會呼叫回呼函數。</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypBeforeReplace</p></td>
<td><p>回呼函數將在修改記錄之前呼叫。</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypAfterReplace</p></td>
<td><p>完成記錄修改之後，將會呼叫回呼函數。</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypBeforeDelete</p></td>
<td><p>回呼函數將在刪除記錄之前呼叫。</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypAfterDelete</p></td>
<td><p>刪除記錄之後，將會呼叫回呼函數。</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypUserDefinedDefaultValue</p></td>
<td><p>系統會呼叫回呼函式來計算使用者定義的預設值。</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypFreeCursorLS</p></td>
<td><p>當必須釋放與資料指標相關聯的本機儲存體時，就會呼叫回呼函數。</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypFreeTableLS</p></td>
<td><p>當必須釋放與資料表相關聯的本機儲存體時，就會呼叫回呼函數。</p></td>
</tr>
</tbody>
</table>


**grbit**

位群組，其中包含下表所列的零或多個呼叫選項值。

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
<td><p>JET_bitTableCreateFixedDDL</p></td>
<td><p>防止資料表上的 DDL 作業 (例如新增或移除) 的資料行。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableCreateTemplateTable</p></td>
<td><p>使資料表成為範本資料表。 然後，新的資料表可將此資料表的名稱指定為其範本資料表。 設定 JET_bitTableCreateTemplateTable 意指 JET_bitTableCreateFixedDDL。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableCreateNoFixedVarColumnsInDerivedTables</p></td>
<td><p>必須搭配 JET_bitTableCreateTemplateTable 使用。 已取代。 請勿使用。</p></td>
</tr>
</tbody>
</table>


**pSeqSpacehints**

預設連續索引的 [JET_SPACEHINTS](./jet-spacehints-structure.md) 結構指標。

**pSeqSpacehints** 是在 Windows 7 中引進的。

**pLVSpacehints**

分隔 Long 值樹狀結構的 [JET_SPACEHINTS](./jet-spacehints-structure.md) 結構指標。

**pLVSpacehints** 是在 Windows 7 中引進的。

**cbSeparateLV**

將內建的 LV 與主要記錄分開的大小。 分隔的 LV 樹狀結構的任何 long 值 c 結構。 如需詳細資訊，請參閱 ng- [JET_SPACEHINTS](./jet-spacehints-structure.md)中的值。 如果記錄變得太大，則小於此值的 Long 值資料行可能會分開。

**cbSeparateLV** 是在 Windows 7 中引進的。

**tableid**

如果 API 呼叫成功，則為包含新資料表之 [JET_TABLEID](./jet-tableid.md) 的輸出欄位。 如果 API 呼叫失敗，則值為未定義。 此資料表會以獨佔方式開啟。

**到尚未建立**

輸出欄位，其中包含 API 呼叫成功時所建立的物件計數。 如果 API 呼叫失敗，則值為未定義。

所建立的物件計數等於已成功建立之資料行、資料表和索引的總和。

### <a name="requirements"></a>規格需求

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
<td><p><strong>Unicode</strong></p></td>
<td><p>實作為 <strong>JET_TABLECREATE3_W</strong> (Unicode) 和 <strong>JET_TABLECREATE3_A</strong> (ANSI) 。</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>另請參閱

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateTable](./jetcreatetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)  
[JetDefragment2](./jetdefragment2-function.md)
