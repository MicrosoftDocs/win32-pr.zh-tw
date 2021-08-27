---
description: 深入瞭解： JetIdle 函數
title: JetIdle 函式
TOCTitle: JetIdle Function
ms:assetid: 77e036eb-b894-4ff7-b14f-1564bf21873f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269301(v=EXCHG.10)
ms:contentKeyID: 32765593
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIdle
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: babe3077c01b6b2a9c1f2f55b48921582d6343bd
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984541"
---
# <a name="jetidle-function"></a>JetIdle 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetidle-function"></a>JetIdle 函式

**JetIdle** 函式已無用，且僅供測試用途使用。 **JetIdle** 可以用來執行閒置清除工作，或檢查 ESE 中的版本存放區狀態。

```cpp
    JET_ERR JET_API JetIdle(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫將使用的會話。

*grbit*

位群組，其中包含要用於此呼叫的選項，其中包含零或多個下列位：


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitIdleCompact</p> | <p>觸發版本存放區的清除。</p> | 
| <p>JET_bitIdleFlushBuffers</p> | <p>保留供未來使用。 如果指定此旗標，則 API 會傳回 JET_errInvalidgrbit。</p> | 
| <p>JET_bitIdleStatus</p> | <p>如果版本存放區已滿一半，則會傳回 JET_wrnIdleFull。</p> | 



### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errInvalidParameter</p> | <p>提供給 API 的 <em>grbit</em> 參數無效。</p> | 



如果此函式成功，則會觸發適當的作業，或使用錯誤碼指出版本存放區根據提供的 *grbit* 的填滿程度。

如果此函式失敗，則要求的作業將不會順利完成。

#### <a name="remarks"></a>備註

版本存放區會維護 ESE 的快照集隔離機制。 如果版本存放區的長度超過一半，則程式可能會關閉長時間執行的交易。 如果長時間執行的交易耗盡版本存放區，ESE 將會停止允許對資料庫進行寫入作業。

#### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 
| <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | 
| <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)
