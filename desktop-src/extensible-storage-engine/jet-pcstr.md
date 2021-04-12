---
description: 深入瞭解： JET_PCSTR
title: JET_PCSTR
TOCTitle: JET_PCSTR
ms:assetid: 5826e6b9-5297-421f-abaa-016708bf16f6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269254(v=EXCHG.10)
ms:contentKeyID: 32765556
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
ms.openlocfilehash: 2786435822fefb56b09c3bb434612dc1fbf13f99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195341"
---
# <a name="jet_pcstr"></a>JET_PCSTR


_**適用于：** Windows |Windows Server_

## <a name="jet_pcstr"></a>JET_PCSTR

**JET_PCSTR** 資料類型包含以 null 終止的常數 **ASCII** 字串 (char \*) 。

**Windows vista： JET_PCSTR** 是在 windows vista 中引進。

```cpp
    typedef __nullterminated const char *  JET_PCSTR;
```

### <a name="data-types"></a>資料類型

JET_PCSTR

以 Null 終止的常數 ASCII 字串 (char \*) 。

### <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>用戶端</strong></p></td>
<td><p>需要 Windows Vista。</p></td>
</tr>
<tr class="even">
<td><p><strong>伺服器</strong></p></td>
<td><p>需要 Windows Server 2008。</p></td>
</tr>
<tr class="odd">
<td><p><strong>標頭</strong></p></td>
<td><p>宣告于 Esent. h 中。</p></td>
</tr>
</tbody>
</table>

