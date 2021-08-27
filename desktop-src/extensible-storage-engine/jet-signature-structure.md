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
ms.openlocfilehash: da4684872358d9d6751812b2adb2b2bea819a2e3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476474"
---
# <a name="jet_signature-structure"></a>JET_SIGNATURE 結構


_**適用于：** Windows |Windows伺服器_

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


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)
