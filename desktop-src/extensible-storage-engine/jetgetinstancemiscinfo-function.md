---
description: 深入瞭解： JetGetInstanceMiscInfo 函數
title: JetGetInstanceMiscInfo 函式
TOCTitle: JetGetInstanceMiscInfo Function
ms:assetid: 0bfe36fe-4ddd-442b-b934-57a7bfb28e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269183(v=EXCHG.10)
ms:contentKeyID: 32765486
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceMiscInfo
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 07167dc0f2cad5192dc30e9897541b6619086bfc
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481344"
---
# <a name="jetgetinstancemiscinfo-function"></a>JetGetInstanceMiscInfo 函式


_**適用于：** Windows |Windows伺服器_

## <a name="jetgetinstancemiscinfo-function"></a>JetGetInstanceMiscInfo 函式

當實例在線上時， **JetGetInstanceMiscInfo** 函式會抓取實例的相關資訊。

**Windows vista： JetGetInstanceMiscInfo** 是 Windows vista 引進。

```cpp
    JET_ERR JET_API JetGetInstanceMiscInfo(
      __in          JET_INSTANCE instance,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>參數

*實例*

識別將用於 API 呼叫的資料庫實例。

*pvResult*

將接收資訊的緩衝區指標。 緩衝區的類型取決於 *InfoLevel*。 呼叫端會負責適當地對齊緩衝區。

*cbMax*

傳入 *pvResult* 的緩衝區大小（以位元組為單位）。

*InfoLevel*

判斷針對 *實例* 指定的實例，將會抓取何種類型的資訊。 *PvResult* 中儲存的資料格式取決於 *InfoLevel*。

下列選項可用於此參數。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_InstanceMiscInfoLogSignature</p> | <p><em>pvResult</em> 會被視為與此實例相關聯之交易記錄順序的 <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a> 結構。</p> | 



### <a name="return-value"></a>傳回值

此函數會傳回具有下列其中一個傳回碼的 [JET_ERR](./jet-err.md) 資料類型。 如需可能 ESE 錯誤的詳細資訊，請參閱可延伸的[儲存體引擎錯誤](./extensible-storage-engine-errors.md)和[錯誤處理參數](./error-handling-parameters.md)。


| <p>傳回碼</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>作業已成功完成。</p> | 
| <p>JET_errBufferTooSmall</p> | <p>緩衝區太小。</p> | 
| <p>JET_errInvalidParameter</p> | <p>不正確 <a href="gg294048(v=exchg.10).md">JET_INSTANCE</a> 或指定的 <em>InfoLevel</em> 無效。</p> | 



#### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows Server 2008。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | | <p><strong>程式庫</strong></p> | <p>使用 ESENT。</p> | | <p><strong>DLL</strong></p> | <p>需要 ESENT.dll。</p> | 



#### <a name="see-also"></a>另請參閱

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SIGNATURE](./jet-signature-structure.md)
