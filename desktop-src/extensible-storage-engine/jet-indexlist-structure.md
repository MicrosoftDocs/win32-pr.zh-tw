---
description: 深入瞭解： JET_INDEXLIST 結構
title: JET_INDEXLIST 結構
TOCTitle: JET_INDEXLIST Structure
ms:assetid: 0c092b48-e583-49f3-8f5e-1428a84d9265
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269185(v=EXCHG.10)
ms:contentKeyID: 32765488
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
ms.openlocfilehash: c57fda6eaea161839cdaa758c41f13749d4c5eda
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480044"
---
# <a name="jet_indexlist-structure"></a>JET_INDEXLIST 結構


_**適用于：** Windows |Windows伺服器_

## <a name="jet_indexlist-structure"></a>JET_INDEXLIST 結構

**JET_INDEXLIST** 結構包含了 [JetGetIndexInfo](./jetgetindexinfo-function.md)或 [JetGetTableIndexInfo](./jetgettableindexinfo-function.md)函數所建立之臨時表的遍歷所需的資訊。 臨時表中的每個資料列都會描述索引的資料行。

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      gned long cRecord;
      JET_COLUMNID columnidindexname;
      JET_COLUMNID columnidgrbitIndex;
      JET_COLUMNID columnidcKey;
      JET_COLUMNID columnidcEntry;
      JET_COLUMNID columnidcPage;
      JET_COLUMNID columnidcColumn;
      JET_COLUMNID columnidiColumn;
      JET_COLUMNID columnidcolumnid;
      JET_COLUMNID columnidcoltyp;
      JET_COLUMNID columnidCountry;
      JET_COLUMNID columnidLangid;
      JET_COLUMNID columnidCp;
      JET_COLUMNID columnidCollate;
      JET_COLUMNID columnidgrbitColumn;
      JET_COLUMNID columnidcolumnname;
      JET_COLUMNID columnidLCMapFlags;
    } JET_INDEXLIST;
```

### <a name="members"></a>成員

**cbStruct**

結構的大小（以位元組為單位）。 API 呼叫會更新此欄位，因此呼叫端應確定此值符合 sizeof ( JET_INDEXLIST ) 。

**tableid**

所建立之臨時表的資料表識別碼。 呼叫端必須負責關閉資料表。

**cRecord**

已建立之臨時表中的記錄數目。

**columnidindexname**

索引名稱的資料行識別碼。

此資料行是 [JET_coltypText](./jet-coltyp.md)。

**columnidgrbitIndex**

用於索引的 *grbits* 資料行識別碼。 如需有效位清單，請參閱 [JET_INDEXCREATE](./jet-indexcreate-structure.md) 。

此資料行是 [JET_coltypLong](./jet-coltyp.md)。

**columnidcKey**

索引中索引鍵數目的資料行識別碼。

此資料行是 [JET_coltypLong](./jet-coltyp.md)。

**columnidcEntry**

索引中專案數目的資料行識別碼。

此資料行是 [JET_coltypLong](./jet-coltyp.md)。

**columnidcPage**

索引所使用之頁面數目的資料行識別碼。此資料行是 [JET_coltypLong](./jet-coltyp.md)。

**columnidcColumn**

索引所跨越的資料行總數的資料行識別碼。

此資料行是 [JET_coltypLong](./jet-coltyp.md)。

**columnidiColumn**

索引中資料行數目的資料行識別碼。 如需詳細資訊，請參閱本主題的「備註」一節。

此資料行是 [JET_coltypLong](./jet-coltyp.md)。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>cIndexInfoCols<br />15</p> | <p>指定允許15個數據行。</p> | 
| <p>cColumnInfoCols<br />14</p> | <p>指定允許14個數據行。</p> | 
| <p>cObjectInfoCols<br />9</p> | <p>指定允許9個數據行。</p> | 



**columnidcolumnid**

已編制索引之資料行的資料行識別碼。如需詳細資訊，請參閱本主題的「備註」一節。 此資料行是 [JET_coltypLong](./jet-coltyp.md)。

**columnidcoltyp**

已編制索引之資料行的 coltyp 資料行識別碼。 如需詳細資訊，請參閱本主題的「備註」一節。 此資料行是 [JET_coltypLong](./jet-coltyp.md)。

**columnidCountry**

已編制索引之資料行的國家/地區代碼資料行識別碼。 國家/地區代碼已淘汰。

此資料行是 [JET_coltypShort](./jet-coltyp.md)。

**columnidLangid**

用來建立索引的語言識別項 (LCID) 的資料行識別碼。 如需詳細資訊，請參閱 [JET_INDEXCREATE](./jet-indexcreate-structure.md)。

此資料行是 [JET_coltypShort](./jet-coltyp.md)。

**columnidCp**

用來建立索引之字碼頁的資料行識別碼。 如需詳細資訊，請參閱 [JET_COLUMNCREATE](./jet-columncreate-structure.md)。

此資料行是 [JET_coltypShort](./jet-coltyp.md)。

**columnidCollate**

建立索引時所依據之定序順序的資料行識別碼。 定序順序已淘汰。

此資料行是 [JET_coltypShort](./jet-coltyp.md)。

**columnidgrbitColumn**

*Grbits* 的資料行識別碼，適用于索引中的資料行順序。

此資料行的資料可以 JET_bitKeyAscending 或 JET_bitKeyDescending 排序。 此資料行是 [JET_coltypLong](./jet-coltyp.md)。 例如，定義為 "-column1 \\ 0 + column2 \\ 0" 的索引將會有 "column1" 的 JET_bitKeyDescending，而 "column2" 的 JET_bitKeyAscending。

下列選項對此成員有效。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitKeyAscending</p> | <p>以遞增順序的索引區段。</p> | 
| <p>JET_bitKeyDescending</p> | <p>以遞減順序排序的索引區段。</p> | 



**columnidcolumnname**

資料行名稱的資料行識別碼。

此資料行是 [JET_coltypText](./jet-coltyp.md)。

**columnidLCMapFlags**

用來建立索引之旗標的資料行識別碼。 如需詳細資訊，請參閱 [JET_UNICODEINDEX](./jet-unicodeindex-structure.md)的 **dwMapFlags** 一節。

此資料行是 [JET_coltypLong](./jet-coltyp.md)。

### <a name="remarks"></a>備註

臨時表中的每個資料列都會對應至特定索引中的資料行。

例如，索引 "+ A \\ 0 + B \\ 0 + C \\ 0 + D \\ 0 + E \\ 0" 為五個以上的資料行，而且會佔用臨時表中的五個數據列。 在 columnid 資料行所識別的資料行中，這五個數據列的值都是5。 但是，每個資料列會有不同的 columnid 資料行值，範圍介於0到4之間。

特定索引中的索引鍵數目，會對應至呼叫端可以搜尋並取得完全相符的唯一值數目。 專案數目是索引符合的資料列數目。 如果索引具有唯一性條件約束，則索引鍵的數目等於專案的數目。 例如，如果資料表包含下列資訊，並且在名為 "key" 的資料行上建立索引，則會有三個索引鍵 (100、200和 500) ，但有四個專案 ( "this"、"是"、"a" 和 "example" ) 。


| <p>答案</p> | <p>進入</p> | 
|------------|--------------|
| <p>100</p> | <p>該值</p> | 
| <p>100</p> | <p>後</p> | 
| <p>200</p> | <p>以</p> | 
| <p>500</p> | <p>範例</p> | 



### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)
