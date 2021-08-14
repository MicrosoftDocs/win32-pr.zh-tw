---
description: 深入瞭解： JET_PCWSTR
title: JET_PCWSTR
TOCTitle: JET_PCWSTR
ms:assetid: fef64bb9-c2e0-4cfb-8138-c98ae6f50952
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294145(v=EXCHG.10)
ms:contentKeyID: 32765759
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
ms.openlocfilehash: 3958baa23228bdf32807cc4fdc07a471e625d553f57672e318a062038923b5af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119473888"
---
# <a name="jet_pcwstr"></a>JET_PCWSTR


_**適用于：** Windows |Windows伺服器_

## <a name="jet_pcwstr"></a>JET_PCWSTR

**JET_PCWSTR** 資料類型包含以 null 終止的常數 **Unicode** 字串 (char \*) 。

**Windows vista： JET_PCWSTR** 是在 Windows vista 中引進。

```cpp
    typedef __nullterminated const WCHAR * JET_PCWSTR;
```

### <a name="data-types"></a>資料類型

JET_PCWSTR

以 Null 終止的常數 Unicode 字串 (char \*) 。

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

