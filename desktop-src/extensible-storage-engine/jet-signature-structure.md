---
description: 深入瞭解： JET_SIGNATURE 結構
title: JET_SIGNATURE 結構
TOCTitle: JET_SIGNATURE Structure
ms:assetid: 90d3fd56-be65-4126-b50c-b53e3c3f38f6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269340(v=EXCHG.10)
ms:contentKeyID: 32765629
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
ms.openlocfilehash: d6210853e22fda5085980c2fb285411ba431bb43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972255"
---
# <a name="jet_signature-structure"></a>JET_SIGNATURE 結構


_**適用于：** Windows |Windows Server_

## <a name="jet_signature-structure"></a>JET_SIGNATURE 結構

**JET_SIGNATURE** 結構包含可唯一識別資料庫的資訊。

```cpp
    typedef struct {
      unsigned long ulRandom;
      JET_LOGTIME logtimeCreate;
      char szComputerName[JET_MAX_COMPUTERNAME_LENGTH + 1];
    } JET_SIGNATURE;
```

### <a name="members"></a>成員

**ulRandom**

隨機指派的數位。

**logtimeCreate**

執行[JetCreateDatabase](./jetcreatedatabase-function.md)時的[JET_LOGTIME](./jet-logtime-structure.md) 。

**szComputerName**

電腦之 NetBIOS 名稱的選擇性字串值。 可能無法設定這個值。

### <a name="remarks"></a>備註

您可以使用 [JET_DBINFOMISC](./jet-dbinfomisc-structure.md)的元素來找到這個專案。

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

[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)
