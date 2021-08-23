---
description: 深入瞭解：可擴充的儲存體引擎錯誤
title: 可擴充的儲存體引擎錯誤
TOCTitle: Extensible Storage Engine Errors
ms:assetid: 0c071ed6-0ea2-448b-9f9f-e606c5abf3db
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269184(v=EXCHG.10)
ms:contentKeyID: 32765487
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 0c0ee0a4423d5b37913bd7922af07a7b2196a30176b2a1adca37240e03a28594
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721458"
---
# <a name="extensible-storage-engine-errors"></a>可擴充的儲存體引擎錯誤


_**適用于：** Windows |Windows伺服器_

## <a name="extensible-storage-engine-errors"></a>可擴充的儲存體引擎錯誤

可延伸儲存體引擎 (ESE) API 所傳回的所有可能錯誤都是由[JET_ERR](./jet-err.md)資料類型所定義。 如需為此 API 定義的錯誤旗標清單，請參閱可延伸的[儲存體引擎錯誤碼](./extensible-storage-engine-error-codes.md)。

在整個 ESE API 檔中，只會記錄最重要的錯誤。 這些錯誤通常代表 API 使用錯誤或非常重要的錯誤狀況。 請注意，這些 ESE Api 中的任何一項也可能會傳回未針對每個 API 記載的其他錯誤。 在這些情況下，呼叫端應該直接處理錯誤，就像 API 所傳回的任何其他錯誤一樣。 特定的錯誤值接著可以用於診斷用途，例如追蹤。

一般情況下，大於零的值應解釋為警告、值為零應解讀為成功，而小於零的值則應視為錯誤。 這些值中沒有其他模式 (例如，) 的值範圍應該依賴應用程式。

當 ESE 遇到一些較嚴重的錯誤時，它會建立一個事件記錄檔專案，其中包含錯誤的詳細資料。 記錄層級可由 [事件記錄參數](./event-log-parameters.md)控制。

某些應用程式需要能夠以 Hresult 的方式傳回 [JET_ERR](./jet-err.md)s。 下列 c + + 範例顯示如何進行轉換：

```cpp
    #ifndef FACILITY_JET_ERR
    #define FACILITY_JET_ERR 0xE5E
    #endif
    #ifndef HRESULT_FROM_JET_ERR
    #define HRESULT_FROM_JET_ERR( __err )
    (
      ( __err ) == JET_errSuccess ?
      S_OK :
      (
        ( __err ) == JET_errOutOfMemory ?
        E_OUTOFMEMORY :
        MAKE_HRESULT
        (
          (
            ( __err ) < 0 ?
            SEVERITY_ERROR :
            SEVERITY_SUCCESS
          ),
          FACILITY_JET_ERR,
          (
            ( __err ) < 0 ?
            -( __err ) :
            ( __err )
          )
          & 0xFFFF
        )
      )
    )
    
    #endif
```

如需設定系統參數進行錯誤處理的詳細資訊，請參閱 [錯誤處理參數](./error-handling-parameters.md)。

### <a name="see-also"></a>另請參閱

[錯誤處理參數](./error-handling-parameters.md)

[可擴充的儲存體引擎錯誤碼](./extensible-storage-engine-error-codes.md)

[JET_ERR](./jet-err.md)
