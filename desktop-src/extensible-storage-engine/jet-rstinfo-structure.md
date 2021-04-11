---
description: 深入瞭解： JET_RSTINFO 結構
title: JET_RSTINFO 結構
TOCTitle: JET_RSTINFO Structure
ms:assetid: 2f144d68-dcd9-4d0d-9d9e-a7d2a5c350fe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269216(v=EXCHG.10)
ms:contentKeyID: 32765519
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
ms.openlocfilehash: 3a776c84d89dfc97272c65bb0c0684faba814fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112549"
---
# <a name="jet_rstinfo-structure"></a>JET_RSTINFO 結構


_**適用于：** Windows |Windows Server_

## <a name="jet_rstinfo-structure"></a>JET_RSTINFO 結構

**JET_RSTINFO** 結構包含復原程式的控制資訊，例如資料庫重新配置資訊，以及控制停止復原的能力。

**Windows Vista：** 在 Windows Vista 中引進 **JET_RSTINFO** 結構。

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_RSTMAP* rgrstmap;
      long crstmap;
      JET_LGPOS lgposStop;
      JET_LOGTIME logtimeStop;
      JET_PFNSTATUS pfnStatus;
    } JET_RSTINFO;
```

### <a name="members"></a>成員

**cbStruct**

結構的大小。

**rgrstmap**

結構，描述已還原資料庫的舊路徑和新路徑。

**crstmap**

Rgrstmap 中的陣列專案計數。

**lgposStop**

停止復原的記錄位置。 不會執行任何復原。

**logtimeStop**

保留供未來使用。

**pfnStatus**

用於報告復原狀態的狀態函數。

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>實作為 <strong>JET_RSTINFO_W</strong> (Unicode) 和 <strong>JET_RSTINFO_A</strong> (ANSI) 。</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>另請參閱

[JetInit3](./jetinit3-function.md)
