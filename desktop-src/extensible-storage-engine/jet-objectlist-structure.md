---
description: 深入瞭解： JET_OBJECTLIST 結構
title: JET_OBJECTLIST 結構
TOCTitle: JET_OBJECTLIST Structure
ms:assetid: 95f12f2a-13da-48d4-a254-fc0cb718b17d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269348(v=EXCHG.10)
ms:contentKeyID: 32765635
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 21a3ea030421406a5bc571bb5cc1887f77b4710d
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983121"
---
# <a name="jet_objectlist-structure"></a>JET_OBJECTLIST 結構


_**適用于：** Windows |Windows伺服器_

## <a name="jet_objectlist-structure"></a>JET_OBJECTLIST 結構

**JET_OBJECTLIST** 結構會遍歷以 [JetGetObjectInfo](./jetgetobjectinfo-function.md)建立的臨時表。 臨時表中的每個資料列都會描述資料庫中的物件。

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidcontainername;
      JET_COLUMNID columnidobjectname;
      JET_COLUMNID columnidobjtyp;
      JET_COLUMNID columniddtCreate;
      JET_COLUMNID columniddtUpdate;
      JET_COLUMNID columnidgrbit;
      JET_COLUMNID columnidflags;
      JET_COLUMNID columnidcRecord;
      JET_COLUMNID columnidcPage;
    } JET_OBJECTLIST;
```

### <a name="members"></a>成員

**cbStruct**

結構的大小（以位元組為單位）。 API 呼叫會更新此欄位，因此呼叫端應確定此值符合 sizeof ( JET_INDEXLIST ) 。

**tableid**

所建立之臨時表的資料表識別碼。 呼叫端必須包含將關閉資料表的程式碼。

**cRecord**

已建立之臨時表中的記錄數目。

**columnidcontainername**

容器型別名稱的資料行識別碼。

目前唯一支援的容器是資料表。 此資料行是 [JET_coltypText](./jet-coltyp.md)。

**columnidobjectname**

物件名稱的資料行識別碼。

此資料行是 [JET_coltypText](./jet-coltyp.md)。

**columnidobjtyp**

物件之類型的資料行識別碼。 目前唯一支援的容器是資料表，因此此欄位將會 JET_objtypTable。

此資料行是 [JET_coltypLong](./jet-coltyp.md)。

**columniddtCreate**

已過時。 請勿使用。

**columniddtUpdate**

已過時。 請勿使用。

**columnidgrbit**

適用于物件之 **grbits** 的資料行識別碼。 如需適用 **grbits** 的清單，請參閱 [JET_TABLECREATE](./jet-tablecreate-structure.md)。

此資料行是 [JET_coltypLong](./jet-coltyp.md)。

**columnidflags**

適用于物件之旗標的資料行識別碼。 如需適用旗標的清單，請參閱 [JET_OBJECTINFO](./jet-objectinfo-structure.md)。

此資料行是 [JET_coltypLong](./jet-coltyp.md)。

**columnidcRecord**

存在於資料表中，以 **columnidobjectname** 命名的記錄數目的資料行識別碼。

此資料行是 [JET_coltypLong](./jet-coltyp.md)。

**columnidcPage**

物件所使用之頁面數目的資料行識別碼。

此資料行是 [JET_coltypLong](./jet-coltyp.md)。

### <a name="remarks"></a>備註

臨時表中的每個資料列都會對應至資料庫中的物件。

當使用 [JetGetObjectInfo](./jetgetobjectinfo-function.md)函數中的 *InfoLevel* 參數來建立臨時表時，設定為 JET_ObjInfoListNoStats 時， **columnidcRecord** 和 **columnidcPage** 所識別的資料行將不會包含有意義的資訊。

目前，只有資料表的相關資訊會在臨時表中。

### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JetGetObjectInfo](./jetgetobjectinfo-function.md)
