---
description: 用來產生目錄的 RunGraphAndWait 函式
ms.assetid: f6eac1cf-05c3-48b6-b9b4-02966facdc95
title: 用來產生目錄的 RunGraphAndWait 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d14b71454bd8c47ab22f165ba59951037bf669a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191756"
---
# <a name="rungraphandwait-function-for-generating-a-table-of-contents"></a><span data-ttu-id="00009-103">用來產生目錄的 RunGraphAndWait 函式</span><span class="sxs-lookup"><span data-stu-id="00009-103">RunGraphAndWait Function for Generating a Table of Contents</span></span>

<span data-ttu-id="00009-104">下列函式是範例程式中的 helper 函式，會在 [自動產生目錄](generating-a-table-of-contents-automatically.md)中討論。</span><span class="sxs-lookup"><span data-stu-id="00009-104">The following function is a helper function in an example program that is discussed in [Generating a Table of Contents Automatically](generating-a-table-of-contents-automatically.md).</span></span>


```C++
HRESULT RunGraphAndWait(IGraphBuilder* pGraph)
{
   IMediaControl* pControl = NULL;
   HRESULT hr = pGraph->QueryInterface(IID_IMediaControl, (VOID**)&pControl);

   if(SUCCEEDED(hr))
   {
      hr = pControl->Run();

      if(SUCCEEDED(hr))
      {
         IMediaEvent* pEvent = NULL;
         hr = pControl->QueryInterface(IID_IMediaEvent, (VOID**)&pEvent);

         if(SUCCEEDED(hr))
         {
           long eventCode = 0;
           hr = pEvent->WaitForCompletion(INFINITE, &eventCode);
           pEvent->Release();
           pEvent = NULL;
         }
      }

      pControl->Release();
      pControl = NULL;
   }

   return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="00009-105">相關主題</span><span class="sxs-lookup"><span data-stu-id="00009-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00009-106">自動產生目錄</span><span class="sxs-lookup"><span data-stu-id="00009-106">Generating a Table of Contents Automatically</span></span>](generating-a-table-of-contents-automatically.md)
</dt> </dl>

 

 



