---
title: 執行 IMediaObject FreeStreamingResources
description: 執行 IMediaObject FreeStreamingResources
ms.assetid: 970dd10b-a7a0-4ba0-97e3-725d5c914500
keywords:
- Windows Media Player 外掛程式，Echo 範例串流資源
- 外掛程式，Echo 範例串流資源
- 數位信號處理外掛程式，Echo 範例串流資源
- DSP 外掛程式，Echo 範例串流資源
- Echo DSP 外掛程式範例，串流資源
- Echo DSP 外掛程式範例，釋放記憶體
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a31a293cfc68caf43496d031426de2441c9c1d05
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839687"
---
# <a name="implementing-imediaobjectfreestreamingresources"></a>執行 IMediaObject：： FreeStreamingResources

在外掛程式物件終結之前，您的程式碼必須先釋放任何配置的記憶體。 Windows Media Player 會呼叫 **FreeStreamingResources** 以允許您這樣做。 基於安全考慮，外掛程式 wizard 建立的範例會在 **FinalRelease** 方法中包含對 **FreeStreamingResources** 的呼叫，以確保釋放記憶體。 您必須將下列程式碼新增至 Echo 範例的 **FreeStreamingResources** ：


```
// Test whether a buffer exists.
if (m_pbDelayBuffer)
{
    delete m_pbDelayBuffer;
    m_pbDelayBuffer = NULL;
    m_pbDelayPointer = NULL;
    m_cbDelayBuffer = 0;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用串流資源**](working-with-streaming-resources.md)
</dt> </dl>

 

 




