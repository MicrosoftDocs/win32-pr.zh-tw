---
description: 深入瞭解： JET_SNPROG 結構
title: JET_SNPROG 結構
TOCTitle: JET_SNPROG Structure
ms:assetid: 8b4224e4-ad4d-440f-8915-8eb43b0885f0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269328(v=EXCHG.10)
ms:contentKeyID: 32765618
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 961e9cf264652924cfb1d870fa1a04aabc7fb61a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468720"
---
# <a name="jet_snprog-structure"></a>JET_SNPROG 結構


_**適用于：** Windows |Windows Server_

## <a name="jet_snprog-structure"></a>JET_SNPROG 結構

**JET_SNPROG** 結構包含長時間執行之作業進度的相關資訊。 當呼叫回呼函式來通知作業的狀態，而且作業仍在進行時，回呼函式的最後一個參數就是 **JET_SNPROG** 結構的指標。

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cunitDone;
      unsigned long cunitTotal;
    } JET_SNPROG;
```

### <a name="members"></a>成員

**cbStruct**

**JET_SNPROG** 結構的大小（以位元組為單位）。 此值會確認下欄欄位是否存在。

**cunitDone**

長時間執行的函式期間已完成的工作單位數目。

**cunitTotal**

需要完成的工作單位數目。 此值應該一律大於或等於 **cunitDone**。

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

