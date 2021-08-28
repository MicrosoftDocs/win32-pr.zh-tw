---
description: 深入瞭解： JET_DBID
title: JET_DBID
TOCTitle: JET_DBID
ms:assetid: 516acb79-aa75-4609-81b6-3b2e4e0c95af
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269248(v=EXCHG.10)
ms:contentKeyID: 32765550
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
ms.openlocfilehash: c576734a3e2da71f041509e5b7d7d9244427dbb8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986691"
---
# <a name="jet_dbid"></a>JET_DBID


_**適用于：** Windows |Windows伺服器_

## <a name="jet_dbid"></a>JET_DBID

**JET_DBID** 資料類型包含資料庫的控制碼。 資料庫控制碼是用來管理資料庫的架構。 它也可以用來管理該資料庫內的資料表。

```cpp
    typedef unsigned long JET_DBID;
```

### <a name="data-types"></a>資料類型

JET_DBID

資料庫的控制碼。

JET_dbidNil 的值表示控制碼無效。

### <a name="remarks"></a>備註

資料庫控制碼是透過呼叫 [JetCreateDatabase](./jetcreatedatabase-function.md) 或 [JetOpenDatabase](./jetopendatabase-function.md)來建立。

[JetCloseDatabase](./jetclosedatabase-function.md)可以明確關閉資料庫控制碼，或由[JetEndSession](./jetendsession-function.md)或[JetTerm](./jetterm-function.md)隱含關閉。

資料庫控制碼只能在建立它的會話內使用。 資料庫控制碼是否存在，會對應至資料庫的邏輯開啟。 邏輯開啟與資料庫的實體開放式不同，這會在資料庫附加至系統時發生。

### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetEndSession](./jetendsession-function.md)
