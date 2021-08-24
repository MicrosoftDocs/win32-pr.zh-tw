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
ms.openlocfilehash: 48e9da5822f69d4460a1699252112899a990188d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470874"
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


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitRecordInIndex</p> | <p>指定索引範圍應正常處理。</p> | 
| <p>JET_bitRecordNotInIndex</p> | <p>保留供未來使用。 請勿使用。</p> | 



### <a name="remarks"></a>備註

傳遞至 [JetIntersectIndexes](./jetintersectindexes-function.md)的每個 **JET_INDEXRANGE** 結構代表一個索引範圍，此範圍將由 API 呼叫來交集。 **JET_INDEXRANGE** 中提供的資料指標必須已經設定有效的索引範圍，且成功呼叫 [JetSetIndexRange](./jetsetindexrange-function.md)。

### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetIntersectIndexes](./jetintersectindexes-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
