---
description: 深入瞭解： JET_SESID
title: JET_SESID
TOCTitle: JET_SESID
ms:assetid: 56b53532-e0a8-4255-8442-bb90184d91da
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269253(v=EXCHG.10)
ms:contentKeyID: 32765555
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
ms.openlocfilehash: 60920995e72fdc1f45dcc6c083be7bcc1a91b3fa
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466405"
---
# <a name="jet_sesid"></a>JET_SESID


_**適用于：** Windows |Windows伺服器_

## <a name="jet_sesid"></a>JET_SESID

**JET_SESID** 資料類型包含要用於呼叫 JET API 的會話控制碼。

```cpp
    typedef JET_API_PTR JET_SESID;
```

### <a name="data-types"></a>資料類型

JET_SESID

**Null** 或 [JET_sesidNil](./invalid-handle-constants.md)可以用來表示不正確會話控制碼。

### <a name="remarks"></a>備註

會話是 database engine 的交易內容。 您可以使用它來開始、認可或中止交易，這些交易會影響此會話或其他會話所進行之變更的可見度和持久性。

您可以使用 [JetBeginTransaction](./jetbegintransaction-function.md)來啟動交易。 您可以使用 [JetBeginSession](./jetbeginsession-function.md)來建立會話。 可以在任何時間建立的會話數目上限是由 [JET_paramMaxSessions](./resource-parameters.md)所控制，可以透過 [JetSetSystemParameter](./jetsetsystemparameter-function.md)來設定。

會話是由呼叫 [JetEndSession](./jetendsession-function.md) 明確結束，或呼叫 [JetTerm](./jetterm-function.md)以隱含方式結束。

每個會話一次只能供一個執行緒使用。 此外，引擎的預設行為是在呼叫 [JetBeginTransaction](./jetbegintransaction-function.md) 的第一次呼叫時，將會話限制在相同的執行緒上，直到發出 [JetCommitTransaction](./jetcommittransaction-function.md) 或 [JetRollback](./jetrollback-function.md) 的相符呼叫為止。 您可以使用 [JetSetSessionCoNtext](./jetsetsessioncontext-function.md) 和 [JetResetSessionCoNtext](./jetresetsessioncontext-function.md)設定自訂會話內容，來變更此行為，以移除第二個限制。

### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JET_paramMaxSessions](./resource-parameters.md)  
[JetBeginSession](./jetbeginsession-function.md)  
[JetBeginTransaction](./jetbegintransaction-function.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetResetSessionCoNtext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSessionCoNtext](./jetsetsessioncontext-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetTerm](./jetterm-function.md)
