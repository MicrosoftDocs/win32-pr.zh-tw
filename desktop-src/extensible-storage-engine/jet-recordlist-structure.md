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
ms.openlocfilehash: 16aca3a13bbae7c61bfe03aca49acea775820d39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852256"
---
# <a name="jet_recordlist-structure"></a>JET_RECORDLIST 結構


_**適用于：** Windows |Windows Server_

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
</tbody>
</table>


### <a name="see-also"></a>另請參閱

[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetIntersectIndexes](./jetintersectindexes-function.md)  
[JetRollback](./jetrollback-function.md)
