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
ms.openlocfilehash: dacaff181b40af870bd01bf9d287683c3d3d63a6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469475"
---
# <a name="jet_conditionalcolumn-structure"></a>JET_CONDITIONALCOLUMN 結構


_**適用于：** Windows |Windows伺服器_

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


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitIndexColumnMustBeNull</p> | <p><em>SzColumnName</em>參數所指定的資料行必須是 Null，指定資料列的索引項目才會出現在此索引中。</p> | 
| <p>JET_bitIndexColumnMustBeNonNull</p> | <p><em>SzColumnName</em>參數所指定的資料行必須是索引項目的非 Null，才能讓指定的資料列出現在此索引中。</p> | 



### <a name="remarks"></a>備註

條件式索引僅包含符合指定條件之資料列的索引項目目。 例如，資料行可以命名為「標記」，而當資料列被標記時，資料行會設定為非 Null 值。 這個資料行上的 JET_bitIndexColumnMustBeNonNull 條件式索引會顯示所有標記的資料列，而 JET_bitIndexColumnMustBeNull 的條件索引會顯示未標記的資料列。 這也是執行旗標刪除和垃圾收集索引的便利方式。

### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>Unicode</strong></p> | <p>實作為 <strong>JET_CONDITIONALCOLUMN_W</strong> (Unicode) 和 <strong>JET_CONDITIONALCOLUMN_A</strong> (ANSI) 。</p> | 



### <a name="see-also"></a>另請參閱

[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)
