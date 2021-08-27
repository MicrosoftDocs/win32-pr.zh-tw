---
description: 深入瞭解： JetSetTableSequential 函數
title: JetSetTableSequential 函式
TOCTitle: JetSetTableSequential Function
ms:assetid: 874ddd3c-0d69-4d48-b61a-e9e0457426ef
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269323(v=EXCHG.10)
ms:contentKeyID: 32765613
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetTableSequential
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a8b49b112c9566b15226e8ffd52f4240cff2fb8
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471714"
---
# <a name="jetsettablesequential-function"></a>JetSetTableSequential 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetsettablesequential-function"></a>JetSetTableSequential 函式

**JetSetTableSequential** 函式會通知資料庫引擎應用程式正在掃描包含指定資料指標的整個目前索引。 因此，用來存取索引資料的方法將會進行微調，使此案例的速度越快越好。

**Windows xp：****JetSetTableSequential** 是在 Windows xp 引進。  

```cpp
    JET_ERR JET_API JetSetTableSequential(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

*tableid*

要用於此呼叫的資料指標。

*grbit*

指定零或多個下列選項的位群組。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitPrereadForward</p> | <p>此選項是用來以正向方向編制索引。</p><p><strong>Windows 7：</strong><strong>JET_bitPrereadForward</strong>是 Windows 7 中引進的。  </p> | 
| <p>JET_bitPrereadBackward</p> | <p>此選項可用來在反向方向編制索引。</p><p><strong>Windows 7：</strong><strong>JET_bitPrereadBackward</strong>是 Windows 7 中引進的。  </p> | 



### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errClientRequestToStopJetService</p> | <p>作業無法完成，因為呼叫 <a href="gg269240(v=exchg.10).md">JetStopService</a>時，與會話相關聯之實例上的所有活動都已停止。</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>作業無法完成，因為與會話相關聯的實例發生嚴重錯誤，需要撤銷所有資料的存取權，以保護該資料的完整性。</p><p><strong>Windows XP：</strong> 此傳回值會在 Windows XP 中引進。</p> | 
| <p>JET_errNotInitialized</p> | <p>無法完成作業，因為與會話相關聯的實例尚未初始化。</p> | 
| <p>JET_errRestoreInProgress</p> | <p>作業無法完成，因為與會話相關聯的實例正在進行還原作業。</p> | 
| <p>JET_errTermInProgress</p> | <p>無法完成作業，因為與會話相關聯的實例正在關閉中。</p> | 



如果此函式成功，則資料指標的目前索引會針對整個索引的連續掃描進行優化。 不會變更資料庫狀態。

如果此函式失敗，將不會變更資料指標的設定。 不會變更資料庫狀態。

#### <a name="remarks"></a>備註

如果應用程式需要有效率地掃描索引的已知子集，則在使用 [JetSetIndexRange](./jetsetindexrange-function.md)建立索引範圍時也會執行類似的優化。 只有 Windows XP 和更新版本才提供這項優化。

如果應用程式需要有效率地掃描索引的未知子集，則不應採取任何動作。 引擎可以自動偵測掃描行為，而且會事先提取資料。 不過，這種行為並不是積極的。

這項優化可讓您有效率地掃描主要索引，並讓您只在次要索引中以有效率的方式掃描索引項目目資料。 它不會在您有效率地抓取記錄資料時，掃描次要索引。 這是因為引擎不會在記錄資料上執行預先讀取。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista 或 Windows XP。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008 或 Windows server 2003。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)  
[JetStopService](./jetstopservice-function.md)
