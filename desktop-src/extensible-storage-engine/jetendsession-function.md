---
description: 深入瞭解： JetEndSession 函數
title: JetEndSession 函式
TOCTitle: JetEndSession Function
ms:assetid: a9a8f98a-258e-4fbb-bed0-657581984a07
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294054(v=EXCHG.10)
ms:contentKeyID: 32765660
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEndSession
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b96ae49ef907cea158d1496339a740e1026ffea
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472564"
---
# <a name="jetendsession-function"></a>JetEndSession 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetendsession-function"></a>JetEndSession 函式

**JetEndSession** 函式會結束會話，並清除和解除配置與指定會話相關聯的任何資源。

```cpp
    JET_ERR JET_API JetEndSession(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

要結束的會話。 當會話結束時，會釋放相關聯的資源。

*grbit*

保留的。 此參數可包含 JET_bitForceSessionClosed 旗標，但此旗標已保留，且設定不會有任何作用。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>無法完成作業，因為與該會話相關聯之實例上的所有活動都不是呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>的結果。</p> | 
| <p>JET_errInvalidParameter</p> | <p>提供的其中一個參數包含未預期的值，或多個參數值的組合產生了非預期的結果。</p> | 
| <p>JET_errInvalidSesid</p> | <p>會話不是有效的 JET 會話。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errOutOfMemory</p> | <p>因為無法配置記憶體，所以操作失敗。</p> | 
| <p>JET_errSessionInUse</p> | <p>這表示會話已在另一個執行緒上使用，或未正確設定或重設會話。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>無法完成作業，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p><p>只有 Windows XP 和更新版本才會傳回此錯誤。</p> | 
| <p>JET_errOutOfBuffers</p> | <p>指出沒有其他緩衝區的系統錯誤。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉。</p> | 



成功時，會話控制碼已關閉且無法使用，而且與此會話相關的所有資源都會清除。

失敗時，有數個額外的錯誤可能會在排序表關閉、資料指標關閉和交易回復時發生。 這些錯誤不太可能發生，而且如果在呼叫 **JetEndSession** 時，您的會話完全不在使用中，則不太可能發生。 如果無法正確清除會話的某些部分，將會傳回這些錯誤。

#### <a name="remarks"></a>備註

此 API 會復原任何開啟的交易 (未認可至層級 0) 。 此外，也會清除與此會話相關聯的所有資料指標，以及已建立或開啟的任何排序表。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginSession](./jetbeginsession-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)
