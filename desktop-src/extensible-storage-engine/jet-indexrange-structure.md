---
description: 深入瞭解： JET_INDEXRANGE 結構
title: JET_INDEXRANGE 結構
TOCTitle: JET_INDEXRANGE Structure
ms:assetid: 8e437f7d-1e21-4a0b-a5a5-1c78235a4f80
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269335(v=EXCHG.10)
ms:contentKeyID: 32765624
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
ms.openlocfilehash: b5b68e7ebf6df39757ab39947201b945e35a3ece85518a3cb202525033cdd214
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118485596"
---
# <a name="jet_indexrange-structure"></a>JET_INDEXRANGE 結構


_**適用于：** Windows |Windows伺服器_

## <a name="jet_indexrange-structure"></a>JET_INDEXRANGE 結構

使用 [JetIntersectIndexes](./jetintersectindexes-function.md)函式時， **JET_INDEXRANGE** 結構會識別索引範圍。

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      JET_GRBIT grbit;
    } JET_INDEXRANGE;
```

### <a name="members"></a>成員

**cbStruct**

**JET_INDEXRANGE** 的大小（以位元組為單位）。

**tableid**

先前已有索引範圍設定為 [JetSetIndexRange](./jetsetindexrange-function.md)的資料指標。

**grbit**

僅由下列其中一項組成的位元遮罩。

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
<td><p>JET_bitRecordInIndex</p></td>
<td><p>指定索引範圍應正常處理。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRecordNotInIndex</p></td>
<td><p>保留供未來使用。 請勿使用。</p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a>備註

傳遞至 [JetIntersectIndexes](./jetintersectindexes-function.md)的每個 **JET_INDEXRANGE** 結構代表一個索引範圍，此範圍將由 API 呼叫來交集。 **JET_INDEXRANGE** 中提供的資料指標必須已經設定有效的索引範圍，且成功呼叫 [JetSetIndexRange](./jetsetindexrange-function.md)。

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
<td><p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p></td>
</tr>
<tr class="odd">
<td><p><strong>標頭</strong></p></td>
<td><p>宣告于 Esent. h 中。</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>另請參閱

[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetIntersectIndexes](./jetintersectindexes-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
