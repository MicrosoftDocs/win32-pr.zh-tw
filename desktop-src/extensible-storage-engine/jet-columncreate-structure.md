---
description: 深入瞭解： JET_COLUMNCREATE 結構
title: JET_COLUMNCREATE 結構
TOCTitle: JET_COLUMNCREATE Structure
ms:assetid: 553263a9-7d2c-4bd7-ad77-1dfb6d21ef2c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269252(v=EXCHG.10)
ms:contentKeyID: 32765554
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
ms.openlocfilehash: 1b14388f26e21550319b910ac01d9ee0dde4d5890336c91e1fca76bc68cce93f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118254978"
---
# <a name="jet_columncreate-structure"></a>JET_COLUMNCREATE 結構


_**適用于：** Windows |Windows伺服器_

## <a name="jet_columncreate-structure"></a>JET_COLUMNCREATE 結構

**JET_COLUMNCREATE** 結構描述要在資料庫中建立的資料行。

```cpp
    typedef struct tag_JET_COLUMNCREATE {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_COLTYP coltyp;
      unsigned long cbMax;
      JET_GRBIT grbit;
      void* pvDefault;
      unsigned long cbDefault;
      unsigned long cp;
      JET_COLUMNID columnid;
      JET_ERR err;
    } JET_COLUMNCREATE;
```

### <a name="members"></a>成員

**cbStruct**

結構的大小（以位元組為單位）。 此欄位必須初始化為 **sizeof ( JET_COLUMNCREATE )**。

**szColumnName**

要建立之資料行的名稱。 此名稱必須符合下列準則：

  - 長度必須少於 JET_cbNameMost 個字元，不包括終止的 Null。

<!-- end list -->

  - 它必須只包含下列集合中的字元：0到9、A 到 Z、a 到 z，以及除了驚嘆號以外的所有其他標點符號 (\!) 、逗點 (、) 、左括弧 (\[) 和右括弧 () \] ，也就是 ASCII 字元0x20、0x22 至0x2d、0x2f 至0x5a、0x5c、0x5d 至0x7f。

<!-- end list -->

  - 它不能以空格開頭。

<!-- end list -->

  - 它至少必須包含一個非空白字元。

**coltyp**

資料行的類型 (例如，文字、二進位或數值) 。 如需詳細資訊，請參閱 [JET_COLTYP](./jet-coltyp.md)。

**cbMax**

可變長度資料行的最大長度（以位元組為單位）。 固定長度資料行的資料行長度。

**grbit**

