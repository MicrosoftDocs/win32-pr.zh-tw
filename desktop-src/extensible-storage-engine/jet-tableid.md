---
description: 深入瞭解： JET_TABLEID
title: JET_TABLEID
TOCTitle: JET_TABLEID
ms:assetid: 09705c32-97d8-460c-8b58-921497e29c13
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269182(v=EXCHG.10)
ms:contentKeyID: 32765485
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
ms.openlocfilehash: 04e59ddada8715872978ccc21da11a349e1b7c43
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983571"
---
# <a name="jet_tableid"></a>JET_TABLEID


_**適用于：** Windows |Windows伺服器_

## <a name="jet_tableid"></a>JET_TABLEID

JET_TABLEID 資料類型包含資料庫資料指標的控制碼，可用於呼叫 JET API。 資料指標只能搭配用來開啟該資料指標的會話使用。

```cpp
    typedef JET_API_PTR JET_TABLEID;
```

### <a name="data-types"></a>資料類型

JET_TABLEID

**Null** 或 [JET_tableidNil](./invalid-handle-constants.md)可以用來表示不正確資料指標控制碼。

### <a name="remarks"></a>備註

資料指標會管理資料庫引擎的資料表使用。 資料指標可以執行下列工作：

  - 掃描記錄

  - 搜尋記錄

  - 選擇有效的排序次序以及這些記錄的可見度

  - 建立、更新或刪除記錄

  - 修改資料表的架構

當基礎資料表的狀態或類型變更時，資料指標支援的功能可能會變更。 例如，臨時表可能不允許在使用某些選項開啟資料時進行搜尋。 資料指標一律會完全連接到基礎資料表，並直接與該資料互動，而不需要任何快取。 此資料庫引擎公開的所有核心 ISAM 功能幾乎都可透過資料指標運作。

您可以使用 [JetOpenTable](./jetopentable-function.md) 或 [JetOpenTempTable](./jetopentemptable-function.md)來建立資料指標。 您可以使用 [JetDupCursor](./jetdupcursor-function.md)來重復資料指標。 您可以使用 [JetCloseTable](./jetclosetable-function.md) 明確地關閉資料指標，或使用 [JetEndSession](./jetendsession-function.md) 或 [JetTerm](./jetterm-function.md)以隱含方式關閉資料指標。 如果資料指標是在中止的交易中開啟，則 [JetRollback](./jetrollback-function.md) 也可以隱含地將它關閉。 可以在任何時間建立的最大資料指標數目是由 [JET_paramMaxCursors](./resource-parameters.md)所控制，可以使用 [JetSetSystemParameter](./jetsetsystemparameter-function.md)進行設定。

### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JET_paramMaxSessions](./resource-parameters.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetDupCursor](./jetdupcursor-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetOpenTable](./jetopentable-function.md)  
[JetOpenTempTable](./jetopentemptable-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetTerm](./jetterm-function.md)
