---
description: 深入瞭解： JET_INSTANCE
title: JET_INSTANCE
TOCTitle: JET_INSTANCE
ms:assetid: a4136bec-95b3-42d7-b21b-1df09197bb11
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294048(v=EXCHG.10)
ms:contentKeyID: 32765647
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
ms.openlocfilehash: 1fc288c17c90070d48669c7ad6f1554d52c83278
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481764"
---
# <a name="jet_instance"></a>JET_INSTANCE


_**適用于：** Windows |Windows伺服器_

## <a name="jet_instance"></a>JET_INSTANCE

**JET_INSTANCE** 資料類型包含資料庫實例的控制碼，可用於呼叫 JET API。

```cpp
    typedef JET_API_PTR JET_INSTANCE;
```

### <a name="data-types"></a>資料類型

JET_INSTANCE

**Null** 或 [JET_instanceNil](./invalid-handle-constants.md)可以用來表示不正確實例控制碼。

### <a name="remarks"></a>備註

當您藉由呼叫 [JetCreateInstance](./jetcreateinstance-function.md)、 [JetCreateInstance2](./jetcreateinstance2-function.md)、 [JetInit](./jetinit-function.md)或 [JetInit2](./jetinit2-function.md) 函式來建立資料庫的實例時，就會取得此控制碼。

**Windows XP：** 只有 Windows XP 和更新版本才支援明確使用實例。

**Windows 2000：** 每個進程只支援一個全域實例。

### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetCreateInstance2](./jetcreateinstance2-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)
