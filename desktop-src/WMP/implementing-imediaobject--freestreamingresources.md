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
# <a name="implementing-imediaobjectfreestreamingresources"></a><span data-ttu-id="38d77-109">執行 IMediaObject：： FreeStreamingResources</span><span class="sxs-lookup"><span data-stu-id="38d77-109">Implementing IMediaObject::FreeStreamingResources</span></span>

<span data-ttu-id="38d77-110">在外掛程式物件終結之前，您的程式碼必須先釋放任何配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="38d77-110">It is important that your code releases any allocated memory before the plug-in object is destroyed.</span></span> <span data-ttu-id="38d77-111">Windows Media Player 會呼叫 **FreeStreamingResources** 以允許您這樣做。</span><span class="sxs-lookup"><span data-stu-id="38d77-111">Windows Media Player calls **FreeStreamingResources** to allow you to do this.</span></span> <span data-ttu-id="38d77-112">基於安全考慮，外掛程式 wizard 建立的範例會在 **FinalRelease** 方法中包含對 **FreeStreamingResources** 的呼叫，以確保釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="38d77-112">For safety, the sample created by the plug-in wizard includes a call to **FreeStreamingResources** in the **FinalRelease** method to ensure that the memory is freed.</span></span> <span data-ttu-id="38d77-113">您必須將下列程式碼新增至 Echo 範例的 **FreeStreamingResources** ：</span><span class="sxs-lookup"><span data-stu-id="38d77-113">You must add the following code to **FreeStreamingResources** for the Echo sample:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="38d77-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="38d77-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38d77-115">**使用串流資源**</span><span class="sxs-lookup"><span data-stu-id="38d77-115">**Working with Streaming Resources**</span></span>](working-with-streaming-resources.md)
</dt> </dl>

 

 