位群組，其中包含此結構的選項，以及包含零或多個下列值的選項。

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
<td><p>JET_bitColumnFixed</p></td>
<td><p>此資料行是固定的。 無論資料儲存在資料行中的資料量為何，它一律會使用資料列中相同數量的空間。 JET_bitColumnFixed 不能與 JET_bitColumnTagged 一起使用。 這個位不能用在 long 值，例如 <strong>JET_coltypLongText</strong> 和 <strong>JET_coltypLongBinary</strong>。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTagged</p></td>
<td><p>資料行已標記。 如果標記的資料行不包含資料，就不會佔用資料庫中的任何空間。 此位無法搭配 JET_bitColumnFixed 使用。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnNotNull</p></td>
<td><p>資料行絕對不能設定為 Null 值。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnAutoincrement</p></td>
<td><p>資料行會自動遞增。 此數位是遞增的數位，而且在資料表中保證是唯一的。 但數位可能不是連續的。 例如，如果將五個數據列插入資料表中，自動遞增資料行可以包含值 {1，2，6，7，8}。</p>
<p><strong>Windows 2000：</strong>這個位只能用在<strong>JET_coltypLong</strong>類型的資料行上。</p>
<p><strong>Windows Server 2003 和更新版本：</strong>這個位只能用在<strong>JET_coltypLong</strong>或<strong>JET_coltypCurrency</strong>類型的資料行上。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnUpdatable</p></td>
<td><p>只有對 <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>的呼叫才會有此位有效。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnTTKey</p></td>
<td><p>只有對 <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>的呼叫才會有此位有效。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnTTDescending</p></td>
<td><p>只有對 <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>的呼叫才會有此位有效。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnMultiValued</p></td>
<td><p>此資料行可以是多重值。 多重值資料行可以有零個、一個或多個相關聯的值。 多值資料行中的各種值是由各種結構的 <strong>itagSequence</strong> 成員識別，例如 <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>、 <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>、 <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>、 <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a> <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>。 多重值資料行必須是標記的資料行;也就是說，它們不能是固定長度或可變長度的資料行。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnEscrowUpdate</p></td>
<td><p>此資料行是「正在託管」更新資料行。 交易更新資料行可以透過 <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> 的不同會話同時更新，並維持交易一致性。</p>
<ul>
<li><p>只有當資料表是空的時，才可以建立「正在進行」的更新資料行。</p></li>
<li><p>「使用中」更新資料行的類型必須是 <strong>JET_coltypLong。</strong></p></li>
<li><p>「正在進行」的更新資料行必須有預設值 (<strong>cbDefault</strong> 必須是正數) 。</p></li>
<li><p>JET_bitColumnEscrowUpdate 不能與下列常數一起使用：</p>
<ul>
<li><p>JET_bitColumnTagged</p></li>
<li><p>JET_bitColumnVersion</p></li>
<li><p>JET_bitColumnAutoincrement</p></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnUnversioned</p></td>
<td><p>建立沒有版本的資料行。 嘗試加入具有相同名稱之資料行的其他交易將會失敗。 這個位只對 <a href="gg294122(v=exchg.10).md">JetAddColumn</a>很有用。 它不能用在交易內。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnMaybeNull</p></td>
<td><p>保留供未來使用。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnFinalize</p></td>
<td><p>使用 JET_bitColumnDeleteOnZero 而不是 JET_bitColumnFinalize。 JET_bitColumnFinalize 指定可以完成資料行。 當可以完成的資料行具有到達零的「保管更新」資料行時，將會刪除該資料列。 未來的版本可以改為叫用回呼函數。 如需詳細資訊，請參閱 <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>。 可以完成的資料行必須是「託管更新」資料行。 JET_bitColumnFinalize 不能與 JET_bitColumnUserDefinedDefault 一起使用。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitColumnUserDefinedDefault</p></td>
<td><p>資料行的預設值是由回呼函數（ <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>）所提供。 具有使用者定義預設值的資料行必須是標記的資料行。 <strong>pvDefault</strong> 必須指向 <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> 結構，而且 <strong>cbDefault</strong> 必須設定為 sizeof (<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>) 。</p>
<p>JET_bitColumnUserDefinedDefault 不能與下列常數一起使用：</p>
<ul>
<li><p>JET_bitColumnFixed</p></li>
<li><p>JET_bitColumnNotNull</p></li>
<li><p>JET_bitColumnVersion</p></li>
<li><p>JET_bitColumnAutoincrement</p></li>
<li><p>JET_bitColumnUpdatable</p></li>
<li><p>JET_bitColumnEscrowUpdate</p></li>
<li><p>JET_bitColumnFinalize</p></li>
<li><p>JET_bitColumnDeleteOnZero</p></li>
<li><p>JET_bitColumnMaybeNull</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_bitColumnDeleteOnZero</p></td>
<td><p>此資料行是「正在進行的更新」資料行，當它到達零時，將會刪除記錄。 可以完成之資料行的常見用法是使用它做為參考計數位段，而且當欄位到達零時，就會刪除記錄。 JET_bitColumnDeleteOnZero 與 JET_bitColumnFinalize 相關。 零刪除資料行必須是「託管更新」資料行。 JET_bitColumnDeleteOnZero 不能與 JET_bitColumnFinalize 一起使用。 JET_bitColumnDeleteOnZero 不能與使用者定義的預設資料行一起使用。</p></td>
</tr>
</tbody>
</table>


**pvDefault**

指向緩衝區，這會是資料行的預設值。 緩衝區的長度為 **cbDefault**。 如果沒有預設值，則應該將 **pvDefault** 設定為 Null，而 **cbDefault** 應該設定為零。 如果 *grbit* 已設定 JET_bitColumnUserDefinedDefault， **pvDefault** 將會被解釋為 JET_USERDEFINEDDEFAULT 結構的指標。 預設值不能大於255個位元組。 如果預設值大於255個位元組，則會以無訊息模式截斷。

**cbDefault**

**PvDefault** 所指定的緩衝區大小（以位元組為單位）。

**cp**

資料行的字碼頁。 Text 資料行的唯一有效值是英文 (1252) 和 Unicode (1200) 。 值為零表示預設將會使用 (英文、1252) 。 如果資料行不是文字資料行，則字碼頁會自動設為零。

**columnid**

成功時，會在此欄位中傳回新建立之資料行的資料行識別碼。 失敗時，值為未定義。

**犯 錯**

**Err** 欄位將包含建立此資料行的狀態。 如需可能傳回值的清單，請參閱 [JetAddColumn](./jetaddcolumn-function.md) 。

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>實作為 <strong>JET_COLUMNCREATE_W</strong> (Unicode) 和 <strong>JET_COLUMNCREATE_A</strong> (ANSI) 。</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>另請參閱

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_RETINFO](./jet-retinfo-structure.md)  
[JET_SETINFO](./jet-setinfo-structure.md)  
[JET_SETCOLUMN](./jet-setcolumn-structure.md)  
[JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)  
[JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)  
[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)  
[JetEscrowUpdate](./jetescrowupdate-function.md)  
[JetRenameColumn](./jetrenamecolumn-function.md)  
[JetSetColumns](./jetsetcolumns-function.md)
