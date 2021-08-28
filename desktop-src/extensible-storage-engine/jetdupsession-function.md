---
description: 深入瞭解： JetDupSession 函數
title: JetDupSession 函式
TOCTitle: JetDupSession Function
ms:assetid: fa8fbaca-fe48-401e-9700-1303f4842ad9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294141(v=EXCHG.10)
ms:contentKeyID: 32765755
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDupSession
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c22be08630c446f6c5ba106b38be6bc24415325
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466625"
---
# <a name="jetdupsession-function"></a>JetDupSession 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetdupsession-function"></a>JetDupSession 函式

**JetDupSession** 函式會啟動會話，並初始化並傳回 ESE 會話控制碼 ([JET_SESID](./jet-sesid.md)) 。 會話會控制資料庫的所有存取權，並且用來控制交易的範圍。 會話可以用來開始、認可或中止交易。 會話也會用來附加、建立或開啟資料庫。 此會話會當做所有 DDL 和 DML 作業的內容使用。 若要增加資料庫的平行存取和平行存取，可以開始多個會話。

**注意** 此 API 會以所有方式運作，以在傳入的會話實例上呼叫 [JetBeginSession](./jetbeginsession-function.md) 。 不建議使用此函數，建議使用 [JetBeginSession](./jetbeginsession-function.md) 。

```cpp
    JET_ERR JET_API JetDupSession(
      __in          JET_SESID sesid,
      __out         JET_SESID* psesid
    );
```

### <a name="parameters"></a>參數

*sesid*

要用來做為複製或開始會話之來源的會話。

*psesid*

在成功傳回時，會話控制碼初始化之變數的指標。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p><p>只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errInvalidParameter</p> | <p>提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errOutOfMemory</p> | <p>因為無法配置記憶體，所以操作失敗。</p> | 
| <p>JET_errOutOfSessions</p> | <p>引擎可讓用戶端啟動的會話數目有限。 您可以使用 <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> 搭配 <em>JET_paramMaxSessions</em> 常數來變更這個值。 會話的預設數目為16。 如需<em>JET_paramMaxSessions</em>的詳細資訊，請參閱<a href="gg294139(v=exchg.10).md">系統參數</a>。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 



成功時，會初始化會話控制碼，並可用於資料庫作業。

失敗時，沒有可用的會話，或無法初始化新的會話。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_SESID](./jet-sesid.md)  
[JetBeginSession](./jetbeginsession-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)  
[系統參數](./extensible-storage-engine-system-parameters.md)
