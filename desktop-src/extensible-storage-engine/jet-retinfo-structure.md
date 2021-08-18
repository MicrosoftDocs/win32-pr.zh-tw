---
description: 深入瞭解： JET_RETINFO 結構
title: JET_RETINFO 結構
TOCTitle: JET_RETINFO Structure
ms:assetid: a47a7902-3ecd-4d42-941f-89d25d78eb4c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294049(v=EXCHG.10)
ms:contentKeyID: 32765648
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
ms.openlocfilehash: a04ee087f036bf0d6a9e0bb4c9c558dbfe3ae5a8fc8e875973ef2930e7ba911a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038726"
---
# <a name="jet_retinfo-structure"></a>JET_RETINFO 結構


_**適用于：** Windows |Windows伺服器_

## <a name="jet_retinfo-structure"></a>JET_RETINFO 結構

**JET_RETINFO** 結構包含 [JetRetrieveColumn](./jetretrievecolumn-function.md)的選擇性輸入和輸出參數。 如果要傳遞此結構的指標，則可以傳遞 null 指標。 傳遞 null **指標和傳遞** **JET_RETINFO** 設定為 sizeof (JET_RETINFO) ， **ibLongValue** 設定為 0 (零) ， **itagSequence** 設定為1。

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_COLUMNID columnidNextTagged;
    } JET_RETINFO;
```

### <a name="members"></a>成員

**cbStruct**

必須設定為 **JET_RETINFO** 結構的大小（以位元組為單位），而且可以用來確認下欄欄位是否存在。

**ibLongValue**

從 [JET_coltypLongBinary](./jet-coltyp.md)或 [JET_coltypLongText](./jet-coltyp.md)類型的資料行抓取的第一個位元組位移。 請注意，從這個位移取出的資料量是輸出緩衝區大小的下限，以及此位移之後的實際值中的資料大小。

**itagSequence**

描述多重值資料行中值的序號。 請注意，值的陣列是以一為基礎。 第一個值是 sequence 1，不是0。 如果 [記錄] 資料行只有一個值，則應將1傳遞為 **itagSequence**

使用可包含多個值的資料行時，您只能在 [JetSetColumn](./jetsetcolumn-function.md) 和 [JetRetrieveColumn](./jetretrievecolumn-function.md) 中使用大於1的序號，或使用 [JetSetColumn](./jetsetcolumn-function.md)中的0。 在目前的引擎執行中，使用 JET_bitColumnTagged 建立的任何資料行都可以包含多個值。 使用 JET_bitColumnMultiValued 所建立的資料行，與多值標記的資料行的索引編制方式不同。 如需詳細資訊，請參閱 [JET_INDEXCREATE](./jet-indexcreate-structure.md) 。

**columnidNextTagged**

藉由將0傳遞為 [JetRetrieveColumn](./jetretrievecolumn-function.md)的 columnid，來抓取所有標記的資料行時，傳回已標記、多重值或稀疏資料行的 columnid。

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

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_RETINFO]()  
[JetRetrieveColumn](./jetretrievecolumn-function.md)
