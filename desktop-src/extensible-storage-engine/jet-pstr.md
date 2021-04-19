---
description: 深入瞭解： JET_PSTR
title: JET_PSTR
TOCTitle: JET_PSTR
ms:assetid: acb1143f-a5ee-4088-9f05-cc2aeef23442
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294056(v=EXCHG.10)
ms:contentKeyID: 32765667
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
ms.openlocfilehash: 6bbed2cad9f9c7816d010a429b1db8eb5306fc1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980644"
---
# <a name="jet_pstr"></a>JET_PSTR


_**適用于：** Windows |Windows Server_

## <a name="jet_pstr"></a>JET_PSTR

JET_PSTR 資料類型包含以 null 終止的 ASCII 字串 (char \*) 。

**Windows vista： JET_PSTR** 是在 windows vista 中引進。

```cpp
    typedef __nullterminated char *  JET_PSTR;
```

### <a name="data-types"></a>資料類型

JET_PSTR

以 Null 終止的 ASCII 字串 (char \*) 。

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

