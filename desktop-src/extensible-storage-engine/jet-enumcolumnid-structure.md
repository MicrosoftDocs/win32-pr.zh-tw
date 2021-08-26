---
description: 深入瞭解： JET_ENUMCOLUMNID 結構
title: JET_ENUMCOLUMNID 結構
TOCTitle: JET_ENUMCOLUMNID Structure
ms:assetid: 5480ebf1-4fc9-49b5-bbb3-12542b86c8f1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269251(v=EXCHG.10)
ms:contentKeyID: 32765553
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
ms.openlocfilehash: 21f28e160f1c31dac909e02bf64acba0ae230305
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479641"
---
# <a name="jet_enumcolumnid-structure"></a>JET_ENUMCOLUMNID 結構


_**適用于：** Windows |Windows伺服器_

## <a name="jet_enumcolumnid-structure"></a>JET_ENUMCOLUMNID 結構

當使用 [JetEnumerateColumns](./jetenumeratecolumns-function.md)函式時， **JET_ENUMCOLUMNID** 結構會列舉一組特定的資料行，並選擇性地列舉這些資料行的一組特定的多個值。 [JetEnumerateColumns](./jetenumeratecolumns-function.md) 會傳回 **JET_ENUMCOLUMNID** 結構的陣列。

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      unsigned long ctagSequence;
      unsigned long* rgtagSequence;
    } JET_ENUMCOLUMNID;
```

### <a name="members"></a>成員

**columnid**

要列舉的資料行識別碼。

如果資料行識別碼為 0 (零) 則會略過此資料行的列舉，而 [JET_ENUMCOLUMN](./jet-enumcolumn-structure.md) 結構輸出陣列中的對應位置將會產生 JET_wrnColumnSkipped 的資料行狀態。

**ctagSequence**

選擇性地識別資料行值的陣列，此陣列 (由一) 的索引，以列舉指定的資料行識別碼。

如果 **ctagSequence** 為 0 (零) 則會忽略 **rgtagSequence** ，並且會列舉指定之資料行識別碼的所有資料行值。

如果 **rgtagSequence** 的元素為 0 (零) ，則會略過以一個索引)  (的該資料行值的列舉。 **JET_ENUMCOLUMNID** 結構之輸出陣列中的對應位置將會產生 JET_wrnColumnSkipped 的資料行狀態值。

**rgtagSequence**

給定資料行的資料行值陣列中，以一個為基底的索引陣列。 單一元素是 [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)中定義的 **itagSequence** 。 **ItagSequence** 0 (零) 表示「略過」。 1的 **itagSequence** 表示會傳回資料行的第一個資料行值，2表示第二個數據行的值，依此類推。

### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JET_COLUMNID](./jet-columnid.md)  
[JET_ENUMCOLUMN](./jet-enumcolumn-structure.md)  
[JET_ENUMCOLUMNID]()  
[JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)  
[JetEnumerateColumns](./jetenumeratecolumns-function.md)
