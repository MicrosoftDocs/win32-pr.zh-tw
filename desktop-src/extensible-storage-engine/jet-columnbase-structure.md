---
description: 深入瞭解： JET_COLUMNBASE 結構
title: JET_COLUMNBASE 結構
TOCTitle: JET_COLUMNBASE Structure
ms:assetid: 171275c3-966d-409d-ad20-a8f240f7500d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269194(v=EXCHG.10)
ms:contentKeyID: 32765497
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
ms.openlocfilehash: 603025166eed7c92d98148a43d26046308235777
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983591"
---
# <a name="jet_columnbase-structure"></a>JET_COLUMNBASE 結構


_**適用于：** Windows |Windows伺服器_

## <a name="jet_columnbase-structure"></a>JET_COLUMNBASE 結構

**JET_COLUMNBASE** 結構描述基底資料行的參數。 [JetGetColumnInfo](./jetgetcolumninfo-function.md)和 [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)函數會使用 **JET_COLUMNBASE** 結構。

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_COLUMNID columnid;
      JET_COLTYP coltyp;
      unsigned short wCountry;
      unsigned short langid;
      unsigned short cp;
      unsigned short wFiller;
      unsigned long cbMax;
      JET_GRBIT grbit;
      tchar szBaseTableName[256];
      tchar szBaseColumnName[256];
    } JET_COLUMNBASE;
