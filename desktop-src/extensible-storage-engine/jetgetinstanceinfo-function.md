---
description: 深入瞭解： JetGetInstanceInfo 函數
title: JetGetInstanceInfo 函式
TOCTitle: JetGetInstanceInfo Function
ms:assetid: ffccdac0-3631-4753-876a-90ddfdd0252f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294149(v=EXCHG.10)
ms:contentKeyID: 32765763
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceInfoW
- JetGetInstanceInfo
- JetGetInstanceInfoA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9dfc8bec0e6cee6e127dc99135d82db3ee3001ab
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478344"
---
# <a name="jetgetinstanceinfo-function"></a>JetGetInstanceInfo 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetgetinstanceinfo-function"></a>JetGetInstanceInfo 函式

**JetGetInstanceInfo** 函數會抓取正在執行之實例的相關資訊。

**Windows xp： JetGetInstanceInfo** 是在 Windows xp 引進。

```cpp
    JET_ERR JET_API JetGetInstanceInfo(
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo
    );
```

### <a name="parameters"></a>參數

*pcInstanceInfo*

緩衝區的指標，此緩衝區會接收儲存在 *paInstanceInfo* 中的元素數目。

*paInstanceInfo*

緩衝區的指標，此緩衝區會接收結構陣列第一個元素的位址。

### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errInvalidParameter</p> | <p>提供的其中一個參數包含未預期的值，或包含的值在與另一個參數的值結合時並沒有意義。 <strong>JetGetInstanceInfo</strong>會在下列情況傳回此錯誤：</p><ul><li><p><em>pcInstanceInfo</em> 或 <em>paInstanceInfo</em> 為 Null。</p></li></ul> | 
| <p>JET_errOutOfMemory</p> | <p>記憶體不足，無法處理要求。</p> | 



#### <a name="remarks"></a>備註

資料庫引擎會配置 [JET_INSTANCE_INFO](./jet-instance-info-structure.md) 結構的陣列。 呼叫端負責使用 [JetFreeBuffer](./jetfreebuffer-function.md)釋出此記憶體。

如果沒有使用中的實例， **JetGetInstanceInfo** 會傳回 JET_errSuccess，而 *pcInstanceInfo* 會收到值為0的值。

#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista 或 Windows XP。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008 或 Windows server 2003。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | | <p><strong>Unicode</strong></p> | <p>實作為 <strong>JetGetInstanceInfoW</strong> (Unicode) 和 <strong>JetGetInstanceInfoA</strong> (ANSI) 。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_INSTANCE_INFO](./jet-instance-info-structure.md)  
[JetFreeBuffer](./jetfreebuffer-function.md)
