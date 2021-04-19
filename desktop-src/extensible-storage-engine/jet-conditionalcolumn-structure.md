---
description: 深入瞭解： JET_CONDITIONALCOLUMN 結構
title: JET_CONDITIONALCOLUMN 結構
TOCTitle: JET_CONDITIONALCOLUMN Structure
ms:assetid: 2ca6b4ba-0dc4-47d5-b072-324e5a381d0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269214(v=EXCHG.10)
ms:contentKeyID: 32765517
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
ms.openlocfilehash: 27d0add64adeb7b609e84d6102a06230df55ebbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979015"
---
# <a name="jet_conditionalcolumn-structure"></a>JET_CONDITIONALCOLUMN 結構


_**適用于：** Windows |Windows Server_

## <a name="jet_conditionalcolumn-structure"></a>JET_CONDITIONALCOLUMN 結構

**JET_CONDITIONALCOLUMN** 結構定義如何針對指定的索引執行條件式索引編制。 條件式索引僅包含符合指定條件之資料列的索引項目目。 不過，條件資料行不是索引索引鍵的一部分，而只會控制索引項目是否存在。

```cpp
    typedef struct tagJET_CONDITIONALCOLUMN {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_GRBIT grbit;
    } JET_CONDITIONALCOLUMN;
```

### <a name="members"></a>成員

**cbStruct**

此欄位必須初始化為 sizeof ( JET_CONDITIONALCOLUMN ) （以位元組為單位）。

**szColumnName**

資料行的名稱，此資料行包含資料庫引擎有條件地索引資料列的資料。

**grbit** 提供條件式索引選項的位群組。 傳入零或邏輯 **或** ed 值對於 **JET_CONDITIONALCOLUMN** 無效。 位欄位必須是下列其中一項：

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
<td><p>JET_bitIndexColumnMustBeNull</p></td>
<td><p><em>SzColumnName</em>參數所指定的資料行必須是 Null，指定資料列的索引項目才會出現在此索引中。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexColumnMustBeNonNull</p></td>
<td><p><em>SzColumnName</em>參數所指定的資料行必須是索引項目的非 Null，才能讓指定的資料列出現在此索引中。</p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a>備註

條件式索引僅包含符合指定條件之資料列的索引項目目。 例如，資料行可以命名為「標記」，而當資料列被標記時，資料行會設定為非 Null 值。 這個資料行上的 JET_bitIndexColumnMustBeNonNull 條件式索引會顯示所有標記的資料列，而 JET_bitIndexColumnMustBeNull 的條件索引會顯示未標記的資料列。 這也是執行旗標刪除和垃圾收集索引的便利方式。

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
<td><p>實作為 <strong>JET_CONDITIONALCOLUMN_W</strong> (Unicode) 和 <strong>JET_CONDITIONALCOLUMN_A</strong> (ANSI) 。</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>另請參閱

[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)
