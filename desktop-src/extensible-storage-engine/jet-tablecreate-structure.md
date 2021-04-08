---
description: 深入瞭解： JET_TABLECREATE 結構
title: JET_TABLECREATE 結構
TOCTitle: JET_TABLECREATE Structure
ms:assetid: ff06325c-d61e-4239-b2d4-868f557f5f76
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294146(v=EXCHG.10)
ms:contentKeyID: 32765760
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f96b73daaf446023a7fe3a5729dcb1c90b5f14e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112068"
---
# <a name="jet_tablecreate-structure"></a>JET_TABLECREATE 結構


_**適用于：** Windows |Windows Server_

## <a name="jet_tablecreate-structure"></a>JET_TABLECREATE 結構

**JET_TABLECREATE** 結構所包含的資訊，必須用來建立在 ESE 資料庫中填入資料行和索引的資料表。 [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)會使用 **JET_TABLECREATE** 結構。

```cpp
    typedef struct tagJET_TABLECREATE {
      unsigned long cbStruct;
      tchar* szTableName;
      tchar* szTemplateTableName;
      unsigned long ulPages;
      unsigned long ulDensity;
      JET_COLUMNCREATE* rgcolumncreate;
      unsigned long cColumns;
      JET_INDEXCREATE* rgindexcreate;
      unsigned long cIndexes;
      JET_GRBIT grbit;
      JET_TABLEID tableid;
      unsigned long cCreated;
    } JET_TABLECREATE;
```

### <a name="members"></a>成員

**cbStruct**

此結構的大小，以位元組為單位， (未來的擴充) 。 它必須設定為 sizeof ( JET_TABLECREATE ) （以位元組為單位）。

**szTableName**

要建立之資料表的名稱。

名稱必須使用符合下列條件：

  - 值小於 JET_cbNameMost，不包括終止的 Null。

<!-- end list -->

  - 包含下列一組字元：0到9、A 到 Z、a 到 z，以及除了驚嘆號以外的所有其他標點符號 (\!) 、逗點 (、) 、左括弧 (\[) 和右括弧 () \] ，也就是 ASCII 字元0x20、0x22 至0x2d、0x2f 至0x5a、0x5c 和0x5d 至0x7f。

<!-- end list -->

  - 不是以空格開頭。

<!-- end list -->

  - 至少包含一個非空白字元。

**szTemplateTableName**

現有資料表的名稱，要從此資料表繼承基底 DDL (資料定義語言) 。 使用範本資料表可讓您輕鬆地建立具有相同資料行和索引的多個資料表。

**ulPages**

要配置給資料表的初始資料庫頁面數目。 如果有多個資料列插入此資料表中，指定大於1的數位可以減少片段。

**ulDensity**

資料表密度（以百分比為單位）。 此數位必須是0或20到100的範圍。 傳遞0表示應該使用預設值。 預設值為80。

**rgcolumncreate**

[JET_COLUMNCREATE](./jet-columncreate-structure.md)結構的陣列，其中每一個都對應到要在新資料表中建立的資料行。

**cColumns**

**Rgcolumncreate** 中 [JET_COLUMNCREATE](./jet-columncreate-structure.md)元素的數目。

**rgindexcreate**

[JET_INDEXCREATE](./jet-indexcreate-structure.md)結構的陣列，其中每一個都對應至要在新資料表中建立的索引。

**cIndexes**

**Rgindexcreate** 中 [JET_INDEXCREATE](./jet-indexcreate-structure.md)元素的數目。

**grbit**

包含此呼叫選項的位群組，其中包含零或多個下列值。

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
<td><p>設定 JET_bitTableCreateFixedDDL 可防止資料表上的 DDL 作業 (例如) 加入或移除資料行。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableCreateTemplateTable</p></td>
<td><p>設定 JET_bitTableCreateTemplateTable 會使資料表成為範本資料表。 然後，新的資料表可將此資料表的名稱指定為其範本資料表。 設定 JET_bitTableCreateTemplateTable 意指 JET_bitTableCreateFixedDDL。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableCreateNoFixedVarColumnsInDerivedTables</p></td>
<td><p>已取代。 請勿使用。</p></td>
</tr>
</tbody>
</table>


**tableid**

如果 API 呼叫成功，則為包含新資料表之 [JET_TABLEID](./jet-tableid.md) 的輸出欄位。 如果 API 呼叫失敗，則值為未定義。

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
<td><p><strong>Unicode</strong></p></td>
<td><p>實作為 <strong>JET_TABLECREATE_W</strong> (Unicode) 和 <strong>JET_TABLECREATE_A</strong> (ANSI) 。</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>另請參閱

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetCreateTable](./jetcreatetable-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
