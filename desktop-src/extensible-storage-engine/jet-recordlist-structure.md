---
description: 深入瞭解： JET_RECORDLIST 結構
title: JET_RECORDLIST 結構
TOCTitle: JET_RECORDLIST Structure
ms:assetid: 6b4d97a0-4b42-4f7c-bb18-b6db3c92668a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269287(v=EXCHG.10)
ms:contentKeyID: 32765579
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
ms.openlocfilehash: 983a0d6a73d4a3bb5e44095f46cc52d537ce15f3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465095"
---
# <a name="jet_recordlist-structure"></a>JET_RECORDLIST 結構


_**適用于：** Windows |Windows伺服器_

## <a name="jet_recordlist-structure"></a>JET_RECORDLIST 結構

**JET_RECORDLIST** 結構會在與 [JetIntersectIndexes](./jetintersectindexes-function.md)函數搭配使用時，尋找位於指定索引範圍交集內的記錄。

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidBookmark;
    } JET_RECORDLIST;
```

### <a name="members"></a>成員

**cbStruct**

**JET_RECORDLIST** 結構的大小（以位元組為單位）。

**tableid**

臨時表的資料表識別碼，包含查詢結果的書簽。 如果使用 [JetRollback](./jetrollback-function.md)復原目前的交易，則會自動關閉資料表;否則，必須使用 [JetCloseTable](./jetclosetable-function.md)來關閉它。

**cRecord**

臨時表中的資料列數目。

**columnidBookmark**

臨時表中書簽資料行的資料行識別碼。

### <a name="remarks"></a>備註

**Tableid** 所識別的臨時表具有單一資料行。 該單一資料行包含書簽，而且每一筆記錄都應符合 JET_cbBookmarkMost 位元組大小的緩衝區。

### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetIntersectIndexes](./jetintersectindexes-function.md)  
[JetRollback](./jetrollback-function.md)
