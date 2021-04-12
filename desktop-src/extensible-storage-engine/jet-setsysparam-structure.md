---
description: 深入瞭解： JET_SETSYSPARAM 結構
title: JET_SETSYSPARAM 結構
TOCTitle: JET_SETSYSPARAM Structure
ms:assetid: 3c0fdd28-99bd-4026-b64b-6859ef9dc91b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269230(v=EXCHG.10)
ms:contentKeyID: 32765532
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
ms.openlocfilehash: 0e88795bb3ee966bf2ad7fa50cc7d2180d7264bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318172"
---
# <a name="jet_setsysparam-structure"></a>JET_SETSYSPARAM 結構


_**適用于：** Windows |Windows Server_

## <a name="jet_setsysparam-structure"></a>JET_SETSYSPARAM 結構

**JET_SETSYSPARAM** 結構的陣列表示使用 [JetEnableMultiInstance](./jetenablemultiinstance-function.md)函式時，設定為引數的一組特定全域系統參數。

**WINDOWS XP：** 此結構是在 Windows XP 中引進的。

```cpp
    typedef struct {
      unsigned long paramid;
      JET_API_PTR lParam;
      const tchar* sz;
      JET_ERR err;
    } JET_SETSYSPARAM;
```

### <a name="members"></a>成員

**paramid**

將設定之系統參數的識別碼。

如需系統參數及其屬性的完整清單，請參閱可延伸 [儲存引擎系統參數](./extensible-storage-engine-system-parameters.md) 。

**lParam**

如果系統參數是整數類型，則為所選取系統參數設定的選擇性值。

**深圳**

如果系統參數是字串類型，則為所選取系統參數設定的選擇性值。

**犯 錯**

使用先前指定的參數呼叫 [JetSetSystemParameter](./jetsetsystemparameter-function.md) 所產生的錯誤。

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
<td><p>實作為 <strong>JET_ SETSYSPARAM_W</strong> (Unicode) 和 <strong>JET_</strong> SETSYSPARAM_A (ANSI) 。</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>另請參閱

[可擴充儲存引擎系統參數](./extensible-storage-engine-system-parameters.md)  
[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JetEnableMultiInstance](./jetenablemultiinstance-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
