---
description: 深入瞭解： JET_SETINFO 結構
title: JET_SETINFO 結構
TOCTitle: JET_SETINFO Structure
ms:assetid: cbc41175-e48f-46b0-aeb1-1120fa2cd981
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294090(v=EXCHG.10)
ms:contentKeyID: 32765705
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
ms.openlocfilehash: 69602aad89142d9f5dc202074ca54cf278767892
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104514737"
---
# <a name="jet_setinfo-structure"></a>JET_SETINFO 結構


_**適用于：** Windows |Windows Server_

## <a name="jet_setinfo-structure"></a>JET_SETINFO 結構

**JET_SETINFO** 結構包含 [JetSetColumn](./jetsetcolumn-function.md)的選擇性輸入參數。 如果要傳遞此結構的指標，則可以傳遞 **Null** 指標。 傳遞 **Null** 的意義等同于傳遞 **JET_SETINFO** ，並將 **cbStruct** 設定為 Sizeof (JET_SETINFO) ，將 **ibLongValue** 設定為 0 (零) ， **itagSequence** 設定為1。

```cpp
typedef struct {
  unsigned long cbStruct;
  unsigned long ibLongValue;
  unsigned long itagSequence;
} JET_SETINFO;
```

### <a name="members"></a>成員

**cbStruct**

**JET_SETINFO** 的大小（以位元組為單位）。 此值會確認下欄欄位是否存在。

**ibLongValue**

要在類型 [JET_coltypLongBinary](./jet-coltyp.md) 或 [JET_coltypLongText](./jet-coltyp.md)的資料行中設定之第一個位元組的位移。

**itagSequence**

描述要設定之多重值資料行中的值順序。 值的陣列是以一為基礎。 第一個值是 sequence 1，而不是 0 (零) 。 如果 [記錄] 資料行只有一個值，則如果要取代該值，則應將1當作 **itagSequence** 傳遞。 值為 0 (零) 表示將新的資料行值實例加入至資料行值序列的結尾。

使用可包含多個值的資料行時，您只能在 [JetSetColumn](./jetsetcolumn-function.md) 和 [JetRetrieveColumn](./jetretrievecolumn-function.md) 中使用大於1的序號，或使用 [JetSetColumn](./jetsetcolumn-function.md)中的0。 在目前的引擎執行中，使用 JET_bitColumnTagged 建立的任何資料行都可以包含多個值。 使用 JET_bitColumnMultiValued 所建立的資料行，與多值標記的資料行的索引編制方式不同。 如需詳細資訊，請參閱 [JET_INDEXCREATE](./jet-indexcreate-structure.md) 。

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

[JetSetColumn](./jetsetcolumn-function.md)
