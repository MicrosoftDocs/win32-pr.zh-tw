---
description: 深入瞭解： JET_COLUMNDEF 結構
title: JET_COLUMNDEF 結構
TOCTitle: JET_COLUMNDEF Structure
ms:assetid: ee1fc473-bff5-438e-98ae-247de12e76f9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294130(v=EXCHG.10)
ms:contentKeyID: 32765744
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
ms.openlocfilehash: fccf3b076b71e8923366a95810d1f3009d4fe1c4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471134"
---
# <a name="jet_columndef-structure"></a>JET_COLUMNDEF 結構


_**適用于：** Windows |Windows伺服器_

## <a name="jet_columndef-structure"></a>JET_COLUMNDEF 結構

**JET_COLUMNDEF** 結構會定義可以儲存在資料行中的資料。

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_COLUMNID columnid;
      JET_COLTYP coltyp;
      unsigned short wCountry;
      unsigned short langid;
      unsigned short cp;
      unsigned short wCollate;
      unsigned long cbMax;
      JET_GRBIT grbit;
    } JET_COLUMNDEF;
```

### <a name="members"></a>成員

**cbStruct**

結構的大小（以位元組為單位）。 它必須設定為 sizeof ( JET_COLUMNDEF) 。

**columnid**

保留的。 **columnid** 必須設定為 0 (零) 。

**coltyp**

資料行的類型 (例如，文字、二進位或數值) 。 如需詳細資訊，請參閱 [JET_COLTYP](./jet-coltyp.md)。

**wCountry**

保留的。 **wCountry** 必須設定為 0 (零) 。

**langid**

已過時。 **langid** 應該設定為 0 (零) 。

**cp**

資料行的字碼頁。 Text 資料行的唯一有效值是英文 (1252) 和 Unicode (1200) 。 值為零表示預設將會使用 (英文、1252) 。 如果資料行不是文字資料行，則字碼頁會自動設為零。

**wCollate**

保留的。 **wCollate** 必須設定為 0 (零) 。

**cbMax**

可變長度資料行的最大長度（以位元組為單位），或固定長度資料行的長度。

**grbit**

位群組，其中包含要用於此呼叫的選項，其中包含零或多個下列值。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitColumnFixed</p> | <p>將會修正此資料行。 無論資料儲存在資料行中的資料量為何，它一律會使用資料列中相同數量的空間。 JET_bitColumnFixed 不能與 JET_bitColumnTagged 一起使用。 這個位不能搭配 <strong>JET_coltypLongText</strong> 和 <strong>JET_coltypLongBinary</strong>) 的 long 值 (使用。</p> | 
| <p>JET_bitColumnTagged</p> | <p>將會標記資料行。 如果標記的資料行不包含資料，就不會佔用資料庫中的任何空間。 此位無法搭配 JET_bitColumnFixed 使用。</p> | 
| <p>JET_bitColumnNotNull</p> | <p>資料行絕對不能設定為 Null 值。</p> | 
| <p>JET_bitColumnVersion</p> | <p>此資料行是版本資料行，可指定資料列的版本。 此資料行的值從零開始，而且會針對資料列上的每個更新自動遞增。</p><p>這個位只能套用至 <strong>JET_coltypLong</strong> 資料行。 此位無法搭配 JET_bitColumnAutoincrement、JET_bitColumnEscrowUpdate 或 JET_bitColumnTagged 使用。</p> | 
| <p>JET_bitColumnAutoincrement</p> | <p>將會自動遞增資料行。 此數位是遞增的數位，而且在資料表中保證是唯一的。 不過，數位可能不是連續的。 例如，如果將五個數據列插入資料表中，「自動遞增」資料行會包含值 {1，2，6，7，8}。 這個位只能用在 <strong>JET_coltypLong</strong> 或 <strong>JET_coltypCurrency</strong>類型的資料行上。</p><p><strong>Windows 2000：</strong>在 Windows 2000 中，此位只能用於<strong>JET_coltypLong</strong>類型的資料行。</p> | 
| <p>JET_bitColumnUpdatable</p> | <p>只有對 <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>的呼叫才會有此位有效。</p> | 
| <p>JET_bitColumnTTKey</p> | <p>只有對 <a href="gg294118(v=exchg.10).md">JetOpenTable</a>的呼叫才會有此位有效。</p> | 
| <p>JET_bitColumnTTDescending</p> | <p>只有對 <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>的呼叫才會有此位有效。</p> | 
| <p>JET_bitColumnMultiValued</p> | <p>此資料行可以是多重值。 多重值資料行可以有零個、一個或多個相關聯的值。 多重值資料行中的各種值是由稱為 <strong>itagSequence</strong> 成員的數位所識別，其屬於各種結構，包括： <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>、 <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>、 <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>、 <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>和 <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>。 多重值資料行必須是標記的資料行;也就是說，它們不能是固定長度或可變長度的資料行。</p> | 
| <p>JET_bitColumnEscrowUpdate</p> | <p>指定資料行是「正在託管」更新資料行。 您可以透過 <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> 的不同會話同時更新交易的更新資料行，並將維持交易一致性。 [保管更新] 資料行也必須符合下列條件：</p><ul><li><p>只有當資料表是空的時，才可以建立「正在進行」的更新資料行。</p></li></ul><ul><li><p>「使用中」更新資料行的類型必須是 <strong>JET_coltypLong</strong>。</p></li></ul><ul><li><p>「正在進行」的更新資料行必須有預設值 (<strong>cbDefault</strong> 必須是正數) 。</p></li></ul><ul><li><p>JET_bitColumnEscrowUpdate 不能與 JET_bitColumnTagged、JET_bitColumnVersion 或 JET_bitColumnAutoincrement 一起使用。</p></li></ul> | 
| <p>JET_bitColumnUnversioned</p> | <p>將在中建立資料行，而不含版本資訊。 這表示嘗試加入具有相同名稱之資料行的其他交易將會失敗。 這個位只對 <a href="gg294122(v=exchg.10).md">JetAddColumn</a>很有用。 它不能用在交易內。</p> | 
| <p>JET_bitColumnMaybeNull</p> | <p>保留供未來使用。</p> | 
| <p>JET_bitColumnFinalize</p> | <p>使用 JET_bitColumnDeleteOnZero 而不是 JET_bitColumnFinalize。 JET_bitColumnFinalize 可以完成資料行。 當可以完成的資料行具有到達零的「保管更新」資料行時，將會刪除該資料列。 未來的版本可能會改為叫用回呼函數 (如需詳細資訊，請參閱 <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>) 。 可以完成的資料行必須是「託管更新」資料行。 JET_bitColumnFinalize 不能與 JET_bitColumnUserDefinedDefault 一起使用。</p> | 
| <p>JET_bitColumnUserDefinedDefault</p> | <p>資料行的預設值將由回呼函數提供。 請參閱 <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>。 具有使用者定義預設值的資料行必須是標記的資料行。 指定 JET_bitColumnUserDefinedDefault 表示 <strong>pvDefault</strong> 必須指向 <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> 結構，而且 <strong>cbDefault</strong> 必須設定為 sizeof ( <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> ) 。</p><ul><li><p>JET_bitColumnUserDefinedDefault 不能與 JET_bitColumnFixed、JET_bitColumnNotNull、JET_bitColumnVersion、JET_bitColumnAutoincrement、JET_bitColumnUpdatable、JET_bitColumnEscrowUpdate、JET_bitColumnFinalize、JET_bitColumnDeleteOnZero 或 JET_bitColumnMaybeNull 一起使用。</p></li></ul> | 
| <p>JET_bitColumnDeleteOnZero</p> | <p>此資料行是「正在進行的更新」資料行，當它到達零時，將會刪除記錄。 可以完成之資料行的常見用法是使用它做為參考計數位段，而且當欄位到達零時，就會刪除記錄。 JET_bitColumnDeleteOnZero 與 JET_bitColumnFinalize 相關。 零刪除資料行必須是「託管更新」資料行。 JET_bitColumnDeleteOnZero 不能與 JET_bitColumnFinalize 一起使用。 JET_bitColumnDeleteOnZero 不能與使用者定義的預設資料行一起使用。</p> | 



### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md)  
[JetAddColumn](./jetaddcolumn-function.md)  
[JetEscrowUpdate](./jetescrowupdate-function.md)  
[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)  
[JetOpenTempTable](./jetopentemptable-function.md)  
[JetOpenTempTable2](./jetopentemptable2-function.md)  
[JetOpenTempTable3](./jetopentemptable3-function.md)  
[JetRenameColumn](./jetrenamecolumn-function.md)
