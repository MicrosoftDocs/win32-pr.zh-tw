---
description: 深入瞭解： JET_COLUMNLIST 結構
title: JET_COLUMNLIST 結構
TOCTitle: JET_COLUMNLIST Structure
ms:assetid: 3899676f-c96e-4f15-9089-4faea6808bc2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269228(v=EXCHG.10)
ms:contentKeyID: 32765530
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
ms.openlocfilehash: 6b7f874c95352ce29954adf46b1682dec89c7a9a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471794"
---
# <a name="jet_columnlist-structure"></a>JET_COLUMNLIST 結構


_**適用于：** Windows |Windows伺服器_

## <a name="jet_columnlist-structure"></a>JET_COLUMNLIST 結構

**JET_COLUMNLIST** 結構包含了遍歷 [JetGetColumnInfo](./jetgetcolumninfo-function.md)和 [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)函數所建立之臨時表所需的資訊。 臨時表中的每個資料列都會描述 API 呼叫中所指定資料表中的資料行。 此結構只搭配 [JetGetColumnInfo](./jetgetcolumninfo-function.md) 和 [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)使用。

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidPresentationOrder;
      JET_COLUMNID columnidcolumnname;
      JET_COLUMNID columnidcolumnid;
      JET_COLUMNID columnidcoltyp;
      JET_COLUMNID columnidCountry;
      JET_COLUMNID columnidLangid;
      JET_COLUMNID columnidCp;
      JET_COLUMNID columnidCollate;
      JET_COLUMNID columnidcbMax;
      JET_COLUMNID columnidgrbit;
      JET_COLUMNID columnidDefault;
      JET_COLUMNID columnidBaseTableName;
      JET_COLUMNID columnidBaseColumnName;
      JET_COLUMNID columnidDefinitionName;
    } JET_COLUMNLIST;
```

### <a name="members"></a>成員

**cbStruct**

結構的大小（以位元組為單位）。 API 呼叫會更新此欄位，因此呼叫端應確定此值符合 sizeof ( JET_COLUMNLIST ) 。

**tableid**

所建立之臨時表的資料表識別碼。 呼叫端必須負責關閉資料表。

**cRecord**

API 呼叫所建立之臨時表中的記錄數目。

**columnidPresentationOrder**

展示順序的資料行識別碼。

展示順序是用來排序臨時表的資料列。 展示順序是固定的 [JET_coltypLong](./jet-coltyp.md)。 如果指定的資訊層級不是精簡層級，則它也會標示為 JET_bitColumnTTKey。

**columnidcolumnname**

資料行名稱的資料行識別碼。

如果指定的資訊層級不是 compact，則它也會標示為 JET_bitColumnTTKey。

**columnidcolumnid**

資料行識別碼的資料行識別碼。

資料行識別碼是固定的 [JET_coltypLong](./jet-coltyp.md)。

**columnidcoltyp**

資料行類型的資料行識別碼。

資料行類型是固定的 [JET_coltypLong](./jet-coltyp.md)。

**columnidCountry**

國家/地區代碼的資料行識別碼。

國家/地區代碼是固定的 [JET_coltypShort](./jet-coltyp.md)。

**columnidLangid**

語言識別項的資料行識別碼。

語言識別項是固定的 [JET_coltypShort](./jet-coltyp.md)。

**columnidCp**

字碼頁的資料行識別碼。

字碼頁是固定的 [JET_coltypShort](./jet-coltyp.md)。

**columnidCollate**

定序順序的資料行識別碼。

定序順序是固定的 [JET_coltypShort](./jet-coltyp.md)。

**columnidcbMax**

**CbMax** 欄位的資料行識別碼。

**CbMax** 是固定的 [JET_coltypLong](./jet-coltyp.md)。

**columnidgrbit**

資料行之 *grbits* 的資料行識別碼。 *Grbit* 欄位是固定的 [JET_coltypLong](./jet-coltyp.md)。 如需這些位的詳細資訊，請參閱 [JET_COLUMNDEF](./jet-columndef-structure.md)。

以下是 **columnidgrbit** 的可能值：

JET_bitColumnTagged

JET_bitColumnFixed

JET_bitColumnUpdatable

JET_bitColumnNotNull

JET_bitColumnAutoincrement

JET_bitColumnVersion

JET_bitColumnMultiValued

JET_bitColumnEscrowUpdate

JET_bitColumnFinalize

JET_bitColumnDeleteOnZero

JET_bitColumnUserDefinedDefault

**columnidDefault**

資料行預設值的資料行識別碼。

預設值為 [JET_coltypLongBinary](./jet-coltyp.md)。

**columnidBaseTableName**

從中衍生資料表之資料表名稱的資料行識別碼。

資料表名稱是 [JET_coltypText](./jet-coltyp.md)。

**columnidBaseColumnName**

從中衍生資料行之資料行名稱的資料行識別碼。

資料行名稱是 [JET_coltypText](./jet-coltyp.md)。

**columnidDefinitionName**

資料行定義的名稱資料行識別碼。

資料行定義名稱是 [JET_coltypText](./jet-coltyp.md)。

### <a name="remarks"></a>備註

依預設，臨時表中的資料列順序會依資料行的名稱排序。 也可以依資料行識別碼進行排序。 如需如何依資料行識別碼排序的詳細資訊，請參閱 [JetGetColumnInfo](./jetgetcolumninfo-function.md) 和 [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)。

對 [JetGetColumnInfo](./jetgetcolumninfo-function.md) 或 [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) 的呼叫可能會指定精簡形式的結果。 如果有任何資料行已從範本資料表繼承，壓縮結果將不會儲存它們。

### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JET_COLTYP](./jet-coltyp.md)

[JET_COLUMNDEF](./jet-columndef-structure.md)

[JET_COLUMNID](./jet-columnid.md)

[JET_ERR](./jet-err.md)

[JET_GRBIT](./jet-grbit.md)

[JET_SESID](./jet-sesid.md)

[JET_TABLEID](./jet-tableid.md)

[JetGetColumnInfo](./jetgetcolumninfo-function.md)

[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)
