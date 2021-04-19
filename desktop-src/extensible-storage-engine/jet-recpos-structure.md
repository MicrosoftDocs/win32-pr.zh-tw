---
description: 深入瞭解： JET_RECPOS 結構
title: JET_RECPOS 結構
TOCTitle: JET_RECPOS Structure
ms:assetid: 7c335120-4b84-4095-8f13-e5315d4996b1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269308(v=EXCHG.10)
ms:contentKeyID: 32765598
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
ms.openlocfilehash: e24e16aaac4228f35350f55f57a14f2820add0cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990344"
---
# <a name="jet_recpos-structure"></a>JET_RECPOS 結構


_**適用于：** Windows |Windows Server_

## <a name="jet_recpos-structure"></a>JET_RECPOS 結構

**JET_RECPOS** 結構包含整數的集合，代表索引中的小數位置。 **centriesLT** 是小於目前索引鍵的索引項目數目。 **centriesInRange** 是等於目前索引鍵的索引項目數目。 **centriesInRange** 不受支援，而且一律會傳回為1。 **centriesTotal** 是索引中的索引項目數目。 所有值都是近似值，無法保證精確度。

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long centriesLT;
      unsigned long centriesInRange;
      unsigned long centriesTotal;
    } JET_RECPOS;
```

### <a name="members"></a>成員

**cbStruct**

[JET_RETINFO](./jet-retinfo-structure.md)結構的大小（以位元組為單位）。 此值會確認下欄欄位是否存在。

**centriesLT**

索引項目的近似數目小於目前的索引鍵。

**centriesInRange**

索引項目目的大約數目等於目前的索引鍵。 無論實際等於目前索引鍵的索引項目數目為何，這個欄位一律會設定為1。

**centriesTotal**

索引中的大約專案數。

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

[JET_RETINFO](./jet-retinfo-structure.md)  
[JetGetRecordPosition](./jetgetrecordposition-function.md)
