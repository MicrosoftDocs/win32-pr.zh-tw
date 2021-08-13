---
description: 深入瞭解： JET_OSSNAPID
title: JET_OSSNAPID
TOCTitle: JET_OSSNAPID
ms:assetid: 89b15492-674a-46e4-8aea-991df4f22a6f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269325(v=EXCHG.10)
ms:contentKeyID: 32765615
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
ms.openlocfilehash: 2dac261072ac9a5ce5a845ff046628cf348cd5815c34e16fccb575c2c0da3095
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118765074"
---
# <a name="jet_ossnapid"></a>JET_OSSNAPID


_**適用于：** Windows |Windows伺服器_

## <a name="jet_ossnapid"></a>JET_OSSNAPID

**JET_OSSNAPID** 資料類型包含資料庫快照集的控制碼。

```cpp
    typedef JET_API_PTR JET_OSSNAPID;
```

### <a name="data-types"></a>資料類型

JET_OSSNAPID

資料庫快照集的控制碼。 此控制碼用於與快照集備份相關的 JET API 元素中。

**Null** 可以用來表示不正確控制碼。

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