```

### <a name="members"></a>成員

**cbStruct**

此結構的大小（以位元組為單位）。 將 **cbStruct** 設定為 sizeof ( JET_COLUMNBASE ) 。

**columnid**

保留的。 將 **columnid** 設定為 0 (零) 。

**coltyp**

資料行的類型 (例如，文字、二進位或數值) 。 如需詳細資訊，請參閱 [JET_COLTYP](./jet-coltyp.md)。

**wCountry**

保留的。 設定為 0 (零) 。

**langid**

保留的。 設定為 0 (零) 。

**cp**

資料行的字碼頁。 Text 資料行的唯一有效值是英文 (1252) 和 Unicode (1200) 。 值為零表示預設將會使用 (英文、1252) 。 如果資料行不是文字資料行，則字碼頁會自動設為零。

**wFiller**

保留的。 設定為 0 (零) 。

**cbMax**

可變長度資料行的最大長度（以位元組為單位），或固定長度資料行的實際長度（以位元組為單位）。

**grbit**

包含零或多個下列值的資料行選項。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitColumnFixed</p> | <p>資料行是固定的，而且會佔用資料列中相同數量的空間，不論它包含多少資料。 JET_bitColumnFixed 無法與 JET_bitColumnTagged 合併，且當 <strong>coltyp</strong> 成員設定為 <strong>JET_coltypLongText</strong> 或 <strong>JET_coltypLongBinary</strong>時無法使用。</p> | 
| <p>JET_bitColumnTagged</p> | <p>只有當資料行包含資料時，資料行才會被標記並在資料庫中佔用空間。 JET_bitColumnTagged 無法與 JET_bitColumnFixed、JET_bitColumnVersion 或 JET_bitColumnEscrowUpdate 合併。</p> | 
| <p>JET_bitColumnNotNull</p> | <p>資料行不得設定為 <strong>Null</strong> 值。</p><p>JET_bitColumnNotNull 無法與 JET_bitColumnUserDefinedDefault 結合。</p> | 
| <p>JET_bitColumnVersion</p> | <p>此資料行是版本資料行，可指定資料列的版本。 此資料行的值從零開始，而且會針對每個資料列更新自動遞增。</p><p>只有當 <strong>coltyp</strong> 成員設定為 <strong>JET_coltypLong</strong> ，而且無法與 JET_bitColumnAutoincrement、JET_bitColumnEscrowUpdate、JET_bitColumnTagged 或 JET_bitColumnUserDefinedDefault 合併時，才可以使用 JET_bitColumnVersion。</p> | 
| <p>JET_bitColumnAutoincrement</p> | <p>資料行會自動遞增。 此數位是遞增的數位，而且在資料表中保證是唯一的。 不過，數位可能不是連續的。 例如，如果將五個數據列插入資料表中，自動遞增的資料行會包含值 {1，2，6，7，8}。</p><p>只有當 <strong>coltyp</strong> 成員設定為 <strong>JET_coltypLong</strong> 或 <strong>JET_coltypCurrency</strong> ，且不能與 JET_bitColumnEscrowUpdate、JET_bitColumnUserDefinedDefault 或 JET_bitColumnVersion 合併時，才可以使用 JET_bitColumnAutoincrement。</p><p><strong>Windows 2000：</strong>只有當<strong>coltyp</strong>成員設定為<strong>JET_coltypLong</strong>時，才可以使用 JET_bitColumnVersion。</p> | 
| <p>JET_bitColumnUpdatable</p> | <p>只對 <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>的呼叫有效。 JET_bitColumnUpdatable 無法與 JET_bitColumnUserDefinedDefault 結合。</p> | 
| <p>JET_bitColumnTTKey</p> | <p>只對 <a href="gg294118(v=exchg.10).md">JetOpenTable</a>的呼叫有效。</p> | 
| <p>JET_bitColumnTTDescending</p> | <p>只對 <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>的呼叫有效。</p> | 
| <p>JET_bitColumnMultiValued</p> | <p>此資料行可以是多重值。 多重值資料行可以有零個、一個或多個相關聯的值。 多重值資料行中的各種值是由各種結構之 <strong>itagSequence</strong> 成員中的數位所識別，例如 <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>、 <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>、 <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>、 <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a> <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>。 多重值資料行必須是標記的資料行;也就是說，它們可能不是固定長度或可變長度的資料行。</p> | 
| <p>JET_bitColumnEscrowUpdate</p> | <p>指定資料行是一種可由不同會話與 <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> 同時更新的交易式更新資料行，而且將具有交易一致性。</p><ul><li><p>只有當資料表是空的時，才可以建立「正在進行」的更新資料行。</p></li></ul><ul><li><p>若為使用中的更新資料行， <strong>coltyp</strong> 成員必須設定為 <strong>JET_coltypLong。</strong></p></li></ul><ul><li><p>「正在進行」的更新資料行必須有預設值 (<strong>cbDefault</strong> 必須是正數) 。</p></li></ul><ul><li><p>JET_bitColumnEscrowUpdate 無法與 JET_bitColumnTagged、JET_bitColumnVersion 或 JET_bitColumnAutoincrement 合併。</p></li></ul> | 
| <p>JET_bitColumnUnversioned</p> | <p>建立資料行時沒有版本號碼。 這表示嘗試加入具有相同名稱之資料行的其他交易將會失敗。 JET_bitColumnUnversioned 只能與 <a href="gg294122(v=exchg.10).md">JetAddColumn</a>搭配使用。 它不能用在交易內。</p> | 
| <p>JET_bitColumnMaybeNull</p> | <p>保留供未來使用。</p><p>JET_bitColumnMaybeNull 無法與 JET_bitColumnUserDefinedDefault 結合。</p> | 
| <p>JET_bitColumnFinalize</p> | <p>請勿使用。 請改用 JET_bitColumnDeleteOnZero。</p><p>可以完成資料行。 可以完成的資料行是一種可在資料行到達零時，會刪除資料列的「正在進行的」更新資料行。 未來的版本可能會改為叫用回呼函式 (請參閱 <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>) 。 可以完成的資料行必須是「託管更新」資料行。 JET_bitColumnFinalize 無法與 JET_bitColumnUserDefinedDefault 結合。</p> | 
| <p>JET_bitColumnUserDefinedDefault</p> | <p>資料行的預設值將由回呼函數提供。 請參閱 <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>。 具有使用者定義預設值的資料行必須是標記的資料行。 如果指定 JET_bitColumnUserDefinedDefault， <strong>pvDefault</strong> 必須指向 <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> 結構，而且 <strong>cbDefault</strong> 必須設定為 sizeof ( JET_USERDEFINEDDEFAULT ) 。</p><p>JET_bitColumnUserDefinedDefault 無法與 JET_bitColumnFixed、JET_bitColumnNotNull、JET_bitColumnVersion、JET_bitColumnAutoincrement、JET_bitColumnUpdatable、JET_bitColumnEscrowUpdate、JET_bitColumnFinalize、JET_bitColumnDeleteOnZero 或 JET_bitColumnMaybeNull 合併。</p> | 
| <p>JET_bitColumnDeleteOnZero</p> | <p>此資料行是「正在進行的更新」資料行，當它到達零時，將會刪除記錄。 零刪除資料行的常見用法是參考計數位段。 當參考的數目落為零時，就會刪除記錄。 零刪除資料行必須是「託管更新」資料行。</p><p>JET_bitColumnDeleteOnZero 取代 JET_bitColumnFinalize。</p><p>JET_bitColumnDeleteOnZero 無法與 JET_bitColumnFinalize 或 JET_bitColumnUserDefinedDefault 結合，也不能與使用者定義的預設資料行一起使用。</p> | 



**szBaseTableName**

目前資料表從中繼承其 DDL 的資料表。

**szBaseColumnName**

範本資料表中的資料行名稱。

### <a name="remarks"></a>備註

**JET_COLUMNBASE** 包含與 [JET_COLUMNDEF](./jet-columndef-structure.md)大部分相同的資訊，但它會在) 使用階層式 DDL 時，加入字串欄位來描述基表 (。

### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 
| <p><strong>Unicode</strong></p> | <p>實作為 <strong>JET_COLUMNBASE_W</strong> (Unicode) 和 <strong>JET_COLUMNBASE_A</strong> (ANSI) 。</p> | 



### <a name="see-also"></a>另請參閱

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNDEF](./jet-columndef-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md)  
[JetGetColumnInfo](./jetgetcolumninfo-function.md)  
[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)  
[JetRenameColumn](./jetrenamecolumn-function.md)
