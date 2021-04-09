---
title: 外掛程式包裝函數
description: 包裝函式，可讓您在任何附加至管線的介面卡上呼叫公用函式，而不需要手動取得介面卡的指標。
ms.assetid: a87536bf-3a10-4062-a509-db7f03172307
keywords:
- Windows 生物特徵辨識架構 API Windows 生物特徵辨識架構 API、外掛程式包裝函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e73d7f935ebe1a2dab047f8dd3a09e0bf6ed3855
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840595"
---
# <a name="plug-in-wrapper-functions"></a>外掛程式包裝函數

Windows 生物特徵辨識架構 API 包含包裝函式，可讓您在任何附加至管線的介面卡上呼叫公用函式，而不需要手動取得介面卡的指標。 每個包裝函式都會檢查輸入引數、抓取介面卡指標，以及呼叫要求的函式。 例如， **WbioEngineSetHashAlgorithm** 包裝函式具有下列簽章。


```C++
inline HRESULT
WbioEngineSetHashAlgorithm(
    __inout PWINBIO_PIPELINE Pipeline,
    __in SIZE_T AlgorithmBufferSize,
    __in PUCHAR AlgorithmBuffer
    )
{
    if (ARGUMENT_PRESENT(Pipeline) &&
        ARGUMENT_PRESENT(Pipeline->EngineInterface) &&
        ARGUMENT_PRESENT(Pipeline->EngineInterface->SetHashAlgorithm))
    {
        return Pipeline->EngineInterface->SetHashAlgorithm(
                                            Pipeline,
                                            AlgorithmBufferSize,
                                            AlgorithmBuffer
                                            );
    }
    else
    {
        return E_NOTIMPL;
    }
}
```



此函數會確認 *管線* 引數不是 **Null**、引擎介面卡存在，而且 [**EngineAdapterSetHashAlgorithm**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn) 函式存在。 所有包裝函式都是在 Winbio \_ adapter .h 標頭檔中定義。 下列主題討論可用的包裝函式。

## <a name="in-this-section"></a>本節內容



| 主題                                                               | 描述                                                                                                                        |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [引擎介面卡包裝函式](engine-adapter-wrappers.md)<br/>   | 您可以用來在引擎介面卡上呼叫函式的函式。 這些函式定義于 Winbio \_ adapter. h 中。<br/>  |
| [感應器介面卡包裝函式](sensor-adapter-wrappers.md)<br/>   | 您可以用來在感應器介面卡上呼叫函式的函式。 這些函式定義于 Winbio \_ adapter. h 中。<br/>  |
| [儲存體介面卡包裝函式](storage-adapter-wrappers.md)<br/> | 您可以用來在儲存體介面卡上呼叫函式的函式。 這些函式定義于 Winbio \_ adapter. h 中。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[外掛程式參考](plug-in-reference.md)
</dt> </dl>

 

 





